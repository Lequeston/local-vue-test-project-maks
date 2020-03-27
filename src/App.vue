<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="sass">
  *
    margin: 0
    padding: 0
    font-family: Geometria,Arial,sans-serif

  .anim-enter-active
    transition: opacity 10s
  .anim-enter-active, .fade-leave-active
      transition: opacity 2s
</style>
