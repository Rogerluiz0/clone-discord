<template>
  <div class="UserInfo">
    <div class="profile">
      <div class="avatar">
        <div class="user-data">
          <strong>Roger</strong>
          <span>#2152</span>
        </div>
      </div>
    </div>

    <div class="actions">
      <img src="../../assets/microphone.svg" id="Microphone">
      <img src="../../assets/headphones.svg" id="HeadPhones">
      <img src="../../assets/cog-outline-two.svg" id="Settings">
    </div>
  </div>
</template>

<script>
  export default {
    name: 'UserInfo'
  }
</script>

<style lang="scss" scoped>
  .UserInfo {
    grid-area: UserInfo;

    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 10px;
    background-color: var(--quaternary);
    box-shadow: rgba(0,0,0,0.2) 0 1px 0 0;

    .profile {
      display: flex;
      align-items: center;

      .avatar {
        width: 32px;
        height: 32px;
        border-radius: 50%;
        background-color: var(--grey);

        .user-data {
          display: flex;
          flex-direction: column;
          margin-left: 40px;
          font-size: 13px;

          strong {
            display: block;
            color: var(--white);
          }

          span {
            color: var(--grey);
          }
        }
      }
    }

    .actions {
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;

      #Microphone, #HeadPhones, #Settings {
        width: 20px;
        height: 20px;
        margin-left: 1.5px;
        margin-right: 1.5px;
      }
    }
  }
</style>