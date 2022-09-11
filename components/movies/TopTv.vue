<template>
  <v-card class="mx-auto" width="200px !importanrt;">
    <v-img :lazy-src="tvsh.src" height="500px"
      ><template v-slot:placeholder>
        <v-row class="fill-height ma-0" align="center" justify="center">
          <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
        </v-row> </template
    ></v-img>
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
