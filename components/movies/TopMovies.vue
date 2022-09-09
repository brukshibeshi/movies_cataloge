<template>
  <v-card class="mx-auto" width="200px !importanrt;">
  <v-img :src="topMovie.src" height="500px" width="300px;"></v-img>
  </v-card>
</template>
<script>
export default {
  props: {
    topMovie: {
      type: Object,
      required: true,
    },
  },
  data: () => ({}),

  methods: {},
};
</script>
