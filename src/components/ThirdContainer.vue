<template>
  <div class="wrapper">
    <div class="wrapper-block">
      <div class="text">
        <div class="text-header">Team</div>
        <div class="text-title">Get Quality Education</div>
        <div class="text-subtitle">
          Problems trying to resolve the conflict between the two major realms
          of Classical physics: Newtonian mechanics
        </div>
      </div>
    </div>
    <div class="card-container">
      <div class="carousel-container" ref="carouselContainer">
        <div class="carousel-wrapper" ref="carouselWrapper">
          <div
            class="card"
            v-for="(card, index) in cards"
            :key="index"
            @click="cardClick(index)"
          >
            <div class="card-item mt-5">
              <img :src="card.image" alt="" />
              <div class="card-title">{{ card.title }}</div>
              <div class="card-subtitle">{{ card.subtitle }}</div>
              <div class="card-icons">
                <img class="card-fb" src="../assets/fb.png" alt="" />
                <img class="card-inst" src="../assets/inst.png" alt="" />
                <img class="card-twt" src="../assets/twt.png" alt="" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="js">

export default {
  data() {
    return {
      cards: [
        { image: "https://i.imgur.com/L5uFZuW.png", title: "Julian Jameson", subtitle: "Profession" },
        { image: "https://i.imgur.com/3iYtCUO.png", title: "Julian Jameson", subtitle: "Profession" },
        { image: "https://i.imgur.com/fnkbb5g.png", title: "Julian Jameson", subtitle: "Profession" },
        { image: "https://i.imgur.com/rcdJBTI.png", title: "Julian Jameson", subtitle: "Profession" },
      ],
      currentIndex: 0,
      intervalId: null,

    };

  },

};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "./src/styles/colors.scss";

.wrapper {
  background-color: $white;
  font-family: "Montserrat-Bold", Helvetica;
  &-block {
    display: flex;
    justify-content: flex-start;
    margin: 0 300px;
  }
}
.text {
  &-header {
    color: $primary-green;
    font-size: 14px;
    font-weight: bold;
    line-height: 24px;
    font-weight: 700;
    letter-spacing: 0.2px;
    margin-bottom: 20px;
  }
  &-title {
    color: $dark-blue;
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 20px;
    font-weight: 700;
    line-height: 32px;
    letter-spacing: 0.1px;
  }
  &-subtitle {
    color: $dark-grey;
    font-size: 14px;
    font-weight: 400;
    letter-spacing: 0.2px;
    line-height: 20px;
    margin-bottom: 20px;
    font-weight: 400;
  }
}
.card {
  &-container {
    display: flex;
    justify-content: center;
    margin: 100px 0;
    gap: 25px;
  }
  &-item {
    border-radius: 10px;
    width: 238px;
    height: 375px;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
    text-align: center;
    img {
      border-radius: 10px 10px 0 0;
    }
  }
  &-title {
    color: $dark-blue;
    font-size: 16px;
    font-weight: bold;
    margin: 20px 0 10px 0;
    font-weight: 700;
    line-height: 24px;
    letter-spacing: 0.1px;
  }
  &-subtitle {
    color: $dark-grey;
    font-size: 14px;
    font-weight: 400;
    letter-spacing: 0.2px;
    line-height: 20px;
    margin-bottom: 10px;
    font-weight: 400;
  }
  &-icons {
    gap: 20px;
    display: flex;
    justify-content: center;
  }
}
.carousel-wrapper {
  display: flex;
  animation: carouselAnimation 15s linear infinite;
  gap: 25px;
}

.card {
  flex: 0 0 auto;
}

// mobile styles
@media (max-width: 768px) {
  .wrapper {
    background-color: $white;
    font-family: "Montserrat-Bold", Helvetica;
    &-block {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin: 20px;
    }
    .carousel-wrapper {
      display: flex;
      flex-direction: column;
      animation: carouselAnimation 15s linear infinite;
      gap: 15px;
    }
    .text {
      &-header {
        color: $primary-green;
        font-size: 14px;
        font-weight: bold;
        line-height: 24px;
        font-weight: 700;
        letter-spacing: 0.2px;
        margin-bottom: 10px;
        text-align: center;
      }

      &-title {
        color: $dark-blue;
        font-size: 24px;
        font-weight: bold;
        margin-bottom: 10px;
        font-weight: 700;
        line-height: 32px;
        letter-spacing: 0.1px;
        text-align: center;
      }

      &-subtitle {
        color: $dark-grey;
        font-size: 14px;
        font-weight: 400;
        letter-spacing: 0.2px;
        line-height: 20px;
        margin-bottom: 20px;
        text-align: center;
      }
    }

    .card-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-around;
      margin: 20px;
      gap: 20px;
      width: 100%;
    }

    .card-item {
      border-radius: 10px;
      width: 100%;
      box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
      text-align: center;
      img {
        border-radius: 10px 10px 0 0;
      }
    }

    .card-title {
      color: $dark-blue;
      font-size: 16px;
      font-weight: bold;
      margin: 10px 0;
      font-weight: 700;
      line-height: 24px;
      letter-spacing: 0.1px;
    }

    .card-subtitle {
      color: $dark-grey;
      font-size: 14px;
      font-weight: 400;
      letter-spacing: 0.2px;
      line-height: 20px;
      margin-bottom: 10px;
      font-weight: 400;
    }

    .card-icons {
      gap: 20px;
      display: flex;
      justify-content: center;
    }
  }
}
</style>
