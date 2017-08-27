<template>
<div>
<h2>gongzuojingli</h2>
    <form> 
      <div v-for="(work,index) in  workHistory"> 
      <input v-model="work.company">gongsi</input>
      <input v-model="work.content">neirong</input>
      <br>
      <button v-on:click="removeWorkHistory(index)">shanchu</button>
       <hr>
       </div>
      <button v-on:click="addWorkHistory">tianjia</button>
        </form>  
</div>                                       
</template>
<script>
export default {
  props:['workHistory'],
  methods:{
  
  addWorkHistory(){
this.workHistory.push({
company:'',content:''
})
},
removeWorkHistory(index){
this.workHistory.splice(index,1)
}
 }
 }


</script>
