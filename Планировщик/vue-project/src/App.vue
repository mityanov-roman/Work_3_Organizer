<script>
export default{
  data(){
    return{
      name: "",
      list: [],
    }
  },
  methods:{
    sayHello(){
      this.list.push(this.name);
      console.log(this.list);
    }
  }
}
</script>

<template>
<div class ="content">
  <h1>Список покупок </h1>
<p>Тут можно создать список покупок</p>
<hr>

<input type="text" v-model="name"> <br>
<button v-if="name==''" disabled>введи данные</button>
  <button v-else @click="sayHello()">Добавить в список</button>
<ul>
  <li v-for="item in list">
  {{ 
    item
  }}</li>
</ul>
</div>
</template>

<style scoped>
.content{
  width: 800px;
  height: 80vh;
  background-color: #fff;
  border-radius: 20px;
  text-align: center;
  margin-top: 50px;
}
.content h1{
  text-transform: appercase;
  padding-top: 30px;
  padding-bottom: 30px;
  font-size: 40px;
}
.content p{
  padding-bottom: 20px;
}
.content input{
  width: 80%;
  font-size: 24px;
  margin-top: 30px;
  border: 0;
  border-bottom: 2px solid gray;
  padding: 2px;
}
.content button{
  width: 300px;
  margin-top: 30px;
  font-size: 24px;
  text-transform: uppercase;
  border: 0;
}
</style>
