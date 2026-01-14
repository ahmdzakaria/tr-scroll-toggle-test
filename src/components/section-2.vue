<template>
  <section class="toggle" id="sec-2">
    <div class="container">
      <div class="grid">
        <!-- LEFT -->
        <div class="left">
          <p class="kicker">Scroll Toggle</p>
          <h2 class="h2">Plan → Walls → Code</h2>
          <p class="desc">
            Ini versi statis dulu. Setelah layout rapi, baru pasang GSAP
            ScrollTrigger (pin + scrub).
          </p>

          <div class="steps">
            <button
              type="button"
              class="step"
              :class="{ active: activeStep === 0 }"
              @click="activeStep = 0"
            >
              <img class="icon" :src="planIcon" alt="plan" />
              <div class="text">
                <div class="t">Plan</div>
                <div class="d">Structure components & layout.</div>
              </div>
            </button>

            <button
              type="button"
              class="step"
              :class="{ active: activeStep === 1 }"
              @click="activeStep = 1"
            >
              <img class="icon" :src="wallsIcon" alt="walls" />
              <div class="text">
                <div class="t">Walls</div>
                <div class="d">Responsive UI with SASS.</div>
              </div>
            </button>

            <button
              type="button"
              class="step"
              :class="{ active: activeStep === 2 }"
              @click="activeStep = 2"
            >
              <img class="icon" :src="codeIcon" alt="code" />
              <div class="text">
                <div class="t">Code</div>
                <div class="d">Smooth animations with GSAP.</div>
              </div>
            </button>
          </div>
        </div>

        <!-- RIGHT -->
        <div class="right">
          <div class="frame">
            <img class="img" :src="images[activeStep]" alt="visual" />
            <div class="overlay"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import planIcon from "@/assets/images/plan.svg";
import wallsIcon from "@/assets/images/icon.svg";
import codeIcon from "@/assets/images/code.svg";

// ⚠️ GANTI sesuai nama file yang benar di folder assets/images kamu
import imgPlan from "@/assets/images/wendy-1080.jpg";
import imgWalls from "@/assets/images/walls-1080.jpg";
import imgCode from "@/assets/images/cotton-1080.jpg";

export default {
  name: "SectionTwo",
  data() {
    return {
      activeStep: 0,
      planIcon,
      wallsIcon,
      codeIcon,
      images: [imgPlan, imgWalls, imgCode],
    };
  },
};
</script>

<style scoped lang="scss">
.toggle {
  background: #0a0c0e;
  border-top: 1px solid rgba(255, 255, 255, 0.08);
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
}

.container {
  max-width: 1120px;
  margin: 0 auto;
  padding: 80px 18px;
}

.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 28px;
  align-items: center;
}

.kicker {
  font-size: 12px;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  opacity: 0.85;
  margin: 0 0 10px;
}

.h2 {
  font-size: 38px;
  margin: 0 0 12px;
}

.desc {
  margin: 0 0 18px;
  opacity: 0.82;
  max-width: 520px;
}

.steps {
  display: grid;
  gap: 12px;
  margin-top: 14px;
}

.step {
  text-align: left;
  display: grid;
  grid-template-columns: 34px 1fr;
  gap: 12px;
  padding: 14px;
  border-radius: 14px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  background: rgba(255, 255, 255, 0.04);
  color: #eaeef5;
  cursor: pointer;
}

.step:hover {
  background: rgba(255, 255, 255, 0.06);
}

.step.active {
  border-color: rgba(139, 255, 176, 0.55);
  box-shadow: 0 0 0 3px rgba(139, 255, 176, 0.12);
}

.icon {
  width: 28px;
  height: 28px;
}

.t {
  font-weight: 700;
  margin-bottom: 4px;
}

.d {
  opacity: 0.82;
  font-size: 14px;
}

.frame {
  position: relative;
  width: 100%;
  aspect-ratio: 4 / 5;
  border-radius: 18px;
  overflow: hidden;
  border: 1px solid rgba(255, 255, 255, 0.12);
  background: rgba(255, 255, 255, 0.03);
}

.img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(
    180deg,
    rgba(10, 12, 14, 0.05),
    rgba(10, 12, 14, 0.58)
  );
}

@media (max-width: 900px) {
  .grid {
    grid-template-columns: 1fr;
  }
  .frame {
    aspect-ratio: 16 / 10;
  }
}
</style>
