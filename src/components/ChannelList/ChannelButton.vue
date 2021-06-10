<template>
  <div class="container" :class="{'active':selected}">
    <div class="channel-info">
      <img src="../../assets/pound.svg" id="HashTagIcon">
      <div>{{ channelName }}</div>
    </div>

    <div class="channel-actions">
      <img src="../../assets/account-plus.svg" id="InviteIcon">
      <img src="../../assets/cog-outline.svg" id="SettingsIcon">
    </div>
  </div>
</template>

<script>
  export default {
    name: 'ChannelButton',

    props: {
      channelName: String,
      selected: Boolean
    }
  }
</script>

<style lang="scss" scoped>
  .container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    cursor: pointer;
    padding: 5px 3px;
    border-radius: 5px;
    background-color: transparent;

    > div {
      display: flex;
      align-items: center;
    }

    .channel-info {
      div {
        color: var(--senary);
        margin-left: 5px;
      }

      #HashTagIcon {
        width: 20px;
        height: 20px;
      }
    }

    .channel-actions {
      display: none;

      #InviteIcon, #SettingsIcon {
        width: 16px;
        height: 16px;
        margin-left: 4px;
      }
    }

    &:hover, &.active {
      background-color: var(--quinary);

      .channel-info {
        div {
          color: var(--white);
        }
      }

      .channel-actions {
        display: inline;
      }
    }
  }
</style>