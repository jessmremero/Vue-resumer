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
 background:red;
}
.editor{
background:yellow;
}
.preview{
background:green;
}


main{
 display:flex;
 flex:1;
 
}
main > .editor{
  width:20em;
}
main > .preview{
  flex:1;
}
</style>
