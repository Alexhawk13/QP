<template>
    <section class="comments container">
    <h2>People love Big <mark>Invest</mark></h2>
    
    <div class="wrapper">
      <div class="slider">
        <div id="trick" class="trick">
          <img src="../assets/images/Comment_photo.png" alt="photo">
          <span class="name">Albert Abello</span>
          <span class="role">Director of Growth</span>
          <img class="quotes" src="../assets/images/quotes.svg" alt="quotes" srcset="">
          <div class="text">This magical product actually works! It has radically changed the way we build our audiences. Increasing new customer sales by 6x in our most mature market.</div>
        </div>
        <div class="slide passive active">
          <div>
            <img src="../assets/images/Comment_photo.png" alt="photo">
            <div>
              <span class="name">Albert Abello</span>
              <span class="role">Director of Growth</span>
            </div>
            
          </div>
          
          <img class="quotes" src="../assets/images/quotes.svg" alt="quotes" srcset="">
          <div class="text">This magical product actually works! It has radically changed the way we build our audiences. Increasing new customer sales by 6x in our most mature market.</div>
        </div>
        <div class="slide passive">
          <img src="../assets/images/Comment_photo.png" alt="comment's author photo">
          <span class="name">Albert Abello</span>
          <span class="role">Director of Growth</span>
          <img class="quotes" src="../assets/images/quotes.svg" alt="quotes" srcset="">
          <div class="text">This magical product actually works! It has radically changed the way we build our audiences. Increasing new customer sales by 6x in our most mature market.</div>
        </div>
        <div class="slide passive">
          <img src="../assets/images/Comment_photo.png" alt="comment's author photo">
          <span class="name">Albert Abello</span>
          <span class="role">Director of Growth</span>
          <img class="quotes" src="../assets/images/quotes.svg" alt="quotes" srcset="">
          <div class="text">This magical product actually works! It has radically changed the way we build our audiences. Increasing new customer sales by 6x in our most mature market.</div>
        </div>
        <div class="slide passive">
          <img src="../assets/images/Comment_photo.png" alt="comment's author photo">
          <span class="name">Albert Abello</span>
          <span class="role">Director of Growth</span>
          <img class="quotes" src="../assets/images/quotes.svg" alt="quotes" srcset="">
          <div class="text">This magical product actually works! It has radically changed the way we build our audiences. Increasing new customer sales by 6x in our most mature market.</div>
        </div>
      </div>
      <div class="pagination">
        <button id="left" @click = "showPrevSlide" class="arrow">
          <img src="../assets/images/arrow_Left.svg" alt="" srcset="">
        </button>
        <span class="counter">0{{commentCount}} / 0{{commentsNumber}}</span>
        <button id="right" @click = "showNextSlide" class="arrow">
          <img src="../assets/images/arrow_Right.svg" alt="" srcset="">
        </button>
      </div>
      
    </div>
  </section>
</template>

<script>
export default {
  data()  {
    return {
      commentCount: 1,
      commentsNumber: null
    }
  },
  methods: {
    showNextSlide() {
      let currentElem = document.getElementsByClassName("active")[0]
      let nextElem = currentElem.nextSibling;
  
      if (nextElem !== null) {
        currentElem.classList.remove("active");
        currentElem.classList.add("next");
        nextElem.classList.add("active");

        this.raiseCommentCount();
      }
    },
    showPrevSlide() {
      let currentElem = document.getElementsByClassName("active")[0]
      let prevElem = currentElem.previousSibling; 
      let trickBlock = document.getElementById("trick");
      if (prevElem !== trickBlock) {
        currentElem.classList.remove("active");
        prevElem.classList.remove("next")
        prevElem.classList.add("active");  

        this.decreaseCommentCount();
      }
    },
    raiseCommentCount() {
      return (this.commentCount += 1);
    },
    decreaseCommentCount() {
      return (this.commentCount -= 1);
    }
  },
  mounted: function() {
    this.commentsNumber = document.getElementsByClassName('slide').length
  }
}
</script>

<style scoped>
  @import "../assets/styles/comments.css";
</style>
