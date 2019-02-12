<template>
  <div class="bg">
    <nuxt />
  </div>
</template>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background: linear-gradient(135deg, rgba(251,143,41,1) 0%, rgba(235,91,103,1) 32%, rgba(224,63,154,1) 63%, rgba(211,39,234,1) 100%);
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
.bg {
  /* The image used */
  background: linear-gradient(135deg, rgba(251,143,41,1) 0%, rgba(235,91,103,1) 32%, rgba(224,63,154,1) 63%, rgba(211,39,234,1) 100%);

}


.button--grey:hover {
  color: #fff;
  background-color: #000;
}
</style>
