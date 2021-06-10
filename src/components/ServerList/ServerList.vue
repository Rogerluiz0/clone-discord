<template>
  <div class="ServerList">
    <ServerButton isHome/>
    <hr id="separator">
    <ServerButton hasNotification :mentions="32"/>
    <ServerButton hasNotification v-for="server in 2" :key="server.id"/>
    <ServerButton/>
  </div>
</template>

<script>
  import ServerButton from './ServerButton.vue'
  export default {
    name: 'ServerList',

    components: {
      ServerButton
    }
  }
</script>

<style lang="scss" scoped>
  .ServerList {
    grid-area: ServerList;

    background-color: var(--tertiary);
    padding: 11px 0;
    max-height: 100vh;

    overflow-y: scroll;

    &::-webkit-scrollbar {
      display: none;
    }

    display: flex;
    flex-direction: column;
    align-items: center;

    hr {
      width: 32px;
      height: 2px;
      border-bottom: 2px solid;
      color: var(--quaternary);
      margin-bottom: 8px;
    }
  }
</style>