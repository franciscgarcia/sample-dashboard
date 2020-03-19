<template>
  <div>
    <div class="pa-4 blue-grey lighten-5">
      {{rewardsData.title}}
      <v-avatar size="20">
        <v-icon size="15">mdi-help-circle</v-icon>
      </v-avatar>
    </div>
    <v-divider></v-divider>
    <v-data-table
      v-model="rewardsData.selected"
      :headers="rewardsData.headers"
      :items="rewardsData.desserts"
      item-key="name"
      class="elevation-1"
    >
    </v-data-table>
  </div>
</template>

<script>
import rewardsData from '../store/rewardsData.json';

export default {
  data() {
    return {
      rewardsData,
    };
  },
  mounted() {
    // insert api here and consume response in data()
  },
};
</script>
