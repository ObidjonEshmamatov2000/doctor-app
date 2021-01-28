<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col cols="12">
          <v-card :loading="loading" class="mx-auto my-12" max-width="374">
            <template slot="progress">
              <v-progress-linear
                color="pink darken-3"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-img
              height="250"
              src="../assets/img/doctor5.jpg"
              align-end
            ></v-img>
            <v-card-title>Dr. Muslima Shamsiddinova</v-card-title>

            <v-card-text>
              <v-row
                align="center"
                class="mx-0"
              >
                <v-rating
                  :value="4.5"
                  color="pink darken-4"
                  dense
                  half-increments
                  readonly
                  size="14"
                ></v-rating>

                <div class="grey--text ml-4">4.5</div>
              </v-row>
              <div class="my-4  text-h6 black--text">Pediatrician</div>
              <div class="">1111 Ahmad Donish street, Tashkent</div>
            </v-card-text>
            <v-divider class="mx-4"></v-divider>
            <v-card-title>Today's availability</v-card-title>
            <v-card-text>
              <v-chip-group
                v-model="selection"
                active-class="pink darken-4 white--text"
                column
              >
                <v-chip>7:30AM</v-chip>
                <v-chip>8:30AM</v-chip>
                <v-chip>9:00AM</v-chip>
                <v-chip>11:30AM</v-chip>
              </v-chip-group>
            </v-card-text>

            <v-card-actions>
              <v-btn
                color="pink darken-4"
                text
                @click="reserve"
              >
                Book appointment
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>

export default {
  name: 'Home',
  components: {
    
  },
  data() {
    return {
      loading: false,
      selection: 1
    }
  },
  methods: {
    reserve() {
      this.loading = true;

      setTimeout(() => (this.loading = false), 2000);
    }
  }
}
</script>
