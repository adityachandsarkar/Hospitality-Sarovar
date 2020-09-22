 <template>
<v-container>
 <v-row>
    <v-col cols="12" md="12">
          <v-menu
          ref="menu1"
          v-model="dateRangeText"
          :close-on-content-click="true"
          transition="scale-transition"
          offset-y
          max-width="290px"
          min-width="290px"
        >
            <template v-slot:activator="{ on, attrs }">
            <v-text-field
              v-model="dateRangeText"
              label="Checkin-CheckOut"
              hint="MM/DD/YYYY format"
              persistent-hint
              v-bind="attrs"
              v-on="on"
            ></v-text-field>
            </template>
          <!-- @blur="date = parseDate(dateFormatted)" -->
      <!-- <v-text-field v-model="dateRangeText" label="Date range"></v-text-field> -->
      <v-date-picker v-model="dates" range></v-date-picker>
    
  </v-menu>
  </v-col>
  </v-row>
</v-container>
</template>

<script>
  export default {
    data: vm => ({
      dates: ['2019-09-10', '2019-09-20'],
      // menu1: false
    }),
    computed: {
      dateRangeText () {
        return this.dates.join(' ~ ')
      },
    },
  }
</script>