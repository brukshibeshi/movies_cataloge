<template>
  <v-card class="mx-auto my-10" max-width="400">
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="5"
        indeterminate
      ></v-progress-linear>
    </template>

    <v-img height="150" :src="trailer.img">
      <v-card-title class="text--white num" v-text="trailer.index"></v-card-title
    ></v-img>
  </v-card>
</template>

<script>
export default {
  props: {
    trailer: {
      type: Object,
      required: true,
    },
  },
  data: () => ({}),

  methods: {},
};
</script>

