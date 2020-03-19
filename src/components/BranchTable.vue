<template>
  <div>
    <div class="pa-4 blue-grey lighten-5">
      {{branchData.title}}
      <v-avatar size="20">
        <v-icon size="15">mdi-help-circle</v-icon>
      </v-avatar>
    </div>
    <v-divider></v-divider>
    <v-data-table
      v-model="branchData.selected"
      :headers="branchData.headers"
      :items="branchData.desserts"
      item-key="name"
      class="elevation-1"
    >
    </v-data-table>
  </div>
</template>

<script>
import branchData from '../store/branchData.json';

export default {
  data() {
    return {
      branchData,
    };
  },
  mounted() {
    // insert api here and consume response in data()
  },
};
</script>
