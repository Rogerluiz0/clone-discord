<template>
  <div class="container-serverButton" :class="{ 'serverButton-isHome':isHome, 'serverButton-hasNotification':hasNotification }">

    <img src="../../../assets/discord.svg" v-if="isHome">
    <div class="mentions" v-if="mentions"> {{ mentions }} </div>
  </div>
</template>

<script>
  export default {
    props: {
      selected: Boolean,
      isHome: Boolean,
      hasNotification: Boolean,
      mentions: Number
    }
  }
</script>

<style src="./style.scss" lang="scss" scoped></style>