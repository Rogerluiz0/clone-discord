<template>
  <div class="container-ChannelButton" :class="{ 'active':selected }">
    <div class="channel-info">
      <img src="../../../assets/pound.svg" id="HashTagIcon">
      <div>{{ channelName }}</div>
    </div>
    <div class="channel-actions">
      <img src="../../../assets/account-plus.svg" id="InviteIcon">
      <img src="../../../assets/cog-outline.svg" id="SettingsIcon">
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      channelName: String,
      selected: Boolean
    }
  }
</script>

<style src="./style.scss" lang="scss" scoped></style>