<template>
  <div class="wrapper">
    <div class="wrapper-block">
      <div class="text">
        <div class="text-header">Newsletter</div>
        <div class="text-title">Watch our Courses</div>
        <div class="text-subtitle">
          Problems trying to resolve the conflict between<br />
          the two major realms of Classical physics: Newtonian mechanics
        </div>
        <div class="input-wrap">
          <input
            class="input-frame"
            type="text"
            placeholder="Your email"
            v-model="email"
          />
          <div class="input-btn" @click="subscribe">Subscribe</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="js">
export default {
  data() {
    return {
      email: "",
    };
  },
  methods: {
    subscribe() {
      if (this.email.includes("@")) {
        console.log("Subscribed with email:", this.email);
      } else {
        alert("Invalid email format");
      }
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
  &-block {
    display: flex;
    justify-content: center;
    margin: 0 220px;
  }
}
.text {
  text-align: center;
  padding-top: 100px;
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
    margin-bottom: 50px;
    font-weight: 400;
  }
}
.input {
  &-wrap {
    display: flex;
    justify-content: center;
    margin: 50px 20px;
  }
  &-frame {
    min-width: 551px;
    width: 100%;
    border: 1px solid lightgray;
    padding-left: 30px;
  }
  &-btn {
    background-color: $primary-green;
    color: $white;
    font-size: 14px;
    font-weight: 500;
    padding: 15px 40px;
    border-radius: 0 5px 5px 0;
    cursor: pointer;
    &:hover {
      background-color: rgb(63, 159, 71);
      transition: 0.2s;
    }
    &:active {
      background-color: grey;
      transition: 0.1s ease-in-out;
    }
  }
}

// mobile styles
@media (max-width: 768px) {
  .wrapper {
    background-color: $pink;
    font-family: "Montserrat-Bold", Helvetica;
    &-block {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin: 0 20px;
    }
  }

  .text {
    text-align: center;
    padding-top: 20px;
    &-header {
      color: $primary-green;
      font-size: 14px;
      font-weight: bold;
      line-height: 24px;
      font-weight: 700;
      letter-spacing: 0.2px;
      margin-bottom: 10px;
    }

    &-title {
      color: $dark-blue;
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 10px;
      font-weight: 700;
      line-height: 28px;
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

  .input-wrap {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 20px;
  }

  .input-frame {
    min-width: 80%;
    width: 100%;
    border: 1px solid lightgray;
    padding: 10px;
    margin-bottom: 10px;
  }

  .input-btn {
    background-color: $primary-green;
    color: $white;
    font-size: 14px;
    font-weight: 500;
    padding: 10px;
    border-radius: 5px;
    cursor: pointer;
    width: 100%;
    text-align: center;
    &:hover {
      background-color: rgb(63, 159, 71);
      transition: 0.2s;
    }
    &:active {
      background-color: grey;
      transition: 0.1s ease-in-out;
    }
  }
}
</style>
