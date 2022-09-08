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
