<template>
<div>
  <h1>My Todo</h1>
  <input v-model = "newTodo" placeholder = "Input here..">
  <button v-on:click = "addTodo()">ADD</button>
  </div>
</template>

<script>
export default {
  data () {
    return{
      newTodo:""
    }
  },
  methods:{
    addTodo () {
      if(this.newTodo === "") return
      this.$emit('add',this.newTodo)
      this.newTodo = ""
    }
  }
}
</script>