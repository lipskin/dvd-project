<template>
  <header class="app-bar row middle-xs">
      <span class="logo col-xs-10">
        DvD
      </span>
  </header>
</template>

<script>
export default {
  name: 'app-bar',
  data() {
    return {
      msg: '',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.app-bar {
    display: flex;
    height: 65px;
    padding: 5px 30px;
    background-color: #00BCD4;
}
.logo {
    align-self: center;
    color: white;
    font-size: 30px;
    font-weight: bold;
    cursor: pointer;
}
.link {
    color: white;
    font-size: 24px;
    font-weight: 400;
    cursor: pointer;
}
</style>
