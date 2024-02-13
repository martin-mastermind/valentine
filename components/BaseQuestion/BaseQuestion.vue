<template>
  <section class="base-question">
    <div class="base-question__body">
      <img class="base-question__body-img" :src="questionImg" />
      <span class="base-question__body-text">
        <NuxtLink to="/love-you">ТЫ</NuxtLink> абобус?
      </span>
      <div class="base-question__body-buttons">
        <button
          ref="yesBtn"
          class="base-question__body-buttons--item"
          @mouseenter="runAway('yes')"
        >
          Да
        </button>
        <button
          ref="noBtn"
          class="base-question__body-buttons--item"
          @mouseenter="runAway('no')"
        >
          Нет
        </button>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import questionImg from "~/assets/question.gif";

const yesPos = ref({
  x: "0px",
  y: "0px",
});
const noPos = ref({
  x: "0px",
  y: "0px",
});

const runAway = (button: "yes" | "no") => {
  const randX = Math.floor(
    Math.random() * 800 * (Math.round(Math.random()) ? 1 : -1)
  );
  const randY = Math.floor(
    Math.random() * 200 * (Math.round(Math.random()) ? 1 : -1)
  );

  const ref = button === "yes" ? yesPos : noPos;

  ref.value.x = randX + "px";
  ref.value.y = randY + "px";
};
</script>

<style scoped lang="scss">
.base-question {
  --yes-x: v-bind("yesPos.x");
  --yes-y: v-bind("yesPos.y");
  --no-x: v-bind("noPos.x");
  --no-y: v-bind("noPos.y");
}
</style>

<style scoped lang="scss" src="./BaseQuestion.scss" />
