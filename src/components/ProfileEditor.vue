<template>
<div>
 <h2>gerenjingli</h2>
       <form>
         <input value="mingzi" v-model="profile.name" >xingming</input>
         <input value="chengshi" v-model="profile.city">chengshi</input>
         <input value="chushengnianyue" v-model="profile.birth">chushengnianyue</input>
       </form>
</div>
</template>
<script>
export default {
  props:['profile']
 }
</script>
