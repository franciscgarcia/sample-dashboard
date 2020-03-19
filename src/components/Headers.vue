<template>
  <v-container fluid>
    <div class="d-flex align-center">
      <v-avatar size="50">
        <v-icon size="30">mdi-chart-pie</v-icon>
      </v-avatar>

      <span class="title">Analytics</span>

      <v-avatar size="20">
        <v-icon size="15">mdi-help-circle</v-icon>
      </v-avatar>
    </div>

    <v-row>
      <v-col cols="12">
        <v-row
          align="center"
          justify="space-between"
          class="grey lighten-5"
          style="height: 250px;"
        >
          <v-card
            v-for="n in 4"
            :key="n"
            class="highlight margin-lr-20"
            outlined
            min-height="160"
            min-width="200"
            max-width="300"
            tile
          >
            <v-list-item three-line>
              <v-list-item-content>
                <div class="d-flex align-center">
                  Title
                  <v-avatar size="20">
                    <v-icon size="15">mdi-help-circle</v-icon>
                  </v-avatar>
                </div>

                <v-list-item-title class="headline mb-1">Headline 5</v-list-item-title>

                <v-list-item-subtitle>
                  Greyhound divisely hello coldly fonwderfully
                </v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>

            <v-spacer></v-spacer>

            <v-divider></v-divider>

            <v-card-actions>
              <span> Label </span>

              <v-spacer></v-spacer>

              <span> Value </span>
            </v-card-actions>
          </v-card>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'HelloWorld',

  data: () => ({
    ecosystem: [
      {
        text: 'vuetify-loader',
        href: 'https://github.com/vuetifyjs/vuetify-loader',
      },
    ],
    importantLinks: [
      {
        text: 'Documentation',
        href: 'https://vuetifyjs.com',
      },
      {
        text: 'Chat',
        href: 'https://community.vuetifyjs.com',
      },
      {
        text: 'Made with Vuetify',
        href: 'https://madewithvuejs.com/vuetify',
      },
      {
        text: 'Twitter',
        href: 'https://twitter.com/vuetifyjs',
      },
      {
        text: 'Articles',
        href: 'https://medium.com/vuetify',
      },
    ],
    whatsNext: [
      {
        text: 'Explore components',
        href: 'https://vuetifyjs.com/components/api-explorer',
      },
      {
        text: 'Select a layout',
        href: 'https://vuetifyjs.com/layout/pre-defined',
      },
      {
        text: 'Frequently Asked Questions',
        href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
      },
    ],
  }),
};
</script>

<style scoped>
  .highlight:active {
    box-shadow: .5px .5px 3px 3px rgb(147, 174, 224);
  }

  .margin-lr-20 {
    margin: 0 20px;
  }
</style>
