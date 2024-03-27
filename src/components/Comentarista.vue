<template>
  <div>
    <button @click="comentar">Comentar</button>
    <p>
      {{ comentario }}
    </p>
  </div>
</template>
<script  lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'

@Component
export default class Comentarista extends Vue {

    private comentario = ''
    private comentar () : void{
       this.comentario = 'Um mega comentário bem bacana!' 
    } 
}
</script>
