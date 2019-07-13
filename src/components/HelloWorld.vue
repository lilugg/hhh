<template>
      <li>
          <h2><p>{{option.title}}</p><span class="fang tip" >{{option.abandon}}</span></h2>
          <p class="side">{{option.site}}</p>
          <h4><p>面试时间：{{option.time}}{{option.hour}}</p><span class="ti">{{option.hint}}</span></h4>
        </li>
</template>

<script>
export default {
  name: 'HelloWorld',
  props:["option"]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
 li{
  margin-top: 10px;
  height: 150px;
  width: 100%;
  background-color: #fff;
 
  
  h2{
   display: flex;
   justify-content: space-between;
   padding: 8px;
   p{
     font-size: 20px;
     font-weight: 900;
   }
  }
}
.fang{
  height: 22px;
  line-height: 22px;
  text-align: center;
  padding: 0 5px;
  font-size: 12px;

}
.side{
  color: #BEBEBE;
margin-left: 8px;
}
h4{
  height: 30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #707070;
 margin: 8px;
 font-size: 14px;
}
.ti{
  font-size: 12px;
  background-color: #eee;
  padding: 5px;
}
.tip{
  color:#E88C89;background:#FCF1F1
}
</style>
