<template>
  <div class="container-ChannelMessage" :class="{ 'has-mention':hasMention }">
    <div class="avatar" :class="{ 'bot-avatar':isBot }"></div>
    <div class="message">
      <div class="user">
        <strong>{{ author }}</strong>
        <span class="bot" v-if="isBot">Bot</span>
        <span class="date">{{ date }}</span>
      </div>
      <div class="body">
        <slot />
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      author: String,
      date: String,
      hasMention: Boolean,
      isBot: Boolean
    }
  }
</script>

<style src="./style.scss" lang="scss" scoped></style>