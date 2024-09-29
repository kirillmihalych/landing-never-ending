<template>
  <div class="scroller">
    <div class="running-line">
      <p>
        Дело помощи утопающим — дело рук самих утопающих! Шахматы двигают вперед не только культуру, но и экономику! Лед
        тронулся, господа присяжные заседатели!
      </p>
      <p>
        Дело помощи утопающим — дело рук самих утопающих! Шахматы двигают вперед не только культуру, но и экономику! Лед
        тронулся, господа присяжные заседатели!
      </p>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@keyframes running-line {
  to {
    transform: translateX(-50%);
  }
}

.scroller {
  width: 100%;
  height: 40px;
  white-space: nowrap;
  text-overflow: clip;
  overflow: hidden;

  position: absolute;
  bottom: 0;
  left: 0;
  background-color: red;
  color: white;

  display: flex;
  align-items: center;
}

.running-line {
  display: flex;
  align-items: center;
  width: max-content;

  animation-name: running-line;
  animation-timing-function: linear;
  animation-duration: 15s;
  animation-iteration-count: infinite;
}
</style>
