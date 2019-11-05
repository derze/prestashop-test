<template>
    <div>
      <div class="closeModal" @click="closeModal">
        <img src="../assets/modal/close.svg" alt="">
      </div>
            <div class="container modal-container" >
              <!-- slider -->
                  <div class="slider">
                    <div class="prev"><img src="../assets/keyboard_arrow_left.svg" alt=""></div>
                      <div class="img"><img src="" alt=""></div>
                    <div class="next "><img src="../assets/keyboard_arrow_right.svg" alt=""></div>
                  </div>
                  <!-- details -->
                <div class="modal-details">
                   <div class="title">
                      <div class="img" style="	height: 50px;	width: 50px;background:#d2d2d2"></div>
                        <span><slot name="descriptif"></slot></span>
                    </div>
                    <div class="notation-avis">
                   <div class="etoiles">
                      <img src="../assets/Gold_Star.svg" alt="" srcset="">
                      <img src="../assets/Gold_Star.svg" alt="" srcset="">
                      <img src="../assets/Gold_Star.svg" alt="" srcset="">
                      <img src="../assets/Gold_Star.svg" alt="" srcset="">
                      <img src="../assets/Gold_Star.svg" alt="" srcset="">
                   </div>
                   <span class="avis">125 avis</span>
                    </div>
                    <div class="badge">
                      <div class="navigation"><span>Navigation</span></div>
                      <div class="conversion"><span>Conversion</span></div>
                    </div>
                    <div class="text-article">
                      <slot name="describe"></slot>
                    </div>
                    <div class="demo">
                      <span>DEMO BOUTIQUE</span>
                    </div>
                    <button class="ajouter">Ajouter au panier</button>
                   </div>
                   

            </div>
    </div>   
</template>


// script
<script>

export default {
  name: 'ModalComponent',
  data (){
    return {
       
  }
  },
  methods: {
   closeModal: function(){
     this.$emit('closed');
   }
      
   }

      
  }

</script>

<style lang="scss" src="./Modal-component.scss">

</style>
