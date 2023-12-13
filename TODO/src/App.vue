<script setup>
import { ref } from 'vue';
let codigos =ref ([[],[],[]]);
let refcode= ref('')
let indice = ref(0)

function pusharray(indice){
  if(indice==1){
    codigos.value[indice-1].push(refcode.value)
  console.log(indice)  }
  if(indice==2){
    codigos.value[indice-1].push(refcode.value)
  console.log(indice)  }
  if(indice==3){
    codigos.value[indice-1].push(refcode.value)
  console.log(indice)  }
  
}




</script>

<template>
  <section class="max-w-[1000px] my-2 mx-auto ">
<div class="bg-slate-700 justify-center flex">
  <h1>SISTEMA DE TURNOS</h1>
</div>
<div>
<div class="flex justify-between">
  <div class="bg-blue-500"> <h1 class="text-white"> MODULO 1</h1>
  <div class="bg-slate-700 w-">
    <div v-for="(obj,index) in codigos[0]" :key="index" >{{ index+1 }} {{ obj }}</div>
  </div>
  
  </div>
  <div class="bg-orange-500"> <h1 class="text-white"> MODULO 2</h1>
    <div class="bg-slate-700 w-">
    <div v-for="(obj,index) in codigos[1]" :key="index" > {{ obj }}</div>
  </div></div>
  <div class="bg-green-500"> <h1 class="text-white"> MODULO 3</h1>
    <div class="bg-slate-700 w-">
    <div v-for="(obj,index) in codigos[2]" :key="index" > {{ obj }}</div>
  </div></div>
</div>




</div>

  <div class="flex">
    <div><h1>{{ (codigos[0].length + codigos[1].length + codigos[2].length)  }}</h1></div>
    <div><input type="text" placeholder="codigo" v-model="refcode"></div>
    <div>
   <input type="number" v-model="indice">

    </div>
    <div>
      <button @click="pusharray(indice)">agregar</button>
    </div>

  </div>









  </section>
</template>


