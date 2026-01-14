<template>
  <section class="notes" id="sec-3">
    <div class="container">
      <h2 class="h2">Submission Notes</h2>
      <p class="p">
        This project recreates the scroll-toggle interaction using Vue 2
        (Options API), SASS, and GSAP ScrollTrigger with a pinned scrub section.
      </p>

      <div class="grid">
        <div class="card">
          <div class="card-title">Tech Stack</div>
          <ul>
            <li>Vue 2 (Options API) via Vue CLI</li>
            <li>SASS (no Tailwind)</li>
            <li>GSAP + ScrollTrigger</li>
          </ul>
        </div>

        <div class="card">
          <div class="card-title">Implemented</div>
          <ul>
            <li>Responsive layout (desktop/tablet/mobile)</li>
            <li>Pinned section + scrub animations</li>
            <li>Step switching (Plan / Walls / Code)</li>
          </ul>
        </div>

        <div class="card">
          <div class="card-title">Bonus (optional)</div>
          <ul>
            <li>ScrollToPlugin for header navigation</li>
            <li>Image optimization via srcset/sizes (if enabled)</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "EEtc",
};
</script>

<style scoped lang="scss">
.notes {
  background: #0a0c0e;
  border-top: 1px solid rgba(255, 255, 255, 0.08);
  padding: 80px 0;
}

.container {
  max-width: 1120px;
  margin: 0 auto;
  padding: 0 18px;
}

.h2 {
  margin: 0 0 10px;
  font-size: 34px;
}

.p {
  margin: 0 0 22px;
  opacity: 0.82;
  max-width: 760px;
}

.grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 14px;
}

.card {
  border: 1px solid rgba(255, 255, 255, 0.1);
  background: rgba(255, 255, 255, 0.04);
  border-radius: 16px;
  padding: 16px;
}

.card-title {
  font-weight: 700;
  margin-bottom: 10px;
}

ul {
  margin: 0;
  padding-left: 18px;
  opacity: 0.88;
}

@media (max-width: 900px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
</style>
