<template>
  <div class="wrapper">
    <div class="wrapper-block">
      <div class="text">
        <img class="text-line" src="../assets/red-line.png" alt="" />
        <div class="text-title">Approdable Packages</div>
        <div class="text-subtitle">
          Problems trying to resolve the conflict between<br />
          the two major realms of Classical physics:<br />
          Newtonian mechanics
        </div>
        <div class="text-btn">
          Learn More<img class="arrow" src="../assets/arrow-next.png" alt="" />
        </div>
      </div>
      <div class="card-wrapper">
        <div class="card">
          <img class="card-logo" src="../assets/board.png" alt="" />
          <div class="card-title">Certified Teacher</div>
          <img class="card-line" src="../assets/thin-line.png" alt="" />
          <div class="card-subtitle">
            The gradual accumulation of information about
          </div>
        </div>
        <div class="card">
          <img class="card-logo" src="../assets/telescope.png" alt="" />
          <div class="card-title">Expert instruction</div>
          <img class="card-line" src="../assets/thin-line.png" alt="" />
          <div class="card-subtitle">
            The gradual accumulation of information about
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SecondContainer",
  props: {},
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
    justify-content: space-evenly;
    align-items: center;
    height: 677px;
  }
}
.text {
  &-line {
    color: $dark-red;
    margin-bottom: 30px;
  }
  &-title {
    color: $dark-blue;
    font-size: 50px;
    font-weight: 700;
    line-height: 50px;
    letter-spacing: 0.2px;
    margin-bottom: 30px;
  }
  &-subtitle {
    color: $dark-grey;
    font-size: 14px;
    margin-bottom: 30px;
    font-weight: 400;
    line-height: 20px;
    letter-spacing: 0.2px;
  }
  &-btn {
    color: $primary-green;
    position: relative;
    font-weight: 700;
    .arrow {
      padding-left: 10px;
      position: absolute;
      top: 0px;
      &:hover {
        transition: 0.4s ease;
        transform: translateX(5px);
      }
    }
  }
}
.card-wrapper {
  display: flex;
  gap: 30px;
}
.card {
  border-radius: 10px;
  height: 292px;
  width: 239px;
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
  &:hover {
    box-shadow: 0 15px 20px rgba(0, 0, 0, 0.2);
    transition: 0.2s ease-in-out;
  }
  &-logo {
    padding: 30px 0 20px 30px;
  }
  &-title {
    padding-left: 30px;
    color: $dark-blue;
    font-size: 16px;
    font-weight: 700;
    line-height: 24px;
    letter-spacing: 0.1px;
  }
  &-line {
    padding: 20px;
    display: flex;
  }
  &-subtitle {
    padding-top: 10px;
    color: $dark-grey;
    padding-left: 30px;
    font-size: 14px;
    margin-bottom: 30px;
    font-weight: 400;
    line-height: 20px;
    letter-spacing: 0.2px;
  }
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
      height: auto;
      padding: 20px;
    }
  }

  .text {
    &-line {
      color: $dark-red;
      display: flex;
      margin: 5px auto;
      margin-bottom: 15px;
    }

    &-title {
      color: $dark-blue;
      font-size: 32px;
      font-weight: 700;
      line-height: 40px;
      letter-spacing: 0.2px;
      margin-bottom: 15px;
      text-align: center;
    }

    &-subtitle {
      color: $dark-grey;
      font-size: 14px;
      margin-bottom: 15px;
      font-weight: 400;
      line-height: 20px;
      letter-spacing: 0.2px;
      text-align: center;
    }

    &-btn {
      color: $primary-green;
      font-weight: 700;
      text-align: center;
      .arrow {
        display: none;
      }
    }
  }

  .card-wrapper {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .card {
    width: 100%;
    border-radius: 10px;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
    &:hover {
      box-shadow: 0 15px 20px rgba(0, 0, 0, 0.2);
      transition: 0.2s ease-in-out;
    }
    &-logo {
      padding: 40px;
    }
    &-title {
      color: $dark-blue;
      font-size: 16px;
      font-weight: 700;
      line-height: 24px;
      letter-spacing: 0.1px;
      text-align: center;
      padding: 0 20px;
    }
    &-line {
      width: 20%;
      height: 3px;
      margin: 0 auto;
    }
    &-subtitle {
      color: $dark-grey;
      font-size: 14px;
      margin-bottom: 20px;
      font-weight: 400;
      line-height: 20px;
      letter-spacing: 0.2px;
      text-align: center;
      padding: 0 20px;
    }
  }
}
</style>
