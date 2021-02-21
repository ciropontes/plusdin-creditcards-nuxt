<template>
  <md-toolbar class="toolbar-main">
    <a class="brand-logo" href="/">
      <img src="../assets/images/logo-plusdin.svg" />
    </a>

    <div class="md-toolbar-section-end">
      <div>
        <a href="/">
          <md-button>Melhores cartões</md-button>
        </a>
      </div>
    </div>
  </md-toolbar>
</template>

<script>
export default {
  name: "NavBar",
  props: [],
  data() {
    return {};
  },
  components: {},
  methods: {
    sair() {
      this.$store.commit("setUsuario", null);
      sessionStorage.clear();
      this.$router.push("/login");
    },
  },
  created() {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.brand-logo {
  width: 50%;
}
.toolbar-main {
  margin-bottom: 20px;
}
@media only screen and (max-width: 600px) {
  .md-toolbar-section-end {
    flex-direction: column;
  }
}
</style>
