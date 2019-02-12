<template>
  <h4 style="text-align: center;display: block;margin-left: auto;margin-right: auto;width: 75%; font-family: Bash-italic; color: #666666">
    {{days}} days, {{hours}} hours, {{minutes}} minutes, {{seconds}} seconds</h4>
</template>

<style>
  @font-face {
    font-family: 'Bash-italic';
    src: url("~assets/fonts/AppleGaramond-LightItalic.ttf") format("truetype");

  }
</style>
<script>
import Vue from "vue";
export default {
    data: function () {
        return {
            timer: "",
            wordString: {},
            start: "",
            end: "",
            interval: "",
            days: "",
            minutes: "",
            hours: "",
            seconds: "",
            message: "",
            statusType: "",
            statusText: "",

        };
    },
    mounted() {
        this.start = new Date().getTime();
        this.end = new Date("May 25, 2019 15:37:25").getTime();
        // Update the count down every 1 second
        this.timerCount("Sep 8, 2018 16:37:25", this.end);
        this.interval = setInterval(() => {
            this.timerCount(this.start, this.end);
        }, 1000);
    },
    methods: {
        timerCount: function (start, end) {
            // Get todays date and time
            var now = new Date().getTime();
            // Find the distance between now an the count down date
            var distance = start - now;
            var passTime = end - now;

            if (distance < 0 && passTime < 0) {
                this.statusType = "expired";
                clearInterval(this.interval);
                return;

            } else if (distance < 0 && passTime > 0) {
                this.calcTime(passTime);
                this.statusType = "running";


            } else if (distance > 0 && passTime > 0) {
                this.calcTime(distance);
                this.statusType = "upcoming";

            }
        },
        calcTime: function (dist) {
            // Time calculations for days, hours, minutes and seconds
            this.days = Math.floor(dist / (1000 * 60 * 60 * 24));
            this.hours = Math.floor((dist % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            this.minutes = Math.floor((dist % (1000 * 60 * 60)) / (1000 * 60));
            this.seconds = Math.floor((dist % (1000 * 60)) / 1000);
        }
    }

}



</script>