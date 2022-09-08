<template>
  <v-card class="mx-auto" width="200px !importanrt;">
    <v-img :src="movie.src" height="450px" width="210px !importanrt;"></v-img>
  </v-card>
</template>
<script>
export default {
  props: {
    movie: {
      type: Object,
      required: true,
    },
  },
  data: () => ({}),
};
</script>
