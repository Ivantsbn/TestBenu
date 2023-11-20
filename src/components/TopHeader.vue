<template>
  <div class="wrapper">
    <!-- NAVBAR -->
    <div class="header">
      <div class="container">
        <div class="header-section">
          <div class="header-logo">
            <div>Brandname</div>
          </div>
          <div class="nav">
            <a href="#">Home</a>
            <a href="#">Product</a>
            <a href="#">Pricing</a>
            <a href="#">Contact</a>
          </div>
          <div class="btns">
            <div class="btn-login">
              <a href="#">Login</a>
            </div>
            <div class="btn-join">
              <a href="#">join us</a>
              <a class="arrow">&rarr;</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Mobile menu -->
    <div class="burger-btn" @click="toggleBurgerMenu">
      <span></span>
      <span></span>
      <span></span>
    </div>
    <div class="burger-menu" :class="{ open: isBurgerMenuOpen }">
      <a href="#">Home</a>
      <a href="#">Product</a>
      <a href="#">Pricing</a>
      <a href="#">Contact</a>
    </div>
  </div>
</template>

<script lang="js">
export default {
  name: "TopHeader",
  props: {},
  data() {
    return {
      isBurgerMenuOpen: false,
    };
  },
  methods: {
    toggleBurgerMenu() {
      this.isBurgerMenuOpen = !this.isBurgerMenuOpen;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "./src/styles/colors.scss";

.wrapper {
  background-color: $pink;
  font-family: "Montserrat-Bold", Helvetica;
}
.container {
  margin: 0 250px;
  height: 91px;
}
.header {
  @media (max-width: 720px) {
    display: none;
  }
  &-logo {
    color: $dark-blue;
    font-size: 32px;
    font-weight: 700;
    letter-spacing: 0.1px;
    line-height: 32px;
    white-space: nowrap;
  }
  &-section {
    padding-top: 20px;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
  }
}
.nav a {
  color: $dark-grey;
  text-decoration: none;
  font-size: 16px;
  margin-right: 30px;

  font-weight: 700;
  &:hover {
    color: black;
    transition: 0.2s ease-in-out;
    font-weight: 700;
    text-decoration: underline;
  }
}
.btns {
  display: flex;
  align-items: center;
}
.btn {
  &-login a {
    color: $primary-green;
    text-decoration: none;
    font-size: 14px;
    font-weight: 700;
    margin-right: 50px;
    letter-spacing: 0.2px;
    line-height: 22px;
    &:hover {
      color: rgb(63, 159, 71);
      transition: 0.2s;
    }
    &:active {
      color: grey;
      transition: 0.1s ease-in-out;
    }
  }

  &-join {
    background-color: $primary-green;
    color: $white;
    font-size: 14px;
    font-weight: 500;
    padding: 15px 20px;
    border-radius: 10px;
    &:hover {
      background-color: rgb(63, 159, 71);
      transition: 0.1s;
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
}
.arrow {
  margin-left: 10px;
}
@media (min-width: 768px) {
  .burger-menu a {
    display: none;
  }
}

//mobile styles
@media (max-width: 768px) {
  .burger-btn {
    z-index: 10;
    display: none;
    cursor: pointer;
    padding: 10px;
    background-color: transparent;
    border: none;

    span {
      display: block;
      width: 25px;
      height: 3px;
      background-color: $dark-blue;
      margin: 5px 0;
      transition: 0.4s;
    }

    &:hover span {
      background-color: $primary-green;
    }
  }

  .burger-menu {
    position: fixed;
    top: 0;
    right: 0;
    max-width: 60px;
    height: 16%;
    background-color: transparent 0.5;
    padding: 20px;
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    justify-content: flex-start;
    transform: translateX(100%);
    transition: transform 0.4s ease-in-out;
    z-index: 2;

    a {
      color: $dark-grey;
      border-bottom: 1px solid $dark-grey;
      text-decoration: none;
      font-size: 16px;
      margin-bottom: 15px;
      font-weight: 700;

      &:hover {
        color: black;
        transition: 0.2s ease-in-out;
        font-weight: 700;
        text-decoration: underline;
      }
    }

    &.open {
      transform: translateX(0);
    }
  }

  .nav {
    display: none;
  }

  .burger-btn {
    display: block;
  }

  .header-section {
    flex-direction: column;
    align-items: flex-start;
  }

  .burger-menu {
    width: 100%;
  }
}
</style>
