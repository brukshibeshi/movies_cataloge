<template>
  <v-card class="mx-auto" max-width="344">
    <v-img :src="topMovie.src" height="450px"></v-img>
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
