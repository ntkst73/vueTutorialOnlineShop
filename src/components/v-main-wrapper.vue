<template>
  <div class="v-main-wrapper">
    <keep-alive>
      <router-view></router-view>
    </keep-alive>
  </div>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  name: "v-main-wrapper",
  props: {},
  data() {
    return {};
  },
  methods: {},
  watch: {},
};
</script>

<style scoped>
.v-main-wrapper {
  margin: 0 auto;
}
</style>