<template>
  <div>
    <what-is-this :key="componentKey"></what-is-this>
  </div>
</template>

<script>
export default {
  name: "WhatIsThisView",

  data() {
    return {
      componentKey: 0
    };
  },
  computed: {
    serverStatus: function() {
      return this.$store.state.serverStatus;
    },
    BaseUrl: function() {
      return this.$store.state.baseurl;
    }
  },
  watch: {
    BaseUrl: function() {
      this.componentKey += 1;
    }
  }
};
</script>
