<template>
      <v-card>
        <v-card-title>
          <span class="headline"></span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col cols="12" md="3">
                <v-menu
                  v-model="menu2"
                  :close-on-content-click="false"
                  transition="scale-transition"
                  offset-y
                  max-width="290px"
                  min-width="290px"
                >
                  <template v-slot:activator="{ on, attrs }">
                    <v-text-field
                      v-model="computedDateFormatted"
                      label="Date"
                      
                      readonly
                      v-bind="attrs"
                      v-on="on"
                    ></v-text-field>
                  </template>
                  <v-date-picker v-model="date" no-title @input="menu2 = false"></v-date-picker>
                </v-menu>
                
              </v-col>

              <v-col cols="12" md="3">
                <v-autocomplete
                  :items="['Events', 'Pilgrims', 'Holidays', 'Business', 'Others']"
                  label="Services"
                  multiple
                ></v-autocomplete>
              </v-col>
              <v-col cols="12" md="3">
                <v-autocomplete
                  :items="['Agra', 'Delhi', 'Mumbai', 'Tirupati', 'Jalgaon', 'Tiruvantampuram', 'Ratnagiri', 'Thane', 'Banglore']"
                  label="Destinations"
                ></v-autocomplete>
              </v-col>
              <v-col cols="12" md="3">
                <v-autocomplete
                  :items="['Agra', 'Delhi', 'Mumbai', 'Tirupati', 'Jalgaon', 'Tiruvantampuram', 'Ratnagiri', 'Thane', 'Banglore']"
                  label="Destinations"
                ></v-autocomplete>
              </v-col>
            </v-row>
          </v-container>
          
        </v-card-text>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
  export default {
    data: vm => ({
      date: new Date().toISOString().substr(0, 10),
      dateFormatted: vm.formatDate(new Date().toISOString().substr(0, 10)),
      menu1: false,
      menu2: false,
    }),

    computed: {
      computedDateFormatted () {
        return this.formatDate(this.date)
      },
    },

    watch: {
      date (val) {
        this.dateFormatted = this.formatDate(this.date)
      },
    },

    methods: {
      formatDate (date) {
        if (!date) return null

        const [year, month, day] = date.split('-')
        return `${month}/${day}/${year}`
      },
      parseDate (date) {
        if (!date) return null

        const [month, day, year] = date.split('/')
        return `${year}-${month.padStart(2, '0')}-${day.padStart(2, '0')}`
      },
    },
  }
</script>