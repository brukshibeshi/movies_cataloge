<template>
<v-app dark>
  <div>
    <navbar />
    <v-main>
      <nuxt />
    </v-main>
  </div>
  </v-app>
</template>

<script>
import navbar from "@/components/Navbar";
export default {
  components: {
    navbar,
  },
};
</script>
<style scoped>
body {
  background: #1e1e1e !important;
}
</style>