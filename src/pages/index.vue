<template>
  <div class="page">
    <Header :activeIndex="1" />

    <main class="main">
      <section-1 />
      <section-2 />
      <etc />

      <section class="placeholder">
        <h2>Next: Section-2 (Scroll Toggle)</h2>
      </section>
    </main>
  </div>
</template>

<script>
import Header from "@/components/header.vue";
import Section1 from "@/components/section-1.vue";
import Section2 from "@/components/section-2.vue";
import Etc from "@/components/etc.vue";

export default {
  name: "IndexPage",

  components: {
    Header,
    "section-1": Section1,
    "section-2": Section2,
    etc: Etc,
  },
};
</script>

<style scoped lang="scss">
.page {
  min-height: 100vh;
  background: #0a0c0e;
  color: #eaeef5;
}

.main {
  padding-top: 76px; /* offset header fixed */
}

.placeholder {
  max-width: 1120px;
  margin: 0 auto;
  padding: 40px 18px;
}
</style>
