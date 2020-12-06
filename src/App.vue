<template>
  <div id="app">
    <div>
      <head-banner></head-banner>
    </div>

    <div>
      <div class="container-fluid">
        <section-api></section-api>
      </div>
    </div>

    <div>
      <aditional-section></aditional-section>
    </div>

    <div>
      <team-card></team-card>
    </div>

    <div>
      <footer-page></footer-page>
    </div>
  </div>
</template>

<script>
import HeadBanner from "./components/HeadBanner.vue";
import SectionApi from "./components/SectionApi.vue";
import AditionalSection from "./components/AditionalSection.vue";
import TeamCard from "./components/TeamCard.vue";
import FooterPage from "./components/FooterPage.vue";

export default {
  name: "App",
  components: {
    HeadBanner,
    SectionApi,
    AditionalSection,
    TeamCard,
    FooterPage,
  },
};
</script>

