<template>
  <div>
    <carousel/>
    <v-container
      v-for="align in alignments"
      :key="align"
      class="grey lighten-5 mb-6"
    >
      <v-row
        :align="align"
        no-gutters
        style="height: 150px;"
      >
        <v-col
          v-for="n in 5"
          :key="n"
        >
          <v-card
            class="pa-2"
            outlined
            tile
          > 
           <v-switch v-model="closeOnContentClick" label="Close on content click"></v-switch>
            <v-menu top :close-on-content-click="closeOnContentClick">
            <template v-slot:activator="{ on, attrs }">
            <v-btn
             color="primary"
             dark
             v-bind="attrs"
             v-on="on"
            >
             Dropdown
            </v-btn>
            </template>

            <v-list>
            <v-list-item
            v-for="(item, index) in items"
            :key="index"
            @click=""
            >
            <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
            </v-list>
            </v-menu>
            
          </v-card>
        </v-col>
      </v-row>
    </v-container>

    
  </div>
</template>

<script>
  export default {
    data: () => ({
      alignments: [
        
        'center',
       
      ],

      
      items: [
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me 2' },
      ],
      closeOnContentClick: true,
   
    }),
  }
</script>