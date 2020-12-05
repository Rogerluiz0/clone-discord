<template>
  <div class="container-ChannelData">
    <div class="messages">
      <ChannelMessage isBot author="Jirem" date="07/12/2020">
        Esta é uma mensagem de Teste
      </ChannelMessage>
      <ChannelMessage author="Jovem Dinâmico" date="07/12/2020" v-for="message in 7" :key="message.id">
        Esta é uma mensagem de Teste
      </ChannelMessage>
      <ChannelMessage hasMention isBot author="Jirem" date="07/12/2020">
        <Mention>Roger</Mention> eu sou melhor do que você em tudo
      </ChannelMessage>
      <ChannelMessage author="Roger" date="07/12/2020">
        <Mention>Jirem</Mention> quem é você?
      </ChannelMessage>
    </div>
    <div class="input-wrappeer">
      <input type="text" placeholder="Conversar em #chat-livre">
      <img src="../../assets/at.svg" id="At">
    </div>
  </div>
</template>

<script>
  import ChannelMessage from './ChannelMessage/ChannelMessage.vue'
  import Mention from './Mention/Mention.vue'

  export default {
    components: {
      ChannelMessage,
      Mention
    }
  }
</script>

<style src="./style.scss" lang="scss" scoped></style>