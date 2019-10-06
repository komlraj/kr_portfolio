<template>
  <v-app style="background: rgb(8, 8, 11);">
    <div>
            <router-link to="/activity">Activity</router-link>
          </div>

    <div class="text-center footer">
    <v-bottom-sheet v-model="sheet">
      <template v-slot:activator="{ on }">
        <v-btn
          v-on="on"
        >
          Explore Me
        </v-btn>
      </template>
      <v-sheet class="text-center" height="500px">
        <v-btn
          class="foot-close-btn"
          @click="sheet = !sheet"
        >X</v-btn>
        <div>
          
          <form>
            <div>
              <div>Tell us about you</div>
              <div>
                <v-container>
                  <v-text-field label="Name"></v-text-field>
                  <v-text-field label="Email"></v-text-field>
                </v-container>
              </div>
            </div>
            <div>
              <div>Tell us about your idea</div>
              <div>
                <v-text-field label="give us a short description"></v-text-field>
              </div>
            </div>
          </form>
        </div>
      </v-sheet>
    </v-bottom-sheet>
  </div>
  </v-app>
</template>

<script>
import Activity from './Activity.vue';

export default {
  name: 'Home',
  components: {
    Activity
  },
  data: () => ({
    sheet: false,
    insta_access_token: '4139325652.fee72d9.879771c4fcac4b5d8efbd2d8c4579a6c'
  }),
};
</script>

<style scoped>
  .footer {
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
  }
</style>
