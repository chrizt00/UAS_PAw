<template>
  <v-app id="inspire">
    <v-app-bar
      :clipped-left="$vuetify.breakpoint.lgAndUp"
      app
      color="primary"
      dark
    >
<!--      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />-->

      <v-toolbar-title
        style="width: 350px"
      >
        <a href="/" class="white--text" style="text-decoration: none"><v-icon>mdi-truck</v-icon>&nbsp;ShipIT</a>
      </v-toolbar-title>

     
      
      <v-text-field
        flat
        solo-inverted
        hide-details
        prepend-inner-icon="mdi-magnify"
        label="Search"
        class="hidden-sm-and-down pl-10 ml-4"
      />
      <v-spacer />
      <v-btn v-on="on" href="/cart" icon>
        <v-badge
          content="2"
          value="2"
          color="green"
          overlap
        >
          <v-icon>mdi-cart</v-icon>
        </v-badge>
      </v-btn>




      <v-menu>
        <template v-slot:activator="{ on }">
          <v-btn icon v-on="on">
            <v-icon>mdi-account-circle</v-icon>
          </v-btn>
        </template>
        
       <v-card
          class="mx-auto"
          max-width="344"
          outlined
          close-on-content-click>
          

          <v-list-item-group c>
         <v-flex>
        <login />
      </v-flex>

      <v-flex>
        <Register />
      </v-flex>

      <v-flex>
        <updateProfil />
      </v-flex>
          </v-list-item-group>
        </v-card>
      </v-menu>
    </v-app-bar>
    <v-content>
      <v-bottom-navigation
        :value="activeBtn"
        color="primary"
        horizontal
      >
        <a href="/" class="v-btn">
          <span>Home</span>
        </a>
        <a href="/shop" class="v-btn">
          <span>Shop</span>
        </a>
        <a href="/product" class="v-btn">
          <span>Product</span>
        </a>
        <v-btn href="/blog">
          <span>Blog</span>
        </v-btn>
      </v-bottom-navigation>
    </v-content>
      <router-view/>
    <v-footer
      :padless="true"
    >
      <v-card
        flat
        tile
        width="100%"
        class="secondary white--text text-center"
      >
        <v-card-text>
          <v-btn
            class="mx-4 white--text"
            icon
          >
            <v-icon size="24px">mdi-home</v-icon>
          </v-btn>
          <v-btn
            class="mx-4 white--text"
            icon
          >
            <v-icon size="24px">mdi-email</v-icon>
          </v-btn>
          <v-btn
            class="mx-4 white--text"
            icon
          >
            <v-icon size="24px">mdi-calendar</v-icon>
          </v-btn>
           <v-btn
            class="mx-4 white--text"
            icon
          >
            <v-icon size="24px">mdi-delete</v-icon>
          </v-btn>

        </v-card-text>
        <v-divider></v-divider>

        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} — <strong>ShipIT</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>
<script>
import login from './login'
import Register from './Register'
import updateProfil from './updateProfil'

    export default {
        components:{login, Register, updateProfil},
        
        data () {
            return {
                items: [
                    { title: 'Login' , router: <login />},
                    { title: 'Sign Up', router: 'Register' },
                    { title: 'My Profile', router: './updateProfil' },
                ],
                activeBtn: 1,
            }
        },

        methods: {
      onOptionChanged(title) {
        this.$bvModal.msgBoxConfirm('Please confirm that you want to delete everything.')
        .then(confirmed => {
          if(confirmed) {
            this.actualOption = value;
          } else {
            this.selectedOption = this.actualOption;
          }
        }).
        catch(() => {
          /* Reset the value in case of an error */
          this.selectedOption = this.actualOption;
        })
      }
    }
    }
</script>
