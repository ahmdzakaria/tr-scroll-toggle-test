<template>
  <div class="page">
    <Header :activeIndex="1" />

    <main class="main">
      <section class="placeholder">
        <h1>Step 2: Header OK</h1>
        <p>Cek 123</p>
      </section>
    </main>
  </div>
</template>

<script>
import Header from "@/components/header.vue";

export default {
  name: "IndexPage",
  components: { Header },
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
