<template>
  <header class="header">
    <div class="wrap">
      <div class="brand">
        <span class="dot"></span>
        <span class="title">tr-scroll-toggle</span>
      </div>

      <nav class="nav">
        <button
          type="button"
          class="btn"
          :class="{ active: activeIndex === 1 }"
          @click="$emit('jump', 1)"
        >
          Intro
        </button>
        <button
          type="button"
          class="btn"
          :class="{ active: activeIndex === 2 }"
          @click="$emit('jump', 2)"
        >
          Toggle
        </button>
        <button
          type="button"
          class="btn"
          :class="{ active: activeIndex === 3 }"
          @click="$emit('jump', 3)"
        >
          Notes
        </button>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  props: {
    activeIndex: { type: Number, default: 1 },
  },
};
</script>

<style scoped lang="scss">
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 76px;
  z-index: 1000;
  background: rgba(10, 12, 14, 0.75);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
}

.wrap {
  max-width: 1120px;
  margin: 0 auto;
  height: 100%;
  padding: 0 18px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.brand {
  display: flex;
  align-items: center;
  gap: 10px;
  font-weight: 700;
  letter-spacing: 0.3px;
}

.dot {
  width: 10px;
  height: 10px;
  border-radius: 99px;
  background: #8bffb0;
}

.nav {
  display: flex;
  gap: 10px;
}

.btn {
  border: 1px solid rgba(255, 255, 255, 0.12);
  background: rgba(255, 255, 255, 0.05);
  color: #eaeef5;
  padding: 10px 14px;
  border-radius: 12px;
  cursor: pointer;
}

.btn:hover {
  background: rgba(255, 255, 255, 0.08);
}

.btn.active {
  border-color: rgba(139, 255, 176, 0.55);
  box-shadow: 0 0 0 3px rgba(139, 255, 176, 0.12);
}

@media (max-width: 640px) {
  .btn {
    padding: 10px 12px;
  }
}
</style>
