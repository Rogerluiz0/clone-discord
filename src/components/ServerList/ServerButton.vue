<template>
  <div class="ServerButton" :class="{'serverButton-isHome':isHome, 'serverButton-hasNotification':hasNotification}">

    <img src="../../assets/discord.svg" v-if="isHome">
    <div class="mentions" v-if="mentions">{{ mentions }}</div>
  </div>
</template>

<script>
  export default {
    name:'ServerButton',
    
    props: {
      selected: Boolean,
      isHome: Boolean,
      hasNotification: Boolean,
      mentions: Number
    }
  }
</script>

<style lang="scss" scoped>
  .ServerButton {
    width: 48px;
    height: 48px;

    margin-bottom: 8px;
    background-color: var(--primary);
    cursor: pointer;
    position: relative;
    border-radius: 50%;

    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;

    transition: .2s;

    &.active, &:hover {
      border-radius: 16px;
      background-color: var(--discord);
    }

    img {
      width: 24px;
      height: 24px;
      color: #FFF;
    }

    .mentions {
      width: auto;
      height: 24px;
      background-color: var(--notification);
      padding: 0 4px;
      position: absolute;
      bottom: -4px;
      right: -4px;
      border: 4px solid var(--quaternary);
      border-radius: 12px;
      text-align: right;
      font-size: 13px;
      font-weight: bold;
      color: var(--white);
    }
  }

  .serverButton-isHome {
    border-radius: 16px;
    background-color: var(--discord);

    &.active, &:hover {
      background-color: var(--discord);
    }  
  }

  .serverButton-hasNotification {
    &::before {
      content: '';
      width: 9px;
      height: 9px;
      background-color: var(--white);
      position: absolute;
      left: -17px;
      top: calc(50% - 4.5px);
      border-radius: 50%;
      display: block;
    }
  }
</style>