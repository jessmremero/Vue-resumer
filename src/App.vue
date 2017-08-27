<template>
  <div id="app">
    <Topbar class="topbar"/>
    <main>
      <Editor class="editor"/>
     
      <Preview class="preview"/>
    
    </main>
  </div>
</template>

<script>
import Topbar from './components/Topbar'
import Editor from './components/Editor'
import Preview from './components/Preview'
export default {
   components: {
   Topbar , Editor , Preview
}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display:flex;
  height:100vh;
  flex-direction: column;
}
.topbar{
 background:white;
}
.editor{
background:white;
}
.preview{
background:white;
}


main{
 display:flex;
 flex:1;
 background:#ddd;
 
}
main > .editor{
  width:40em;
  margin:16px 8px 16px 16px;
  box-shadow:0 0 3px hsla(0,0,0,0.5);
  border-radius:4px;
}
main > .preview{
  flex:1;
  margin:16px 16px 16px 8px;
  border-radius:4px;
}

   .icon {
       width: 1em; height: 1em;
       vertical-align: -0.15em;
       fill: currentColor;
       overflow: hidden;
    }</style>
