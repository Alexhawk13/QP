<template>
   <section class="faq container">
    <h2>Frequently asked <mark>questions</mark></h2>
    <article>
      <div class="faq__box">
        <h3 class="faq__question">How do i change my details?</h3>
        <div class="show"  @click = "showAnswear"><img src="../assets/images/cross.svg" alt="cross" srcset=""></div>
      </div>
      
      <p class="faq__answear">We provide only the best trading software. The trading terminal MetaTrader4 is the most popular and convenient platform for access to global exchanges. You can work anywhere. All you need is the Internet because the necessary trading tools are already collected in one place and are available in a couple of clicks. Use only the best and develop with us!</p>
    </article>
    <article>
      <div class="faq__box">
        <h3 class="faq__question">How do i change my details?</h3>
        <div class="show"  @click = "showAnswear"><img src="../assets/images/cross.svg" alt="cross" srcset=""></div>
      </div>
      
      <p class="faq__answear">We provide only the best trading software. The trading terminal MetaTrader4 is the most popular and convenient platform for access to global exchanges. You can work anywhere. All you need is the Internet because the necessary trading tools are already collected in one place and are available in a couple of clicks. Use only the best and develop with us!</p>
    </article>
    <article>
      <div class="faq__box">
        <h3 class="faq__question">How do i change my details?</h3>
        <div class="show"  @click = "showAnswear"><img src="../assets/images/cross.svg" alt="cross" srcset=""></div>
      </div>
      
      <p class="faq__answear">We provide only the best trading software. The trading terminal MetaTrader4 is the most popular and convenient platform for access to global exchanges. You can work anywhere. All you need is the Internet because the necessary trading tools are already collected in one place and are available in a couple of clicks. Use only the best and develop with us!</p>
    </article>
    <article>
      <div class="faq__box">
        <h3 class="faq__question">How do i change my details?</h3>
        <div class="show"  @click = "showAnswear"><img src="../assets/images/cross.svg" alt="cross" srcset=""></div>
      </div>
      
      <p class="faq__answear">We provide only the best trading software. The trading terminal MetaTrader4 is the most popular and convenient platform for access to global exchanges. You can work anywhere. All you need is the Internet because the necessary trading tools are already collected in one place and are available in a couple of clicks. Use only the best and develop with us!</p>
    </article>
  </section>
</template>

<script>
export default {
  data()  {
    return {
    }
  },
  methods: {
    showAnswear: function(event) {
       console.log(`clicked on `+ event.target.localName);
      if (event.target.style.transform !== "none" && !event.target.style.transform) {
        event.target.style.transform = `rotate(45deg)`
      }
      else {
        event.target.style.transform = `none`
      }
      event.target.parentElement.parentElement.nextSibling.classList.toggle("active")
    }

    ,
  }
}
</script>

<style scoped>
  @import "../assets/styles/faq.css";
</style>