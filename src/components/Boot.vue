<template>
    <div id="dosLoading">
        <div class="dosLogo">
            <!-- <img id="dosLogoImage" src=""> -->
            <div class="">
                ~~OS 2019 v1 <br>
                Copyright (C) finncho<br><br>
                E:\finncho\dir_
            </div>
        </div>
        <ul id="taskList"></ul>
        <div id="dosCaretContainer">
            <div id="dosCaret"></div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            needsLoading: true,
            dosLoading: '',
            taskList: '',
            tasksLength: 120,
            iter: 0.3,
            taskSpeed: 1,
            tasks: {}
        }
    },
    mounted() {
        this.dosLoading = document.getElementById('dosLoading')
        this.taskList = document.getElementById('taskList')
        if (this.needsLoading) {
            this.runTasks();
        }else {
            this.fullyLoaded();
        }
    },
    methods: {
        getRandomIndexOfArray(arrayLenght) {
            return Math.floor(Math.random() * Math.floor(arrayLenght));
        },
        runTasks() {
            this.setTask()
            var list = document.createElement('li');
            var action = this.tasks.action[this.getRandomIndexOfArray(this.tasks.action.length)];
            var subject = this.tasks.subject[this.getRandomIndexOfArray(this.tasks.subject.length)];
            var resultIndex = this.getRandomIndexOfArray(this.tasks.result.length);
            var result = this.tasks.result[resultIndex];
            var sentence = action+" "+subject+": "+result;

            list.appendChild(document.createTextNode(sentence));
            taskList.appendChild(list);

            //Highligh if if a failed task
            if (resultIndex > 7) {
                list.style.color = 'yellow';
            }
            this.dosLoading.scrollTop = this.dosLoading.scrollHeight;
            this.iter ++;
            if (this.iter < this.tasksLength) {
                var fakeWorkloadTime = (Math.random()*100)*this.taskSpeed;
                if(this.iter % 10){
                    fakeWorkloadTime = fakeWorkloadTime/(this.iter/10);
                }else {
                    fakeWorkloadTime = fakeWorkloadTime*(this.iter/10);
                }
                setTimeout(this.runTasks, fakeWorkloadTime);
            }else {
                setTimeout(this.fullyLoaded, 100);
            }
        },
        fullyLoaded(){
            this.dosLoading.parentNode.removeChild(this.dosLoading);
        },
        setTask() {
            this.tasks.action = [
                'Loading','Generating','Deleting','Cutting','Connecting','Pushing','Crashing','Installing',
                'Pulling','Swimming','Moving','Watching','Following','Liking','Processing','Winning',
                'Twitting','Posting','Judging','Cleaning','Mopping','Skipping','Correcting','Disliking',
                'Unfollowing','Gathering','Frying','Asking','Bypassing','Stealing','Hacking','Petting'
            ];
            this.tasks.subject = [
                'Kittens','Bad pictures','Ugly fonts','Netflix','Facebook fans','Instagram follower',
                'Twitter','Entire Google Database','Selfies','Cats','Chihuahuas',
                'Fake news','Whale screams','Sunglasses','Twelve legged dogs','Grandmas fennel salad','Colours',
                'Brussel Sprouts','Irrelevant questions','Preposterous ','TV Shows',
                'Britney Spears','Surroundings','Security restrictions','User webcam without consent','User Credit card'
            ];
            this.tasks.result = [
                'Successful','Done','Completed','Nailed','Cracked','Too lazy to do it',
                'EO340 Permission Denied','Warning, Dangerous contents','Failed','Not Found','Fatal Error'
            ];
        }
    }
}
</script>

<style lang="scss" scoped>
#dosLoading{
position: absolute;
width: 100%;
height: 100%;
background-color: #000;
z-index: 999999;
font-size: 14px;
text-transform: uppercase;
overflow: hidden;
color: #fff;
line-height: 22px;
letter-spacing: 3.6px
    p {
        max-width: 500px;
    }
}
#dosLogoImage{
  width: 125px;
  margin: 40px;
}
.dosLogo{
  display: flex;
  height: 140px;
  align-items: center;
  font-size: 19px;
    text-transform: none;
    letter-spacing: 0;
    padding-top: 30px;

}
#dosLogoImage{
  width: 125px;
  margin: 40px;
}
#taskList{
  padding: 40px 0px 0px 40px;
}
#dosCaretContainer{
  padding: 10px 0px 40px 40px;
}
#dosCaret{
  width: 10px;
  height: 20px;
  background-color: white;
  animation: caretBlinker 800ms steps(2, start) infinite;
}
@keyframes caretBlinker {
  0%   { opacity: 0; }
  50%   { opacity: 0; }
  51%   { opacity: 1; }
  100% { opacity: 1; }
}
</style>