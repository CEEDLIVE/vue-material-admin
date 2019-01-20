<template>
  <div id="pageDashboard">
    <v-container grid-list-xl fluid>
      <v-layout row wrap>Business</v-layout>
    </v-container>
  </div>
</template>

<script>
import API from '@/api';

export default {
  components: {

  },
  data: () => ({

  }),
  computed: {
    activity() {
      return API.getActivity();
    },
    posts() {
      return API.getPost(3);
    },
    siteTrafficData() {
      return API.getMonthVisit;
    },
    locationData() {
      return API.getLocation;
    }
  },

};
</script>
