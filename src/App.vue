<template>
  <v-app>
    <router-view />
  </v-app>
</template>

<script>
import Home from './components/Home';

export default {
  name: 'App',
  components: {
    Home
  },
  data: () => ({
    sheet: false,
    insta_access_token: '4139325652.fee72d9.879771c4fcac4b5d8efbd2d8c4579a6c'
  }),
};
</script>

<style scoped>
  /* .footer {
    position: fixed;
    bottom: 0;
    display: block;
    width: 100%;
    background: #fff;
    padding: 10px 0 50px 0;
    border-top-left-radius: 20px;
    border-top-right-radius: 20px;
  }
  .v-btn:not(.v-btn--round).v-size--default {
    border-radius: 50%  ;
    padding: 10px;
    min-height: 50px;
    min-width: 50px;
  } */
</style>
