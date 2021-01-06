<template>
  <div class="v-cart-items">
    <h3>Корзина</h3>
    <v-cart-item
      v-for="(item, index) in cart_data"
      :key="item.article"
      :cart_item_data="item"
      @deleteFromCart="deleteFromCart(index)"
    />
  </div>
</template>

<script>
import vCartItem from "./v-cart-item";
import { mapActions } from "vuex";

export default {
  name: "v-cart",
  components: {
    vCartItem,
  },
  props: {
    cart_data: Array,
    default() {
      return [];
    },
  },
  data() {
    return {};
  },
  computed: {},
  methods: {
    ...mapActions(["DELETE_FROM_CART"]),
    deleteFromCart(index) {
      this.DELETE_FROM_CART(index);
    },
  },
  watch: {},
  mounted() {},
};
</script>

<style scoped>
</style>temlate>