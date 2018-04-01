<template lang="pug">
  .admin
    .header
      app-header
    .tabs
      tabs
    .content
      router-view
</template>

<script>
import header from './components/header';
import tabs from './components/tabs';

export default {
  components: {
    appHeader: header,
    tabs
  }
};
</script>

<style scoped lang="scss">
.content {
  position: relative;
  background: url('~images/bg.jpg') center center / cover no-repeat;
  padding: 2rem 1.5rem;

  &:before {
    content: ' ';
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    top: 0;
    background-color: #ffffff;
    opacity: 0.85;
  }
}
</style>
