<template>
  <div class="ChannelInfo">
    <img src="../../assets/pound.svg" id="HashTag">
    <h1 class="title">chat-livre</h1>
    <div class="separator"></div>
    <div class="description">Canal aberto para conversas</div>
  </div>
</template>

<script>
  export default {
    name: 'ChannelInfo'
  }
</script>

<style lang="scss" scoped>
  .ChannelInfo {
    grid-area: ChannelInfo;
    
    background-color: var(--primary);
    
    display: flex;
    align-items: center;
    padding: 0 17px;
    z-index: 2;
    box-shadow: rgba(0,0,0,0.9) 0 1px 0 0;

    #HashTag {
      width: 24px;
      height: 24px;
    }

    .title {
      color: var(--white);
      font-size: 16px;
      margin-left: 9px;
      font-weight: bold;
    }

    .separator {
      background-color: var(--white);
      width: 1px;
      height: 24px;
      opacity: 0.2;
      margin: 0 13px;
    }

    .description {
      color: var(--grey);
      font-size: 15px;
    }
  }
</style>