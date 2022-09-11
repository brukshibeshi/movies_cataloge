<template>
  <v-card class="mx-auto" width="200px !importanrt;">
    <v-img
      :src="movie.src"
      :lazy-src="movie.src"
      height="500px"
      width="210px !importanrt;"
    >
      <template v-slot:placeholder>
        <v-row class="fill-height ma-10" align="center" justify="center">
          <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
        </v-row> </template
    ></v-img>
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
