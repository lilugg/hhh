<template>
  <div id="app">
     <header>
       <div class="loge">
        <p class="iconfont icon-angle-left"></p>
        <p><span class="iconfont icon-fangdajing"></span>面试列表</p>
        <p class="iconfont icon-gengduo"></p>
       </div>
      <div class="list">
        <span v-for="(item,index) in dataJson" :class="{active:index==num}" @click="click(index)" :key="index">{{item.type}}</span>
      </div>
     </header>
     <section>
       <ul>
           <p class="p" v-if="num==0" style=" text-align: center;  margin-top: 30px; color:#666; flex:1 background:#fff">{{msg}}</p>
         <HelloWorld v-for="(item,index) in dataJson[num].list" :key="index" :option="item"/>
        
       </ul>
     </section>
     <footer></footer>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import dataJson from './data/data.json'
export default {
  name: 'App',
  data(){
    return{
      dataJson,
      num:1,
      msg:""
    }
  },
  methods:{
click(index){
  if(index==0){
     this.msg="当前分类还没有面试！"
  }
this.num=index;
}
  },
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
@import"./conmons.scss";
#app ,section{
 width: 100%;
 height: 100%;
 overflow: hidden;
 display: flex;
 flex-direction: column;
 background: #EEEEEE;
}
header{
  width: 100%;
  height: 80px;
  padding: 0 5px;
  background-color: #fff;
  .loge{
    width: 100%;
    height: 40px;
    display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #ccc;
  }
}
.list{
  display: flex;
  height: 40px;
  justify-content: space-between;
  align-items: center;
}
.p{
  width: 100%;
height: 552px;
overflow: hidden;
background-color: #fff;
}
.list span{
  padding-bottom:12px;
}
.list span.active{
  border-bottom: 2px solid #4281BD;
  color:#4281BD;


}
ul{
  width: 100%;
  flex:1;
  overflow:auto; 
}

</style>
