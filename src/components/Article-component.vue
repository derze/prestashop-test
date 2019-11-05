<template>

        <div class="article-card" >
      <div class="card-container">
          <div class=" card-article">
              <div class="card-article-header">
                <div class="img"></div>
                <span class="titre"><slot name="titre"></slot> </span>
              </div>
              <div>
                <p class="descriptif"><slot name="description"></slot> </p>
              </div>
              <div class="commemtaire">
                <slot name="bestPanel"></slot>
                <div class="etoile">
                  <img src="../assets/Gold_Star.svg" alt="" srcset="" class="etoile">
                  <img src="../assets/Gold_Star.svg" alt="" srcset="" class="etoile">
                  <img src="../assets/Gold_Star.svg" alt="" srcset="" class="etoile">
                  <img src="../assets/Gold_Star.svg" alt="" srcset="" class="etoile">
                  <img src="../assets/Empty_Star.svg" alt="" srcset="" class="etoile">   
                </div>
              </div>
              <div class="price_article" >
                <span class="price_recent">195€</span>
                <span class="price_ancient">230€</span>
                <span class="reduction" >Economisez 30%</span>
              </div>
              <slot name="boutton"></slot>
            </div>
          

      </div>  
        </div>
</template>


// script
<script>
// emit une variable a app si cet vriable est vrai alors montrer la modal
export default {
  name: 'ArticleComponent',
  data (){
    
    return {

        titre: '',
        describe:'',
        economy:''   
      }
  },
  methods: {
    changeMsg: function(){
     this.$parent.title = this.titre;
     
   },
   openModel: function(article){
     this.$emit('showit',article)
     
   }
   
      
   }

      
  }

</script>

<style lang="scss" src="./Article-component.scss">

</style>
