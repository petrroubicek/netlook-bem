<template>
  <div class="home">
    <!-- INTRO -->
    <h1 class="home__title">VÍTEJTE</h1>
    <p class="home__description">Výsledné řešení se nachází
      <br>po kliknutí na konkrétní button.
    </p>

    <!-- TASKS -->
    <button
      type="button"
      class="home__component-button btn btn--primary btn--radius"
      @click="showPopUpFN(datas.popUp1.profileImg, 
      datas.popUp1.title, 
      datas.popUp1.doubleRowTitle, 
      datas.popUp1.message, 
      datas.popUp1.btnHorizontal,
      datas.popUp1.btn1Text, 
      datas.popUp1.btn1Class, 
      datas.popUp1.btn2Text, 
      datas.popUp1.btn2Class)"
    >Show popup #1</button>
    
    <button
      type="button"
      class="home__component-button btn btn--primary btn--radius"
      @click="showPopUpFN(datas.popUp2.profileImg, 
      datas.popUp2.title, 
      datas.popUp2.doubleRowTitle, 
      datas.popUp2.message, 
      datas.popUp2.btnHorizontal,
      datas.popUp2.btn1Text, 
      datas.popUp2.btn1Class, 
      datas.popUp2.btn2Text, 
      datas.popUp2.btn2Class)"
    >Show popup #2</button>
    
    <button
      type="button"
      class="home__component-button btn btn--primary btn--radius"
      @click="showContentFN()"
    >Show content</button>

    <!-- CONTACT -->
    <a
      href="tel:777556047"
      class="home__contact-button btn btn--primary btn--radius btn--border"
    >Zavolat řešiteli</a>
  </div>
</template>

<script>
export default {
  name: "Home",
  props: {
    selectedComponent: String,
    showPopUpFN: Function,
    showContentFN: Function
  },
  data() {
    return {
      datas: {
        popUp1: {
          profileImg: "",
          title: "Title example for two rows",
          doubleRowTitle: true,
          message: "Random text all users will see. You",
          btnHorizontal: false,
          btn1Text: "Btn1",
          btn1Class: "btn btn--primary btn--radius btn--shadow",
          btn2Text: "Btn3",
          btn2Class: "btn"
        },
        popUp2: {
          profileImg: "../images/girl.png",
          title: "Title example for two rows",
          doubleRowTitle: false,
          message: "Random text all users will see. You don´t know",
          btnHorizontal: true,
          btn1Text: "Btn2",
          btn1Class: "btn btn--border btn--radius",
          btn2Text: "Btn1",
          btn2Class: "btn btn--primary btn--radius"
        }
      }
    };
  }
};
</script>

<style lang="scss">
@import "../assets/scss/_home.scss";
</style>