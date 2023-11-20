<template>
  <div class="wrapper">
    <div class="wrapper-block">
      <div class="text-wrap">
        <div class="text-header">Welcome</div>
        <div class="text-title">Best Learning<br />Opportunities</div>
        <div class="text-subtitle">
          Our goal is to make online<br />education work for everyone
        </div>
        <div class="btns">
          <div class="btn-join">Join Us</div>
          <div class="btn-learn">Learn More</div>
        </div>
      </div>
      <div class="img">
        <img src="../assets/hero-cover-1.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FirstContainer",
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "./src/styles/colors.scss";

.wrapper {
  background-color: $pink;
  font-family: "Montserrat-Bold", Helvetica;
  &-block {
    display: flex;
    justify-content: space-around;
    align-items: center;
    width: 100%; /* Задаем максимальную ширину, если необходимо */
    margin: 0 auto;
  }
}
.title {
  color: $primary-green;
}
.img img {
  height: 650px;
  width: auto;
  max-width: 100%;
  object-fit: cover;
  position: relative;
  right: 0;
  top: 0;
}
.btns {
  display: flex;
  align-items: center;
  cursor: pointer;
}
.btn {
  &-join {
    background-color: $primary-green;
    color: $white;
    font-size: 14px;
    font-weight: 500;
    padding: 15px 40px;
    border-radius: 5px;
    &:hover {
      background-color: rgb(63, 159, 71);
      transition: 0.2s;
    }
    &:active {
      background-color: grey;
      transition: 0.1s ease-in-out;
    }
    a {
      color: $white;
      text-transform: uppercase;
      text-decoration: none;
    }
  }
  &-learn {
    background-color: $pink;
    border: 2px solid $primary-green;
    color: $primary-green;
    font-size: 14px;
    font-weight: 500;
    padding: 15px 25px;
    border-radius: 10px;
    margin: 0 10px;
    &:hover {
      background-color: rgb(251, 193, 193);
      color: darkolivegreen;
      transition: 0.2s;
    }
    &:active {
      background-color: rgb(165, 135, 135);
      transition: 0.1s ease-in-out;
    }
    a {
      color: $white;
      text-transform: uppercase;
      text-decoration: none;
    }
  }
}
.text {
  &-wrap {
    flex: 1;
    padding-left: 200px;
  }
  &-header {
    color: $primary-green;
    font-size: 16px;
    font-weight: bold;
    margin-bottom: 20px;
  }
  &-title {
    color: $dark-blue;
    font-size: 58px;
    font-weight: bold;
    margin-bottom: 20px;
    line-height: 80px;
    letter-spacing: 0.2px;
  }
  &-subtitle {
    color: $dark-grey;
    font-size: 20px;
    font-weight: 200;
    letter-spacing: 0.2px;
    line-height: 30px;
    margin-bottom: 20px;
    font-weight: 400;
  }
}
//mobile styles
@media (max-width: 768px) {
  .wrapper {
    background-color: $pink;
    font-family: "Montserrat-Bold", Helvetica;
    &-block {
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 100%;
      margin: 0 auto;
    }
  }

  .img img {
    height: auto;
    width: 100%;
    max-width: 100%;
    object-fit: cover;
    position: relative;
    right: 0;
    top: 0;
  }

  .text {
    &-wrap {
      padding: 20px;
      text-align: center;
    }

    &-header {
      color: $primary-green;
      font-size: 16px;
      font-weight: bold;
      margin-bottom: 10px;
    }

    &-title {
      color: $dark-blue;
      font-size: 32px;
      font-weight: bold;
      margin-bottom: 10px;
      line-height: 40px;
    }

    &-subtitle {
      color: $dark-grey;
      font-size: 16px;
      font-weight: 200;
      letter-spacing: 0.2px;
      line-height: 24px;
      margin-bottom: 20px;
      font-weight: 400;
    }
  }

  .btns {
    display: flex;
    flex-direction: column;
    align-items: center;
    cursor: pointer;
  }

  .btn {
    &-join,
    &-learn {
      margin: 10px 0;
    }
  }
}
</style>
