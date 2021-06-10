<template>
  <div class="UserRow">
    <div class="avatar" :class="{'bot-avatar':isBot}"></div>
    <strong>{{ nickname }}</strong>
    <div class="bot" v-if="isBot">Bot</div>
  </div>
</template>

<script>
  export default {
    name: 'UserRow',

    props: {
      nickname: String,
      isBot: Boolean,
    }
  }
</script>

<style lang="scss" scoped>
  .UserRow {
    display: flex;
    align-items: center;

    cursor: pointer;
    margin-top: 5px;
    padding: 5px;
    border-radius: 5px;
    background-color: transparent;
    transition: 0.2s;

    .avatar {
      width: 32px;
      height: 32px;
      border-radius: 50%;
      flex-shrink: 0;
      background-color: var(--primary);
    }

    strong {
      margin-left: 13px;
      font-weight: 500;
      color: var(--white);
      opacity: 0.7;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
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

    .bot-avatar {
      background-color: var(--mention-detail);
    }

    &:hover {
      background-color: rgba(0,0,0,0.1);
    }
  }
</style>