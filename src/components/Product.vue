<template>
  <div>
    <v-container>
      <div class="row">
        <div class="col-md-5 col-sm-5 col-xs-12">
          <v-img :src="require('../assets/img/home/slider4.jpg')"></v-img>
        </div>
        <div class="col-md-7 col-sm-7 col-xs-12">
          <div class="pl-6">
            <p class="display-1 mb-0">Modern White Bag</p>
            <v-card-actions class="pa-0">
              <p class="headline font-weight-light pt-3">Rp 350.000 <del style="" class="subtitle-1 font-weight-thin">Rp 500.000</del></p>
              <v-spacer></v-spacer>
            </v-card-actions>
            <p class="subtitle-1 font-weight-standard">
              Ukuran 40x50, warna putih susu, cocok untuk kamu yang selalu tampil simple tapi tetap elegan
            </p>
            <p class="title">ITEMS</p>

            <v-text-field
                outlined
                style="width:100px"
                :value="1"
                dense
            ></v-text-field>
            <v-btn class="primary white--text" outlined tile dense><v-icon>mdi-cart</v-icon> ADD TO CART</v-btn>

          </div>

        </div>
      </div>
      <div class="row">
        <div class="col-sm-12 col-xs-12 col-md-12">
          <v-card-text
            class="pa-0 pt-4"
            tile
            outlined
          >
            <p class="subtitle-1 font-weight-light pt-3 text-center">YOU MIGHT ALSO LIKE</p>
            <v-divider></v-divider>
            <div class="row text-center">
              <div class="col-md-2 col-sm-4 col-xs-12 text-center">
                <v-hover
                  v-slot:default="{ hover }"
                  open-delay="200"
                >
                  <v-card
                    :elevation="hover ? 16 : 2"
                  >
                    <v-img
                      class="white--text align-end"
                      height="200px"
                      :src="require('../assets/img/home/deal1.jpg')"
                    >
                    </v-img>

                    <v-card-text class="text--primary text-center">
                      <div>Upto 60% + Extra 10%</div>
                      <div>Baggit, Zara, Fossil</div>
                    </v-card-text>

                    <div class="text-center">
                      <v-btn
                        class="ma-2"
                        outlined
                        color="info"
                      >
                        Explore
                      </v-btn>
                    </div>
                  </v-card>
                </v-hover>
              </div>
              <div class="col-md-2 col-sm-4 col-xs-12 text-center" >
                <v-hover
                  v-slot:default="{ hover }"
                  open-delay="200"
                >
                  <v-card
                    :elevation="hover ? 16 : 2"
                  >
                    <v-img
                      class="white--text align-end"
                      height="200px"
                      :src="require('../assets/img/home/deal2.jpg')"
                    >
                    </v-img>

                    <v-card-text class="text--primary text-center">
                      <div>Upto 50%</div>
                      <div>Zara, Selected, Celio</div>
                    </v-card-text>

                    <div class="text-center">
                      <v-btn
                        class="ma-2"
                        outlined
                        color="info"
                      >
                        Explore
                      </v-btn>
                    </div>
                  </v-card>
                </v-hover>
              </div>
              <div class="col-md-2 col-sm-4 col-xs-12 text-center" >
                <v-hover
                  v-slot:default="{ hover }"
                  open-delay="200"
                >
                  <v-card
                    :elevation="hover ? 16 : 2"
                  >
                    <v-img
                      class="white--text align-end"
                      height="200px"
                      :src="require('../assets/img/home/deal3.jpg')"
                    >
                    </v-img>

                    <v-card-text class="text--primary text-center">
                      <div>Upto 60% + Extra 10%</div>
                      <div>Jack & Jones, Levis</div>
                    </v-card-text>

                    <div class="text-center">
                      <v-btn
                        class="ma-2"
                        outlined
                        color="info"
                      >
                        Explore
                      </v-btn>
                    </div>
                  </v-card>
                </v-hover>
              </div>
              <div class="col-md-2 col-sm-4 col-xs-12 text-center" >
                <v-hover
                  v-slot:default="{ hover }"
                  open-delay="200"
                >
                  <v-card
                    :elevation="hover ? 16 : 2"
                  >
                    <v-img
                      class="white--text align-end"
                      height="200px"
                      :src="require('../assets/img/shop/5.jpg')"
                    >
                    </v-img>

                    <v-card-text class="text--primary text-center">
                      <div>Upto 60% + Extra 10%</div>
                      <div>Nike, Adidas, Puma</div>
                    </v-card-text>

                    <div class="text-center">
                      <v-btn
                        class="ma-2"
                        outlined
                        color="info"
                      >
                        Explore
                      </v-btn>
                    </div>
                  </v-card>
                </v-hover>
              </div>
              <div class="col-md-2 col-sm-4 col-xs-12 text-center" >
                <v-hover
                  v-slot:default="{ hover }"
                  open-delay="200"
                >
                  <v-card
                    :elevation="hover ? 16 : 2"
                  >
                    <v-img
                      class="white--text align-end"
                      height="200px"
                      :src="require('../assets/img/home/deal4.jpg')"
                    >
                    </v-img>

                    <v-card-text class="text--primary text-center">
                      <div>Upto 60% + Extra 10%</div>
                      <div>Nike, Adidas, Puma</div>
                    </v-card-text>

                    <div class="text-center">
                      <v-btn
                        class="ma-2"
                        outlined
                        color="info"
                      >
                        Explore
                      </v-btn>
                    </div>
                  </v-card>
                </v-hover>
              </div>
              <div class="col-md-2 col-sm-4 col-xs-12 text-center" >
                <v-hover
                  v-slot:default="{ hover }"
                  open-delay="200"
                >
                  <v-card
                    :elevation="hover ? 16 : 2"
                  >
                    <v-img
                      class="white--text align-end"
                      height="200px"
                      :src="require('../assets/img/shop/3.jpg')"
                    >
                    </v-img>

                    <v-card-text class="text--primary text-center">
                      <div>Upto 60% + Extra 10%</div>
                      <div>Nike, Adidas, Puma</div>
                    </v-card-text>

                    <div class="text-center">
                      <v-btn
                        class="ma-2"
                        outlined
                        color="info"
                      >
                        Explore
                      </v-btn>
                    </div>
                  </v-card>
                </v-hover>
              </div>
            </div>
          </v-card-text>
        </div>
      </div>
    </v-container>
    <v-card  class="accent" >
      <v-container>
        <v-row no-gutters>
          <v-col class="col-12 col-md-4 col-sm-12">
            <v-row >
              <v-col class="col-12 col-sm-3 pr-4 hidden-sm-only" align="right">
                <v-icon class="display-2">mdi-truck</v-icon>
              </v-col>
              <v-col class="col-12 col-sm-9 pr-4">
                <h3 class="font-weight-light">FREE SHIPPING & RETURN</h3>
                <p class="font-weight-thin">Free Shipping over $300</p>
              </v-col>
            </v-row>
          </v-col>
          <v-col class="col-12 col-md-4 col-sm-12">
            <v-row >
              <v-col class="col-12 col-sm-3 pr-4" align="right">
                <v-icon class="display-2">mdi-cash-usd</v-icon>
              </v-col>
              <v-col  class="col-12 col-sm-9 pr-4">
                <h3 class="font-weight-light">MONEY BACK GUARANTEE</h3>
                <p class="font-weight-thin">30 Days Money Back Guarantee</p>
              </v-col>
            </v-row>
          </v-col>
          <v-col class="col-12 col-md-4 col-sm-12">
            <v-row>
              <v-col class="col-12 col-sm-3 pr-4" align="right">
                <v-icon class="display-2">mdi-headset</v-icon>
              </v-col>
              <v-col  class="col-12 col-sm-9 pr-4">
                <h3 class="font-weight-light">020-800-456-747</h3>
                <p class="font-weight-thin">24/7 Available Support</p>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </div>
</template>
<script>
    export default {
        data: () => ({
        }),
    }
</script>
