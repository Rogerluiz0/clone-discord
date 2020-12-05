<template>
  <div class="container-UserList">
    <div class="role">Disponível - 2</div>
    <UserRow isBot nickname="Jirem"/>
    <UserRow nickname="Roger"/>
    <div class="role">Offline - 18</div>
    <UserRow nickname="Luiz" v-for="user in 18" :key="user.id"/>
  </div>
</template>

<script>
  import UserRow from './UserRow/UserRow.vue'

  export default {
    components: {
      UserRow
    }
  }
</script>

<style src="./style.scss" lang="scss" scoped></style>