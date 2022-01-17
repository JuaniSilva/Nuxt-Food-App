<template>
  <nav>
    <ul>
      <li>
        <nuxt-link exact to="/"><AppLogo /></nuxt-link>
      </li>
      <li><nuxt-link to="/restaurants">Restaurants</nuxt-link></li>
    </ul>
    <div v-if="totalItems > 0" class="smallnum">{{ totalItems }}</div>
    <nuxt-link to="/cart">cart</nuxt-link>
  </nav>
</template>

<script>
import AppLogo from "@/components/AppLogo.vue";
import { mapGetters } from "vuex";

export default {
  components: {
    AppLogo,
  },
  computed: {
    ...mapGetters(["totalItems"]),
  },
};
</script>

<style lang="scss" scoped></style>
