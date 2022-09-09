<template>
  <div>
    <navbar />
    <v-main>
      <nuxt />
    </v-main>
  </div>
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
.v-application {
  background-color: #00a86b;
}
.theme--dark.v-application {
  background-color: var(--v-background-base, #121212) !important;
}
.theme--light.v-application {
  background-color: var(--v-background-base, white) !important;
}
</style>