<template>
  <div class="ChannelMessage" :class="{ 'has-mention':hasMention }">
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
    name: 'ChannelMessage',

    props: {
      author: String,
      date: String,
      hasMention: Boolean,
      isBot: Boolean
    }
  }
</script>

<style lang="scss" scoped>
  .ChannelMessage {
    display: flex;
    align-items: center;
    
    padding: 8px 16px;
    margin-right: 4px;
    background-color: transparent;
    margin-top: 13px;

    .avatar {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background-color: var(--secondary);
      flex-shrink: 0;

      &.bot-avatar {
        background-color: var(--mention-detail);
      }
    }

    .message {
      height: 40px;
      margin-left: 17px;

      display: flex;
      flex-direction: column;
      justify-content: space-between;

      .user {
        strong {
          color: var(--white);
          font-size: 16px;
        }

        .bot {
          margin-left: 9px;
          background-color: var(--discord);
          color: var(--white);
          padding: 4px 5px;
          border-radius: 4px;
          text-transform: uppercase;
          font-size: 11px;
          font-weight: bold;
        }

        .date {
          margin-left: 6px;
          color: var(--grey);
          font-size: 13px;
        }
      }

      .body {
        color: var(--white);
        text-align: left;
        font-size: 16px;
      }
    }

    &.has-mention {
      background-color: var(--mention-message);
      border-left: 2px solid var(--mention-detail);
    }

    &:hover {
      background-color: var(--quaternary);
    }
  }
</style>