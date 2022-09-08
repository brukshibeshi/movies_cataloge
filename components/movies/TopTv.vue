<template>
  <v-card class="mx-auto" max-width="344">
    <v-img :src="tvsh.src" height="400px"></v-img>
  </v-card>
</template>
<script>
export default {
  props: {
    tvsh: {
      type: Object,
      required: true,
    },
  },
  data: () => ({}),

  methods: {},
};
</script>
