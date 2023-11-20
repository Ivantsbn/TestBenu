<template>
  <div class="wrapper">
    <div class="wrapper-block">
      <div class="footer">
        <a href="#" class="footer-header">Company Info</a>
        <a href="#" class="footer-title">About Us</a>
        <a href="#" class="footer-title">Carrier</a>
        <a href="#" class="footer-title">We are hiring</a>
        <a href="#" class="footer-title">Blog</a>
      </div>
      <div class="footer">
        <a href="#" class="footer-header">Legal</a>
        <a href="#" class="footer-title">About Us</a>
        <a href="#" class="footer-title">Carrier</a>
        <a href="#" class="footer-title">We are hiring</a>
        <a href="#" class="footer-title">Blog</a>
      </div>
      <div class="footer">
        <a href="#" class="footer-header">Features</a>
        <a href="#" class="footer-title">Business Marketing</a>
        <a href="#" class="footer-title">User Analytic</a>
        <a href="#" class="footer-title">Live Chat</a>
        <a href="#" class="footer-title">Unlimited Support</a>
      </div>
      <div class="footer">
        <a href="#" class="footer-header">Resources</a>
        <a href="#" class="footer-title">IOS & Android</a>
        <a href="#" class="footer-title">Watch a Demo</a>
        <a href="#" class="footer-title">Customers</a>
        <a href="#" class="footer-title">API</a>
      </div>
      <div class="footer">
        <div class="footer-header">Get In Touch</div>
        <div class="footer-icon">
          <img src="../assets/bx_bx-phone.png" />
          <div class="footer-text">(480) 555-0103</div>
        </div>
        <div class="footer-icon">
          <img src="../assets/bx_bx-map.png" />
          <a
            href="https://www.google.com/maps/place/Iangar/@37.1536371,-83.7619007,15z/data=!4m6!3m5!1s0x884352a00e70879f:0x1ad06ed33b7003c!8m2!3d37.1536371!4d-83.7619007!16s%2Fg%2F11rs2v5qy5?entry=ttu"
            class="footer-text"
          >
            4517 Washington Ave. Manchester,<br />
            Kentucky 39495
          </a>
        </div>
        <div class="footer-icon">
          <img src="../assets/carbon_send-alt.png" />
          <div class="footer-text">debra.holt@example.com</div>
        </div>
      </div>
    </div>
    <div class="footer-container">
      <div class="footer-near-line">
        <div class="copy-right">
          Made With Love By Figmaland All Right Reserved
        </div>
        <div class="icon">
          <img src="../assets/fb.png" alt="" />
          <img src="../assets/inst.png" alt="" />
          <img src="../assets/twt.png" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="js"></script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "./src/styles/colors.scss";

.wrapper {
  background-color: $white;
  font-family: "Montserrat-Bold", Helvetica;
  &-block {
    display: flex;
    justify-content: space-around;
    margin: 0 220px;
    padding: 50px 0;
  }
}
.footer {
  display: flex;
  flex-direction: column;
  &-container {
    background-color: #fafafa;
    padding: 10px 250px;
  }
  &-header {
    color: $dark-blue;
    font-weight: 700;
    margin-bottom: 15px;
    font-size: 16px;
    line-height: 24px;
    letter-spacing: 0.1px;
    &:hover {
      color: black;
      transition: 0.1s ease-in-out;
    }
  }
  &-title {
    color: $dark-grey;
    text-decoration: none;
    margin-bottom: 10px;
    font-size: 14px;
    line-height: 24px;
    font-weight: 700;
    letter-spacing: 0.2px;
    &:hover {
      color: black;
      transition: 0.1s ease-in-out;
    }
  }
  &-text {
    color: $dark-grey;
    margin-bottom: 10px;
    text-decoration: none;
    margin-left: 10px;
    font-size: 14px;
    line-height: 14px;
    font-weight: 700;
    letter-spacing: 0.2px;
  }
  &-near-line {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
  }
  &-icon {
    display: flex;
    align-items: center;
    margin-bottom: 10px;
    img {
      margin-bottom: 10px;
    }
  }
}
.copy-right {
  color: $dark-grey;
  font-size: 14px;
  font-weight: 700;
  letter-spacing: 0.2px;
  line-height: 24px;
}
.icon {
  display: flex;
  gap: 10px;
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
      margin: 0 20px;
      padding: 20px 0;
    }
  }

  .footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 15px;

    &-container {
      background-color: #fafafa;
      padding: 10px 20px;
    }

    &-header,
    &-title,
    &-text {
      color: $dark-blue;
      text-decoration: none;
      margin-bottom: 5px;
      font-size: 14px;
      line-height: 15px;
      font-weight: 700;
      letter-spacing: 0.2px;
      text-align: center;

      &:hover {
        color: black;
        transition: 0.1s ease-in-out;
      }
    }

    &-near-line {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      width: 100%;
    }

    &-icon {
      display: flex;
      align-items: center;
      margin-bottom: 10px;

      img {
        margin-bottom: 10px;
        max-width: 30px;
      }
    }
  }

  .copy-right {
    color: $dark-grey;
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.2px;
    line-height: 16px;
    text-align: center;
  }

  .icon {
    display: flex;
    gap: 10px;
  }
}
</style>
