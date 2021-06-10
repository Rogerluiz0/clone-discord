<template>
  <span class="mention"> <slot/> </span>
</template>

<script>
  export default {
    name: 'Mention'
  }
</script>

<style lang="scss" scoped>
.mention {
  color: var(--link);
  cursor: pointer;

  &:hover {
    text-decoration: underline;
  }
}
</style>