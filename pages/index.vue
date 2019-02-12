<template>
  <section class="container">
    <div class="row">
    <div class="col">
      <div class="card" style="border:3px solid rgb(236, 94, 100); margin:0 auto; min-width:260px;width:300px;height:auto;border-radius:4px; box-shadow: 0px 0px 32px #4d4d4d80;">

        <div class="card-body">
          <img src="/logo.png" class="card-img-top" alt="..." style="display:block;margin:50px auto 0;width:180px;height:180px;">
          <br>
          <br>
          <h2 style="text-align: center; font-family: Bash-font; color: #666666; line-height: 0.8"><p>Big things have</p><p>small beginnings</p></h2>
          <br>
          <br>
          <timer>Wait for it</timer>
          <br>
          <br>
        </div>

      </div>
      <div class="row">
          <div class="col">
            <footer style="text-align: center; font-family: Bash-italic; color: #fff; font-size: 0.9rem;">Copyright &copy; Bash 2018</footer>
          </div>
      </div>
    </div>

    </div>
  </section>
</template>

<script>
import timer from '~/components/timer.vue'

export default {
  components: {
    timer
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

@font-face {
  font-family: 'Bash-font';
  src: url("~assets/fonts/AppleGaramond-Light.ttf") format("truetype");

}

@font-face {
  font-family: 'Bash-italic';
  src: url("~assets/fonts/AppleGaramond-LightItalic.ttf") format("truetype");

}


</style>
