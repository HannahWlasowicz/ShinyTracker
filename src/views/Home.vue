<template>
  <div>
    <b-tabs content-class="mt-3">
      <b-tab title="Tracker" active><Tracker/></b-tab>
      <b-tab title="Settings"><Settings/></b-tab>
    </b-tabs>
  </div>
</template>

<script>
// @ is an alias to /src
import Tracker from '../components/Tracker.vue'
import Settings from '../components/Settings.vue'

export default {
  name: "Home",
  components: {
    Tracker,
    Settings
  },
};
</script>
