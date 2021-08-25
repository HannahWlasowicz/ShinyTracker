<template>
    <div>
        <input v-model="searh" @change="searchPokemon" type="text" placeholder="Search..">
    </div>
</template>

<script>


export default {
    name: 'Settings',
    data() {
    return {
      search: ''
    }
  },
  methods: {
      searchPokemon(){
        //   Search api for pokemon
        console.log("Sup")
      }
  }
}
</script>
