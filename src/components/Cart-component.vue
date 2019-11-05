<template>
  <div>
    <h1>Your cart (1)</h1>
    <div class="card-cart">
      <div class="card-cart-header">
          <div class="img-place"></div>
        <div class="description">
        <span >Module Custom Suggestions - Related Products</span>
        <p>By PrestaShop</p>
       </div>
          <span class="solde">-30%</span>
          <div class="choix">
            <!-- remplacer par une div, valeur change au clic des fleche haut et bas -->
            <input value="1" min="1" max="9" type="number" class="select"/>
            <!--  -->
            <a href="#" class="supprimer">Supprimer</a>
            <div class="prices ">
              <span class="price-ancient ">{{oldPrice}}</span>
              <span class="price-recent " >{{price}}€</span>
            </div>
          </div>
      </div>
      <div class="card-footer">
        <div class="footer-haut ">
          <div class="support">
                      <span class="">Support mise a jour <img src="../assets/icons8-undefined-24.png" alt="" srcset=""></span>
                        <div class="radio-container">
                          <form style="display:flex">
                            <label class="classique radio">
                              <input type="radio" name="option" value="male"> Classique - 3 mois <B>Inclus</B>
                                  
                              </label>
                            <label class="zen radio">
                              <input type="radio" name="option" value="male"> Zen - 12 mois
                              <span>RECOMMANDE</span><B>90€</B>
                              </label>                      
                            </form>
                        </div>
          </div>
        </div>
       
        <div class="footer-bas ">
          <form action="">
            <input type="checkbox" name="installation" id="installation">
            <label for="installation">Option installation</label>
          </form>
          <div class="module"><span>Module installé par nos experts en toute sécurité </span><B>90€</B></div>
        </div>
      </div>
    </div>
  </div>
</template>


// script
<script>


export default {
  name: 'CartComponent',
  data (){
    return {
      price: 195,
      oldPrice: 230,
      
      }
  },
  methods: {
    // price-recent prend sa valeur * le nombre du select 
   priceCalc: function(){
      
      
   }

      
  }
}
</script>

<style lang="scss" src="./Cart-component.scss">

</style>
