<template>
  <div class="custom-layout">
    <Nav />
    Other Layout using component:
    <slot />
  </div>
</template>

<style>
.custom-layout {
  font-size: 50%;
  background: black;
}
</style>
