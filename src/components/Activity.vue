<template>
  <v-container>
    <div>hello activity</div>
    <div>
      <v-carousel v-if="instaData" hide-delimiters>
        <v-carousel-item
          v-for="(item,i) in instaData"
          :key="i"
          :src="item.images.standard_resolution.url"
        >
        <div>Hello World</div>
        </v-carousel-item>
  </v-carousel>
    </div>
  </v-container>
</template>

<script>
import axios from 'axios';

export default {
  name: "activity",
  data: () => ({
    instaData: null,
    url : 'https://api.instagram.com/v1/users/self/media/recent/?access_token=4139325652.fee72d9.879771c4fcac4b5d8efbd2d8c4579a6c&count=25#'
  }),
  mounted() {
    axios.get(this.url).then(data => {
      this.instaData = data.data.data.slice(6, 20);
    })
    }
};
</script>
