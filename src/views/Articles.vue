<template>
  <v-app style="background: rgb(8, 8, 11);">
    <div>
        <BottomNav />
    </div>
  </v-app>
</template>

<script>
import BottomNav from "../components/BottomNav";

export default {
  name: 'Home',
  components: {
    BottomNav
  },
  data: () => ({
    sheet: false,
    insta_access_token: '4139325652.fee72d9.879771c4fcac4b5d8efbd2d8c4579a6c'
  }),
};
</script>

