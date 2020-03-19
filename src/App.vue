<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-btn
          text
        >
          <v-icon>mdi-menu</v-icon>
        </v-btn>
      </div>

      <v-spacer></v-spacer>
        <div style="position: fixed; top: 25%; left: 50%;">
          Kollab
        </div>
      <v-spacer></v-spacer>

        <v-avatar size="50">
          <v-icon size="40">mdi-account-circle</v-icon>
        </v-avatar>
        <v-select
          label="Kiko"
          style="max-width: 100px;"
        ></v-select>

      <v-divider
        class="mx-4"
        inset
        vertical
      ></v-divider>

      <v-badge
        bordered
        top
        color="orange accent-4"
        dot
        offset-x="10"
        offset-y="10"
      >
        <v-icon>
          mdi-bell
        </v-icon>
      </v-badge>

      <v-divider
        class="mx-4"
        inset
        vertical
      ></v-divider>

      <v-icon>
        mdi-comment-question-outline
      </v-icon>
    </v-app-bar>

    <v-content class="grey lighten-5">
      <Headers/>
      <!-- <HelloWorld/> -->
      <Charts/>

      <div>
        <v-row style="margin: 3%;" class="d-flex justify-space-around">
          <v-card>
            <BranchTable/>
          </v-card>

          <v-card>
            <RewardsTable/>
          </v-card>
        </v-row>
      </div>
    </v-content>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue';
import Headers from './components/Headers.vue';
import Charts from './components/Charts.vue';
import BranchTable from './components/BranchTable.vue';
import RewardsTable from './components/RewardsTable.vue';

export default {
  name: 'App',

  components: {
    // HelloWorld,
    Headers,
    Charts,
    BranchTable,
    RewardsTable,
  },

  data: () => ({
    //
  }),
};
</script>
