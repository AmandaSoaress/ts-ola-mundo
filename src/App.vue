<template>
  <div id="app">
    <Comentarista nome="Amanda Soares"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Comentarista from './components/Comentarista.vue';

@Component({
  components: {
    Comentarista,
  },
})
export default class App extends Vue {}

</script>
