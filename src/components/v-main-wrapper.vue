<template>
  <div class="v-main-wrapper">
    <v-catalog></v-catalog>
    <v-cart v-if="CART.length" :cart_data="CART"></v-cart>
  </div>
</template>

<script>
import vCatalog from "./v-catalog";
import vCart from "./v-cart";
import { mapGetters } from "vuex";

export default {
  name: "v-main-wrapper",
  components: {
    vCatalog,
    vCart,
  },
  props: {},
  data() {
    return {
    };
  },
  computed: {
    ...mapGetters(["CART"])
  },
  methods: {},
  watch: {},
  mounted() {
    console.log("Hello word");
  },
};
</script>

<style scoped>
.v-main-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  max-width: 900px;
  margin: 0 auto;
}
</style>