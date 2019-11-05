<template>
 <div class="navbar ">
     <nav class="container">
       <!-- image -->
       <div class="logo">
         <img src="../assets/logo_ps_first.svg" alt="" style="margin:5px;">
         <img src="../assets/logo_ps_second.svg" alt="">
        </div>
        <!-- etapes -->
        <div class="steps">
          <div class="line"></div>
          <div class="step-container"><div class="step step-active"><p>Cart</p> <span>1</span></div></div>
              <div class="hr-line"><hr></div>
          <div class="step-container"><div class="step"> <p>Authentification</p><span>2</span></div></div>
              <div class="hr-line"><hr></div>
          <div class="step-container"><div class="step"> <p>Payment</p><span>3</span></div></div>
        </div>
        <div class="help">
          <span class="help-text">Need help ?</span><br>
          <img src="../assets/call-24px.svg" alt="" srcset=""> 
          <span class="help-number"> +44 .2 036.971.999</span>
        </div>
     </nav>
 </div>
</template>

<script>
export default {
  name: 'NavComponent',
  props: {
    msg: String
  }
}
</script>
<style lang="scss" src="./Nav-component.scss"></style>
