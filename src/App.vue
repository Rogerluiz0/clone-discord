<template>
  <div id="container-main">
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

<style src="./styles/app.scss" lang="scss" scoped></style>