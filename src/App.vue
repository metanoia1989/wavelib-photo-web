<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>


export default {
  name: 'App',
  created() {
    (function  () {  
        function resi() {  
          var html = document.querySelector("html");  
          var wW = document.body.clientWidth || document.documentElement.clientWidth;  
          var maxW = 640;  
          var minW = 320;  
          if (wW > maxW) wW = maxW;  
          var ratio = wW / minW;  
          html.style.fontSize = 50 * ratio + "px"  
        }  

        window.addEventListener("DOMContentLoaded", function() {  
            var bodys = document.querySelector("body").style;  
            bodys.opacity = "1";  
            bodys.filter = "alpha(opacity=100)";  
            resi()  
        });  
        window.addEventListener("resize", resi);  
    })();   
  },
}
</script>
<style>
  @import url(./assets/css/global.css);
</style>
