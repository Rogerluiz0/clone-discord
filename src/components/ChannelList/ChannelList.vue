<template>
  <div class="container-ChannelList">
    <section>
      <div class="category">
        <div>Geral</div>
        <img src="../../assets/plus.svg" id="addCategoryIcon">
      </div>
      <ChannelButton selected channelName="chat-livre"/>
      <ChannelButton channelName="dúvidas"/>
      <ChannelButton channelName="apresentação"/>
      <ChannelButton channelName="links"/>
      <ChannelButton channelName="projetos"/>
    </section>
    <section>
      <div class="category">
        <div>Techs</div>
        <img src="../../assets/plus.svg" id="addCategoryIcon">
      </div>
      <ChannelButton channelName="html"/>
      <ChannelButton channelName="css"/>
      <ChannelButton channelName="Javascript"/>
      <ChannelButton channelName="Sass"/>
      <ChannelButton channelName="Vuejs"/>
      <ChannelButton channelName="Nodejs"/>
      <ChannelButton channelName="electron"/>
      <ChannelButton channelName="mongo"/>
      <ChannelButton channelName="postgresql"/>
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
  import ChannelButton from './ChannelButton/ChannelButton.vue'

  export default {
    components: {
      ChannelButton
    }
  }
</script>

<style src="./style.scss" lang="scss" scoped></style>