<template >
  <div>
    <img src="@/assets/logo.png" alt="Logo vue" border-radius="30px">
    <br>
    <br>
    <button @click="comentar">Comentar</button>
    <p>
      {{ comentario }}
    </p>
    <p>{{ detalhes }}</p>
  </div>
</template>
<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";

import { Prop } from "vue-property-decorator";

@Component
export default class Comentarista extends Vue {
  
 
  private comentario = ""
  @Prop () private nome !:string 

  private comentar(): void {
    this.comentario = "Um mega comentário bem bacana!";
  }
  get detalhes () {
    return `Nome do comentarista: ${this.nome}`;
  }
}
</script>

<style>
body{
 
  margin: 50px;
  background-color:#42b983;
}
p{
  font-size: 16px;
}
button{
  padding: 16px;
  border-radius: 12px;
  font-size: 16px;

}
button {
  transition-duration: 0.4s;
}

button:hover {
  background-color: #b11105; /* Green */
  color: white;
}
</style>