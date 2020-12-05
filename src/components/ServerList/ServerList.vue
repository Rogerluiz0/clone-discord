<template>
  <div class="container-serverList">
    <ServerButton isHome/>
    <hr id="separator">
    <ServerButton hasNotification :mentions="32"/>
    <ServerButton/>
    <ServerButton hasNotification :mentions="9"/>
    <ServerButton hasNotification :mentions="56"/>
    <ServerButton/>
    <ServerButton hasNotification v-for="server in 2" :key="server.id"/>
    <ServerButton v-for="server in 3" :key="server.id"/>
    <ServerButton hasNotification :mentions="43"/>
    <ServerButton/>
    <ServerButton hasNotification :mentions="8"/>
  </div>
</template>

<script>
  import ServerButton from './ServerButton/ServerButton.vue'

  export default {
    components: {
      ServerButton
    }
  }
</script>

<style src="./style.scss" lang="scss" scoped></style>