<template>
  <div class="hello">
    <p>{{ count }}</p>
    <button v-on:click="increase">+</button>
    <button v-on:click="decrease">-</button>
    <button v-on:click="reset">Reset</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increase: function() {
      this.count = this.count +1;
    },
    decrease: function() {
      if(this.count > 0){
        this.count = this.count - 1;
      }
    },
    reset: function () {
      this.count = 0;
    }
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #0e26af;
}
</style>
