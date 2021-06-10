<template>
  <div class="ChannelList">
    <section>
      <div class="category">
        <div>Geral</div>
        <img src="../../assets/plus.svg" id="addCategoryIcon">
      </div>

      <ChannelButton selected channelName="chat"/>
      <ChannelButton channelName="links"/>
    </section>

    <section>
      <div class="category">
        <div>Techs</div>
        <img src="../../assets/plus.svg" id="addCategoryIcon">
      </div>

      <ChannelButton channelName="HTML"/>
      <ChannelButton channelName="CSS"/>
      <ChannelButton channelName="Javascript"/>
      <ChannelButton channelName="Sass"/>
      <ChannelButton channelName="Vuejs"/>
      <ChannelButton channelName="Nodejs"/>
    </section>

    <section>
      <div class="category">
        <div>Vagas</div>
        <img src="../../assets/plus.svg" id="addCategoryIcon">
      </div>

      <ChannelButton channelName="Front-end"/>
      <ChannelButton channelName="Back-end"/>
      <ChannelButton channelName="Full-Stack"/>
      <ChannelButton channelName="UI/UX"/>
    </section>

    <section>
      <div class="category">
        <div>Canais de voz</div>
        <img src="../../assets/plus.svg" id="addCategoryIcon">
      </div>

      <ChannelButton channelName="bate-papo"/>
      <ChannelButton channelName="lives"/>
    </section>
  </div>
</template>

<script>
  import ChannelButton from './ChannelButton.vue'
  
  export default {
    name: 'ChannelList',

    components: {
      ChannelButton
    }
  }
</script>

<style lang="scss" scoped>
  .ChannelList {
    grid-area: ChannelList;

    display: flex;
    flex-direction: column;
    
    overflow-y: scroll;
    padding: 24px 10px 0 16px;

    background-color: var(--secondary);

    section+section {
      margin-top: 20px;
    }

    section:last-child { 
      margin-bottom: 20px;
    }

    &::-webkit-scrollbar {
      display: none;
    }

    .category {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 6px;
      color: var(--grey);
      font-size: 12px;
      font-weight: 500;
      text-transform: uppercase;
    }

    #addCategoryIcon {
      width: 21px;
      height: 21px;
      cursor: pointer;
    }
  }
</style>