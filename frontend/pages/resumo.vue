<template>
  <v-card
    class="mt-4 mx-auto"
    max-width="800"
  >
    <v-sheet
      class="v-sheet--offset mx-auto"
      color="#1abc9c"
      elevation="12"
      max-width="calc(100% - 32px)"
    >
      <v-sparkline
        :labels="labels"
        :value="value"
        color="white"
        line-width="2"
        padding="16"
      ></v-sparkline>
    </v-sheet>

    <v-card-text class="pt-0">
      <div class="title font-weight-light mb-2">User Registrations</div>
      <div class="subheading font-weight-light grey--text">Last Campaign Performance</div>
      <v-divider class="my-2"></v-divider>
      <v-icon
        class="mr-2"
        small
      >
        mdi-clock
      </v-icon>
    </v-card-text>

    <v-sheet
      class="v-sheet--offset mx-auto"
      color="#8e44ad"
      elevation="12"
      max-width="calc(100% - 32px)"
    >
      <v-sparkline
        :labels="labels"
        :value="value2"
        color="white"
        line-width="2"
        padding="16"
      ></v-sparkline>
    </v-sheet>

    <v-card-text class="pt-0">
      <div class="title font-weight-light mb-2">User Registrations</div>
      <div class="subheading font-weight-light grey--text">Last Campaign Performance</div>
      <v-divider class="my-2"></v-divider>
      <v-icon
        class="mr-2"
        small
      >
        mdi-clock
      </v-icon>
    </v-card-text>

    <v-sheet
      class="v-sheet--offset mx-auto"
      color="#e74c3c"
      elevation="12"
      max-width="calc(100% - 32px)"
    >
      <v-sparkline
        :labels="labels"
        :value="value3"
        color="white"
        line-width="2"
        padding="16"
      ></v-sparkline>
    </v-sheet>

    <v-card-text class="pt-0">
      <div class="title font-weight-light mb-2">User Registrations</div>
      <div class="subheading font-weight-light grey--text">Last Campaign Performance</div>
      <v-divider class="my-2"></v-divider>
      <v-icon
        class="mr-2"
        small
      >
        mdi-clock
      </v-icon>
    </v-card-text>

  </v-card>
</template>

<script>
  export default {
    data: () => ({
      labels: [
        '12am',
        '3am',
        '6am',
        '9am',
        '12pm',
        '3pm',
        '6pm',
        '9pm',
      ],
      value: [
        200,
        675,
        410,
        390,
        310,
        460,
        250,
        240,
      ],
      value2: [
        200,
        300,
        150,
        30,
        10,
        60,
        20,
        203,
      ],
      value3: [
        500,
        75,
        41,
        90,
        10,
        46,
        50,
        24,
      ],
    }),
  }
</script>

<style>
  .v-sheet--offset {
    top: -24px;
    position: relative;
  }
</style>