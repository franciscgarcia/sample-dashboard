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

        <v-avatar size="40">
          <v-icon>mdi-account-circle</v-icon>
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

    <v-content>
      <Headers/>
      <HelloWorld/>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Headers from './components/Headers.vue';

export default {
  name: 'App',

  components: {
    HelloWorld,
    Headers,
  },

  data: () => ({
    //
  }),
};
</script>
