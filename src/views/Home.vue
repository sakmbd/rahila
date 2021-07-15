<template>
  <div>
    <home-component />
    <div class="text-center">
      <v-dialog
        v-model="dialog"
        persistent
        width="500"
      >
        <v-card>
          <v-card-title class="text-h6 white--text pink">
            Select Rahila's birthday?
          </v-card-title>
          <v-spacer/>

          <v-card-text>
            <v-select
              :items="days"
              label="Day"
              v-model="day"
            >
              <template v-slot:item="{ item, attrs, on }">
                <v-list-item
                  v-bind="attrs"
                  v-on="on"
                >
                  <v-list-item-title
                    :id="attrs['aria-labelledby']"
                    v-text="item"
                  ></v-list-item-title>
                </v-list-item>
              </template>
            </v-select>

            <v-select
              :items="months"
              label="Month"
              v-model="month"
            >
              <template v-slot:item="{ item, attrs, on }">
                <v-list-item
                  v-bind="attrs"
                  v-on="on"
                >
                  <v-list-item-title
                    :id="attrs['aria-labelledby']"
                    v-text="item"
                  ></v-list-item-title>
                </v-list-item>
              </template>
            </v-select>

            <v-alert type="error" v-if="errorFlag">
              Wrong answer!
            </v-alert>
          </v-card-text>

          <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="red lighten-2"
            dark
            @click="checkDOB"
          >
            Submit
          </v-btn>
        </v-card-actions>
        </v-card>
      </v-dialog>
    </div>
  </div>
</template>

<script>
import HomeComponent from '../components/HomeComponent'

export default {
  name: 'Home',
  components: {
    HomeComponent
  },
  data () {
    return {
      errorFlag: false,
      dialog: true,
      month: '',
      day: '',
      months: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
      days: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31]
    }
  },
  created () {
    this.checkAlreadyAnswered()
  },
  methods: {
    checkDOB () {
      if (this.day === 20 && this.month === 'July') {
        this.dialog = false
        localStorage.setItem('isAnswered', true)
        this.$toasted.success('<div class=toastParent><p class=toastM1>Bingoo!!</p> <p class=toastM2>You give the correct answer now you can see all stuff related to Rahila Rehman.</p></div>', {
          theme: 'bubble',
          position: 'top-right',
          className: 'Toaster--Success',
          duration: 7000
        })
      } else {
        this.errorFlag = true
        localStorage.setItem('isAnswered', false)
      }
    },
    checkAlreadyAnswered () {
      const isAnswered = localStorage.getItem('isAnswered')
      if (isAnswered === 'true') {
        this.dialog = false
      }
    }
  }
}
</script>

<style>
.Toaster--Success {
  height: 125px !important;
}
.toastM1 {
  line-height: 1;
  font-size: 24px;
  font-weight: bold;
}
.toastM2 {
  line-height: 1.6;
  margin-top: 11px;
}
</style>
