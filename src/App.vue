<!-- <script>
import axios from "axios";
export default {
  name: "App",
  data() {
    return {};
  },
  created() {
    this.getProjects();
  },

  methods: {
    getProjects() {
      axios.get("http://127.0.0.1:8000/api/projects").then((resp) => {
        this.projects = resp.data.results;
      });
    },
  },
};
</script>

<template>
  <div class="container bd-light mt-3">
    <h2>Ritorno al Vue!!</h2>
  </div>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style> -->

<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  name: "App",
  components: {
    AppHeader,
  },
};
</script>
<template>
  <AppHeader />

  <router-view> </router-view>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
