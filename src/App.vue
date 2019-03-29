<template>
  <div id="app">
   <VueHeader></VueHeader>
   <VueBody></VueBody>
   <VueFooter></VueFooter>
  </div>
</template>

<script>
import VueHeader from './components/VueHeader'
import VueBody from './components/VueBody'
import VueFooter from './components/VueFooter'
export default {
  name: 'App',
  components:{
    VueHeader,
    VueBody,
    VueFooter
  }
}
</script>

<style>
@media screen and (min-width:320px) and (max-width:374px) and (orientation:portrait) {
    html { font-size: 625%; }
}
@media screen and (min-width:360px) and (max-width:374px) and (orientation:portrait) {
    html { font-size: 703%; }
}
@media screen and (min-width:375px) and (max-width:383px) and (orientation:portrait) {
    html { font-size: 732.4%; }
}
@media screen and (min-width:384px) and (max-width:399px) and (orientation:portrait) {
    html { font-size: 750%; }
}
@media screen and (min-width:400px) and (max-width:413px) and (orientation:portrait) {
    html { font-size: 781.25%; }
}
@media screen and (min-width:414px) and (max-width:431px) and (orientation:portrait){
    html { font-size: 808.6%; }
}
@media screen and (min-width:432px) and (max-width:479px) and (orientation:portrait){
    html { font-size: 843.75%; }
}
@media  (min-width: 480px) and (orientation:portrait){
    html { font-size: 625%; }
}
html,body,a,button,input,textarea,img,ul,li,p,dl,dd,h1,h2,h3,h4,h5,h6{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
a,button,input,textarea,img{
  -webkit-tap-highlight-color: transparent;
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  outline: none;
}
body {
  height: 100%;
  width: 100vw;
  overflow: hidden;
  font-family: Helvetica Neue, Helvetica, PingFang SC, Hiragino Sans GB, Microsoft YaHei, 微软雅黑, Arial, sans-serif;
  font-size: 16px;
  line-height: 1.43;
  color: #333;
  word-wrap: break-word;
  word-break: normal;
  hyphens: auto;
  transition:.5s;
  background: rgba(138, 138, 138, 0.2);
}

a {
  text-decoration: none;
  color: #4078c0;
}

img {
  border-style: none;
}

ul{
  list-style: none;
}

::-webkit-scrollbar-track {
  border-radius: 0;
  padding: 0;
  background-color: transparent;
}

::-webkit-scrollbar-thumb {
  border-radius: 10px;
  padding: 0;
  background-color: rgba(0, 0, 0, .2);
}

::-webkit-scrollbar {
  width: 7px;
  height: 7px;
  background-color: transparent;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity .3s;
}
.fade-enter, .fade-leave-to{
  opacity: 0;
}
</style>
