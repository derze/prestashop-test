<template>
  <div>
    <h1>Your order</h1>
    <!-- card order -->
    <div class="card-order">
        <div class="card-order-top">
          <div class="order-price">
              <span>Cart total (1)</span>
              <div >
                <span class="price-ancient">{{priceNow}}€</span>
                <span class="price-recent">{{pricePre}}€</span>
              </div>
          </div>
        </div>
        <div class="card-order-middle-top">
            <a href="#">Use promotion code</a>
        </div>
        <div class="card-order-middle-bottom">
          <span class="total-ex">Total (excl. tax)</span>
          <span class="prix">{{taxEx}}€</span>
        </div>
        <div class="card-order-bottom">
            <div class="order-tax-price">
              <span class="order-total">Total <span style="font-weight:lighter">(incl. tax)</span></span>
              <span class="order-price">{{totalTax}}€</span>
            </div>
            <button class="btn">Procéder au paiement</button>
        </div>
    </div>
        <!-- Secure Payment -->
        <div class="payment">
          <span class="secure-text"><img src="../assets/White_lock.svg" alt=""> 100% secure payment</span>
          <img src="../assets/Group-22.svg" alt="" srcset="">
        </div>
  </div>
</template>


// script
<script>

export default {
  name: 'orderComponent',
  data (){
      return{
        priceNow: 285,
        pricePre: 295,
        taxEx: 240, 
        totalTax: 265,
      }
  },
  methods: {
    
  }
  }
  

</script>

<style lang="scss" src="./Order-component.scss">

</style>
