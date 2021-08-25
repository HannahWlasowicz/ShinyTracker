<template >
  <div class="hello">
    <p>{{ count }}</p>
    <input type="submit" value="+" @click="increase">
    <input type="submit" value="-" @click="decrease">
    <input type="submit" value="Reset" @click="reset">
  </div>
</template>

<script>
export default {
  name: 'Tracker',
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increase() {
      this.count = this.count +1;
    },
    decrease() {
      if(this.count > 0){
        this.count = this.count - 1;
      }
    },
    reset() {
      this.count = 0;
    }
  },
  created() {
    window.addEventListener("keyup", e => {
      const key = e.key;
      if(key == "+"){
        this.increase()
      } else if (key == "-") {
        this.decrease()
      } else if (key == "Delete") {
        this.reset()
      }
      console.log(e.key)
    });
  },
  unmounted() {
    window.removeEventListener('keyup', () => {});
  },
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
