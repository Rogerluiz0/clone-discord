<template>
  <div class="UserList">
    <div class="role">Disponível - 2</div>
    <UserRow isBot nickname="Jirem"/>
    <UserRow nickname="Roger"/>
    <UserRow nickname="Jovem Dinâmico"/>
    
    <div class="role">Offline - 22</div>
    <UserRow nickname="Random User" v-for="user in 22" :key="user.id"/>
  </div>
</template>

<script>
  import UserRow from './UserRow.vue'

  export default {
    name: 'UserList',

    components: {
      UserRow
    }
  }
</script>

<style lang="scss" scoped>
  .UserList {
    grid-area: UserList;

    display: flex;
    flex-direction: column;

    padding: 3px 6px 10px 16px;
    max-height: calc(100vh - 46px);
    
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

    background-color: var(--secondary);

    .role {
      margin-top: 20px;
      color: var(--grey);
      font-weight: 500;
      font-size: 12px;
      text-transform: uppercase;
    }
  }
</style>