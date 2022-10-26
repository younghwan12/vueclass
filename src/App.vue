<template>
  <div>
    <HeaderLayout fonts="nexon" />
    <SliderSection />
    <ImageSection attr="section nexon" layout="container" />
    <ImageTextSection attr="nexon section gray" layout="container" />
    <CardSection attr="section nexon" layout="container" />
    <BannerSection fonts="gmark" />
    <TextSection attr="nexon section" layout="container" />
    <FooterLayout attr="nexon section gray" layout="container" />
  </div>
</template>

<script>
import FooterLayout from "./components/layout/FooterLayout.vue";
import HeaderLayout from "./components/layout/HeaderLayout.vue";
import SliderSection from "./components/section/SliderSection.vue";
import ImageSection from "./components/section/ImageSection.vue";
import ImageTextSection from "./components/section/ImageTextSection.vue";
import BannerSection from "./components/section/BannerSection.vue";
import CardSection from "./components/section/CardSection.vue";
import TextSection from "./components/section/TextSection.vue";

export default {
  name: "App",
  components: {
    HeaderLayout,
    FooterLayout,
    BannerSection,
    SliderSection,
    ImageSection,
    ImageTextSection,
    CardSection,
    TextSection,
  },
};
</script>
