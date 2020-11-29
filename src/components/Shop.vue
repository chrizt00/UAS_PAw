<template>
  <div>
    <v-container>
      <div class="row">
        <div
         class="col-md-3 col-sm-3 col-xs-12"
        >
          <v-card outlined>
            <v-card-title>Filters</v-card-title>
            <v-divider></v-divider>
            <template>
              <v-treeview :items="items" :open="[1]" :active="[5]" :selected-color="'#fff'" activatable open-on-click dense></v-treeview>
            </template>
            <v-divider></v-divider>
            <v-card-title>Price</v-card-title>
            <v-row class="pa-2" dense>
              <v-col cols="12" sm="5">
                <v-text-field
                  :value="range[0]"
                  label="Min"
                  outlined
                  dense
                  @change="$set(range, 0, $event)"
                ></v-text-field>
              </v-col>
              <v-col cols="12" sm="2">
                <p class="pt-2 text-center">TO</p>
              </v-col>
              <v-col cols="12" sm="5">
                <v-text-field
                  :value="range[1]"
                  label="Max"
                  outlined
                  dense
                  @change="$set(range, 1, $event)"
                ></v-text-field>
              </v-col>
            </v-row>
            <v-divider></v-divider>
            <v-divider></v-divider>

          </v-card>
        </div>
        <div
          class="col-md-9 col-sm-9 col-xs-12"
        >

          <v-breadcrumbs class="pb-0" :items="breadcrums"></v-breadcrumbs>

          <v-divider></v-divider>

          <div class="row text-center">
            <div class="col-md-3 col-sm-6 col-xs-12" :key="pro.id" v-for="pro in products">
              <v-hover v-slot:default="{ hover }">
                <v-card
                  class="mx-auto"
                  color="grey lighten-4"
                  max-width="600"
                >
                  <v-img
                    class="white--text align-end"
                    :aspect-ratio="16/9"
                    height="200px"
                    :src="pro.src"
                  >
                    <v-card-title>{{pro.type}} </v-card-title>
                    <v-expand-transition>
                      <div
                        v-if="hover"
                        class="d-flex transition-fast-in-fast-out white darken-2 v-card--reveal display-3 white--text"
                        style="height: 100%;"
                      >
                        <v-btn v-if="hover" href="/product" class="" outlined>VIEW</v-btn>
                      </div>

                    </v-expand-transition>
                  </v-img>
                  <v-card-text class="text--primary">
                    <div><a href="/product" style="text-decoration: none">{{pro.name}}</a></div>
                    <div>Rp.{{pro.price}}</div>
                  </v-card-text>
                </v-card>
              </v-hover>
            </div>
          </div>
          <div class="text-center mt-12">
            <v-pagination
              v-model="page"
              :length="6"
            ></v-pagination>
          </div>
        </div>
      </div>
    </v-container>
  </div>
</template>
<style>
  .v-card--reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: .8;
    position: absolute;
    width: 100%;
  }
</style>
<script>
    export default {
        data: () => ({
            range: [0, 10000],
            select:'Popularity',
            options: [
                'Default',
                'Popularity',
                'Relevance',
                'Price: Low to High',
                'Price: High to Low',
            ],
            page:1,
            breadcrums: [
            ],
            min:0,
            max:10000,
            items: [
                {
                    id: 2,
                    name: 'Color',
                    children: [
                        { id: 2, name: 'Red' },
                        { id: 3, name: 'Blue' },
                        { id: 4, name: 'Yellow' },
                        { id: 5, name: 'Green' },
                        { id: 6, name: 'Black' },
                        { id: 7, name: 'Others' },
                    ],
                },
            ],
            products:[
                {
                    id:1,
                    name:'',
                    price:'253.000',
                    src:require('../assets/img/Bag/1.png')
                },
                {
                    id:2,
                    name:'',
                    price:'500.000',
                    src:require('../assets/img/Bag/2.png')
                },
                {
                    id:3,
                    name:'',
                    price:'300.000',
                    src:require('../assets/img/Bag/3.png')
                },
                {
                    id:4,
                    name:'',
                    price:'250.000',
                    src:require('../assets/img/Bag/4.png')
                },
                {
                    id:5,
                    name:'',
                    price:'330.000',
                    src:require('../assets/img/Bag/5.png')
                },
                {
                    id:6,
                    name:'',
                    price:'220.000',
                    src:require('../assets/img/Bag/6.png')
                },
                {
                    id:7,
                    name:'',
                    price:'310.000',
                    src:require('../assets/img/Bag/7.png')
                },
                {
                    id:8,
                    name:'',
                    price:'400.000',
                    src:require('../assets/img/Bag/8.png')
                },{
                    id:9,
                    name:'',
                    price:'410.000',
                    src:require('../assets/img/Bag/9.png')
                },
                {
                    id:10,
                    name:'',
                    price:'450.000',
                    src:require('../assets/img/Bag/10.png')
                },
                {
                    id:11,
                    name:'',
                    price:'535.000',
                    src:require('../assets/img/Bag/11.png')
                },
                {
                    id:12,
                    name:'',
                    price:'280.000',
                    src:require('../assets/img/Bag/12.png')
                }
            ]
        }),
    }
</script>
