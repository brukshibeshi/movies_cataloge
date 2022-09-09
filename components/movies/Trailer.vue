<template>
  <v-card class="mx-auto my-12" max-width="374">
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="15"
        indeterminate
      ></v-progress-linear>
    </template>

    <v-img height="200" :src="trailer.img">
      <v-card-title class="text--white" v-text="trailer.index"></v-card-title
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
