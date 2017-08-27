<template>
    <div id="editor">
    <nav>
    <ol>
<li v-for="i in [0,1,2,,3,4,5]"
    v-bind:class="{active:currentTab === i}"
    v-on:click="currentTab = i"
>
<svg class="icon">
    <use v-bind:xlink:href="`#icon-${icons[i]}`"></use>
</svg>
</li>
    </ol>
    </nav>
     <ol class="panes">
      <li v-bind:class="{active:currentTab === 0}">
      
      <ProfileEditor v-bind:profile="profile" />
      </li>
       <li v-bind:class="{active:currentTab === 1}">
        <WorkEditor v-bind:workHistory="workHistory" />                
      </li>
       <li v-bind:class="{active:currentTab === 2}">
       <h2>xuexijingli</h2>
       </li>
       <li v-bind:class="{active:currentTab === 3}">
       <h2>xiangmujingli</h2>
      </li>
       <li v-bind:class="{active:currentTab === 4}">
       <h2>huojiangjingli</h2>
      </li>
       <li v-bind:class="{active:currentTab === 5}">
       <h2>lianxifangshi</h2>
      </li>
     </ol>
    </div>
</template>
<script>
import ProfileEditor from './ProfileEditor'
import WorkEditor from './WorkEditor'
export default{
components:{ProfileEditor,WorkEditor},
data(){
return {
currentTab:0,
icons:['shenfenzheng','heart','shenfenzheng','heart','shenfenzheng','heart'],
profile:{
name:"",
city:"",
birth:""
},
workHistory:[
{company:'',content:''},
]
}
},
methods:{

},
}
</script>
<style>
#editor{
min-height:100px;
display:flex;
}
#editor>nav{
width:100px;
background:black;
}
#editor>nav>ol>li{
list-style:none;
color:white;

font-size:30px;
margin:20px 0px;
}
#editor>nav>ol>li.active{
background:white;
color:black;
}
#editor>ol>li{
display:none;
}

#editor>ol>li.active{
display:block;
}
.panes>li input{
display:block;
margin:10px 0px;
}
</style>
