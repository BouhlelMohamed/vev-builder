<template>
  <button @click="addElement">Ajouter une div </button>
  <component v-for="(item,index) in items" :key="index" :is="item.type" ></component>
</template>

<script>
import Div from './Elements/Div.vue';

export default {
  name: "Builder",
  components: {Div},
  data(){
    return {
      items: []
    }
  },
  methods: {
    addElement(){
      this.items.push({ type: Div })
    }
  }
}
</script>
