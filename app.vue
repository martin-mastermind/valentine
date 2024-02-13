<template>
  <NuxtPage />
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Pangolin&family=Roboto:wght@100;300;400;500;700;900&display=swap");

* {
  box-sizing: border-box;
  outline: none;
  padding: 0;
  margin: 0;
}

body {
  width: 100vw;
  height: 100vh;
  overflow: hidden;

  font-family: "Pangolin", cursive;
  font-weight: 500;
}
</style>

<style>
.page-enter-active,
.page-leave-active {
  transition: 0.3s ease-in-out;
}
.page-enter-from,
.page-leave-to {
  opacity: 0;
}
</style>
