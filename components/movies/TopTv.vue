<template>
  <v-card class="mx-auto" width="200px !importanrt;">
    <v-img :src="tvsh.src" height="500px"></v-img>
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
