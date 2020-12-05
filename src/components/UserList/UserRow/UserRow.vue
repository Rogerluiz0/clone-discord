<template>
  <div class="container-UserRow">
    <div class="avatar" :class="{ 'bot-avatar':isBot }"></div>
    <strong>{{ nickname }}</strong>
    <div class="bot" v-if="isBot">Bot</div>
  </div>
</template>

<script>
  export default {
    props: {
      nickname: String,
      isBot: Boolean,
    }
  }
</script>

<style src="./style.scss" lang="scss" scoped></style>