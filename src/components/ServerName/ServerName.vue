<template>
  <div class="ServerName">
    <div class="title">Roger's Server</div>
    <img src="../../assets/chevron-down.svg" id="ExpandIcon">
  </div>
</template>

<script>
  export default {
    name: 'ServerName'
  }
</script>

<style lang="scss" scoped>
  .ServerName {
    grid-area: ServerName;

    display: flex;
    align-items: center;
    justify-content: space-between;

    background-color: var(--secondary);
    padding: 0 11px 0 16px;
    box-shadow: rgba(0,0,0,0.9) 0 1px 0 0;
    z-index: 2;

    .title {
      color: var(--white);
      font-size: 16px;
      font-weight: bold;
    }

    #ExpandIcon {
      width: 28px;
      height: 28px;
      cursor: pointer;
    }
  }
</style>