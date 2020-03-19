<template>
  <div class="small">
    <v-card style="padding: 0 30px;">
      <div>
        <v-row class="d-flex align-center">
          <span>Sales Overview</span>
          <v-avatar size="20">
            <v-icon size="15">mdi-help-circle</v-icon>
          </v-avatar>

          <v-spacer></v-spacer>

          <div style="padding-top: 1%">
            <v-row>
              <v-select
                items="items"
                label="All Transactions"
                solo
              ></v-select>

              <v-select
                items="items"
                label="All Branches"
                solo
              ></v-select>
            </v-row>
          </div>
        </v-row>
      </div>

      <line-chart :chartData="datacollection" :styles="myStyles"
      :options="datacollection.options"></line-chart>
    </v-card>
  </div>
</template>

<script>
import LineChart from '../store/LineChart';

export default {
  components: {
    LineChart,
  },
  data() {
    return {
      datacollection: null,
    };
  },
  mounted() {
    this.fillData();
  },
  computed: {
    myStyles() {
      return {
        height: '400px',
        position: 'relative',
      };
    },
  },
  methods: {
    fillData() {
      this.datacollection = {
        labels: [this.getRandomInt(), this.getRandomInt(), this.getRandomInt(),
          this.getRandomInt(), this.getRandomInt(), this.getRandomInt(), this.getRandomInt()],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: 'rgb(84, 86, 199)',
            data: [this.getRandomInt(), this.getRandomInt(), this.getRandomInt(),
              this.getRandomInt(), this.getRandomInt(), this.getRandomInt(), this.getRandomInt()],
          },
          {
            label: 'Data Two',
            backgroundColor: '#46C1A4',
            data: [this.getRandomInt(), this.getRandomInt(), this.getRandomInt(),
              this.getRandomInt(), this.getRandomInt(), this.getRandomInt(), this.getRandomInt()],
          },
        ],
        options: {
          scales: {
            yAxes: [
              {
                ticks: {
                  beginAtZero: true,
                },
              }],
          },
          responsive: true,
          maintainAspectRatio: false,
        },
      };
    },
    getRandomInt() {
      return Math.floor(Math.random() * (50 - 5 + 1)) + 5;
    },
  },
};
</script>

<style>
  .small {
    max-width: 90%;
    max-height: 500px;
    margin:  5px auto;
  }
</style>
