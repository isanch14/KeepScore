<template>
  <nav
    class="nav w-screen z-20 text-black"
    :class="ishome ? '' : 'shadow-2xl bg-blue-800'"
  >
    <div class="left">
      <span class="font-light text-3xl">
        <span class="font-semibold">Welcome!</span>
      </span>
    </div>
    <div class="right">
      <router-link class="link" to="/">Home</router-link> |
      <router-link class="link" to="/search">Login</router-link>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
  props: {
    ishome: {
      type: Boolean,
      default: true
    }
  }
};
</script>

<style lang="scss" scoped>
.nav {
  @apply h-24 fixed px-12 flex justify-between items-center;
}
.link {
  @apply px-2 font-semibold;
  &:hover {
    @apply text-purple-800;
  }
}
</style>
