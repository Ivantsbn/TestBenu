<template>
  <div class="home">
    <top-header />
    <first-container />
    <second-container />
    <third-container />
    <input-container />
    <footer-section />
  </div>
</template>

<script>
// @ is an alias to /src
import TopHeader from "@/components/TopHeader.vue";
import FirstContainer from "@/components/FirstContainer.vue";
import SecondContainer from "@/components/SecondContainer.vue";
import ThirdContainer from "@/components/ThirdContainer.vue";
import InputContainer from "../components/InputContainer.vue";
import FooterSection from "../components/FooterSection.vue";

export default {
  name: "HomeView",
  components: {
    TopHeader,
    FirstContainer,
    SecondContainer,
    ThirdContainer,
    InputContainer,
    FooterSection,
  },
};
</script>
<style , ThirdContainer, ThirdContainerlang="scss" scoped></style>
