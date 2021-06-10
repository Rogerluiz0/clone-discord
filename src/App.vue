<template>
  <div id="container">
    <ServerList/>
    <ServerName/>
    <ChannelList/>
    <UserInfo/>
    <ChannelInfo/>
    <ChannelData/>
    <UserList/>
  </div>
</template>

<script>
  import ServerList from './components/ServerList/ServerList.vue'
  import ServerName from './components/ServerName/ServerName.vue'
  import ChannelList from './components/ChannelList/ChannelList.vue'
  import UserInfo from './components/UserInfo/UserInfo.vue'
  import ChannelInfo from './components/ChannelInfo/ChannelInfo.vue'
  import ChannelData from './components/ChannelData/ChannelData.vue'
  import UserList from './components/UserList/UserList.vue'

  export default {
    name: 'App',
    components: {
      ServerList,
      ServerName,
      ChannelList,
      UserInfo,
      ChannelInfo,
      ChannelData,
      UserList
    }
  }
</script>

<style lang="scss">
  #container {
    height: 100vh;
    display: grid;
    grid-template-columns: 71px 240px auto 240px;
    grid-template-rows: 46px auto 52px;
    grid-template-areas:
    "ServerList ServerName ChannelInfo ChannelInfo"
    "ServerList ChannelList ChannelData UserList"
    "ServerList UserInfo ChannelData UserList";
  }
</style>
