<template>
 <div class="wrapper">
 <h1>погодное приложение</h1>
 <p>Узнать погоду в {{ city == "" ? "в вашем городе" : city }} </p>
 <input type="text" v-model="city" placeholder="Введите город">
 <button v-if="city != ''">получить погоду</button>
 <button disabled v-else="city != ''">Введите название города</button>

</div>
</template>



<script>
export default{
  data(){
    return {
      city: ""
    }
  }
}
</script>



<style scoped>

.wrapper {
  width: 900px;
  height: 500px;
  border-radius: 50px;
  background: #2c2c2c;
  padding: 20px;
  text-align: center;
  color: rgb(255, 255, 255);

}
.wrapper h1 {
  margin-top: 50px;
}
.wrapper input{
  margin-top: 30px;
  background: transparent;
  border: 0;
  border-bottom:2px solid #000000;
  color: white;
  font-size: 14px;
  padding: 5px 8px;
  outline: none
}
.wrapper input:focus{
  border-bottom-color: #ffffff;
}
.wrapper button{
  background: #2c2c00;
  color:rgb(255, 255, 255);
  border-radius: 10px;
  padding:10px, 15px;
  border: 2px solid #ffcc00;
  margin-left: 20px;
  cursor: pointer;
  transition: transform 500ms ease;
}
.wrapper button:hover {
  transform:scale(1.1) translateY(-5px)
}

.wrapper button:disabled {
  background: #746027;
  cursor: no;
}
</style>
