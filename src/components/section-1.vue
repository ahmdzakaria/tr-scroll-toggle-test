<template>
  <section class="hero" id="sec-1">
    <div class="bg"></div>
    <div class="content">
      <p class="kicker">Scroll Toggle</p>
      <h1 class="h1">Build a smooth scroll toggle</h1>
      <p class="p">
        Recreate the reference interaction using Vue 2 (Options API), SASS, and
        GSAP ScrollTrigger.
      </p>

      <div class="row">
        <div class="pill">Responsive</div>
        <div class="pill">Pinned</div>
        <div class="pill">Scrub</div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SectionOne",
};
</script>

<style scoped lang="scss">
.hero {
  position: relative;
  min-height: calc(100vh - 76px);
  display: grid;
  align-items: center;
  overflow: hidden;
}

.bg {
  position: absolute;
  inset: 0;
  background-image: url("~@/assets/images/wendy-1080.jpg"); /* ganti jika nama beda */
  background-size: cover;
  background-position: center;
  transform: scale(1.06);
  filter: saturate(0.95) contrast(1.05);
}

.bg::after {
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(
    180deg,
    rgba(10, 12, 14, 0.55),
    rgba(10, 12, 14, 0.92)
  );
}

.content {
  position: relative;
  z-index: 1;
  max-width: 1120px;
  margin: 0 auto;
  padding: 80px 18px;
}

.kicker {
  font-size: 12px;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  opacity: 0.85;
  margin: 0 0 14px;
}

.h1 {
  font-size: clamp(36px, 5vw, 64px);
  line-height: 1.03;
  margin: 0 0 12px;
}

.p {
  max-width: 650px;
  font-size: 16px;
  opacity: 0.84;
  margin: 0;
}

.row {
  margin-top: 18px;
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.pill {
  border: 1px solid rgba(255, 255, 255, 0.12);
  background: rgba(255, 255, 255, 0.05);
  padding: 8px 12px;
  border-radius: 999px;
  font-size: 12px;
  opacity: 0.92;
}
</style>
