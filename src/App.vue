<template>
  <div id="app">
    <!-- modal -->
    <ModalComponent id="Amodal" v-if="showModal" @closed="isVisible" style="position:fixed; z-index:5; top:50%;left:46%; transform: translate(-50%,-50%);">
      <span slot="descriptif">{{title}}</span>
      <span slot="describe">{{description}}</span>
    </ModalComponent>

    <!-- Navbar -->
    <NavComponent></NavComponent>
    <!-- container de tout les component -->
    <div class="container">
      <div class="row">
        <!-- details du panier -->
          <CartComponent class="col-md-8"></CartComponent>
          <!-- Panier -->
          <orderComponent class="col-md-4"></orderComponent>
        <!-- ARTICLES  -->
          <!-- cadre de tout les articles -->
          <div class="Acomponent col-md-8">
            <!-- titre -->
              <h1>Complétez votre panier</h1>
              <!-- contour de la carte -->
              <div class="general-card">
                <ArticleComponent  v-on:showit="isVisible()" v-for='article in articles' :key='article.id'>
                  <span slot=titre>{{article.title}}</span>
                  <p slot="description">{{article.description}}</p>
                  <div class="best-seller-panel" v-if="article.bestPanel" slot="bestPanel"><span>Best seller</span></div>
                    <button class="btn" type="submit" v-on:click="isVisible(),title=article.title,description=article.description" slot='boutton'>Ajouter au panier</button>
                </ArticleComponent>
              </div>
           </div>
           <!-- FIN DE ARTICLES -->
      </div>
    </div>
    <FooterComponent></FooterComponent>
  </div>
</template>

<script>
// component
import NavComponent from './components/Nav-component.vue'
import CartComponent from './components/Cart-component.vue'
import orderComponent from './components/Order-component'
import ArticleComponent from './components/Article-component'
import FooterComponent from './components/Footer-component'
import ModalComponent from './components/Modal-component'

const $ = require('jquery');
window.$ = $
export default {
  name: 'app',
  components: {
    NavComponent,
    CartComponent,
    orderComponent,
    ArticleComponent,
    FooterComponent,
    ModalComponent
  },
  data(){
   return{
      showModal: false,
      title: '',
      description: '',

        articles: [{
          id: 1,
          img: '',
          title:'1: Fidélisation - Bons de réduction après daouda',
          description: 'Voici les details de la carte 1: Synchronisez votre boutique avec votre compte Ebay ',
          bestPanel: true,
          economie: true

        },
        {
          id: 2,
          img: '',
          title:'2: Fidélisation - Bons de réduction après achat',
          description: 'Voici les details de la carte 2: Synchronisez votre boutique avec votre compte Ebay ',
          bestPanel: false,
          economie: false
        },{
         id: 3,
          img: '',
          title:'3: Fidélisation - Bons de réduction après achat',
          description: 'Voici les details de la carte 3: Synchronisez votre boutique avec votre compte Ebay ',
          bestPanel: true,
          economie: true

        }]

   }
  },
  methods:{
    isVisible: function(){
      this.showModal= !this.showModal;
      
     
    }
  }
}
</script>

<style lang="scss" src="./styles/root.scss">
#Amodal{
  }
  
</style>
