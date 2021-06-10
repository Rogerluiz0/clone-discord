<template>
  <div class="ChannelData">
    <div class="messages">
      <ChannelMessage author="Jovem Dinâmico" date="07/12/2020">
        Alguém pode me ajudar?
      </ChannelMessage>

      <ChannelMessage author="Roger" date="07/12/2020">
        <Mention>Jovem Dinâmico</Mention> Claro
      </ChannelMessage>

      <ChannelMessage author="Roger" date="07/12/2020">
        Do que precisa?
      </ChannelMessage>

      <ChannelMessage hasMention isBot author="Jirem" date="07/12/2020">
        <Mention>Roger</Mention> subiu de nível!
      </ChannelMessage>
    </div>

    <div class="input-wrappeer">
      <input type="text" placeholder="Conversar em #chat-livre">
      <img src="../../assets/at.svg" id="At">
    </div>
  </div>
</template>

<script>
  import ChannelMessage from './ChannelMessage.vue'
  import Mention from './Mention.vue'
  
  export default {
    name: 'ChannelData',

    components: {
      ChannelMessage,
      Mention
    }
  }
</script>

<style lang="scss" scoped>
  .ChannelData {
    grid-area: ChannelData;

    display: flex;
    flex-direction: column;
    justify-content: space-between;

    background-color: var(--primary);
    flex: 1;

    .messages {
      .ChannelMessage:first-child {
        margin-top: 0;
      }

      .ChannelMessage:last-child {
        margin-bottom: 13px;
      }

      display: flex;
      flex-direction: column;
      height: calc(100vh - 46px - 68px);
      max-height: calc(100vh - 46px - 68px);

      overflow-y: scroll;

      &::-webkit-scrollbar {
        width: 8px;
      }

      &::-webkit-scrollbar-thumb {
        background-color: var(--tertiary);
        border-radius: 4px;
      }

      &::-webkit-scrollbar-thumb-track {
        background-color: var(--secondary);
      }
    }

    .input-wrappeer {
      width: 100%;
      height: 68px;
      padding: 0 16px;
      
      input {
        width: 100%;
        height: 44px;
        padding: 0 10px 0 57px;
        border-radius: 5px;
        color: var(--white);
        background-color: var(--chat-input);
        position: relative;

        &::placeholder {
          color: var(--grey);
        }
      }

      #At {
        width: 24px;
        height: 24px;
        position: relative;
        top: -50%;
        left: 14px;
      }
    }
  }
</style>