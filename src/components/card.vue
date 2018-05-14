<template>
  <article class="card-article mb-5 rounded" :class="classes">
    <div class="card-picture">
      <img :src="img" class="img-fluid">
    </div>
    <header class="p-3">
      <h3>{{ title }}</h3>
    </header>
    <p class="p-3">
      <slot />
    </p>
    <footer>
      <slot name="footer" />
    </footer>
  </article>
</template>

<script>
export default {
  props: {
    panorama: Boolean,
    flat: Boolean,
    title: String,
    img: String
  },
  computed: {
    classes () {
      let clss = ''
      if (this.panorama) clss += 'card-horizontal'
      if (!this.flat) clss += 'shadow-lg'
      return clss
    }
  }
}
</script>

<style lang="sass">
.card-article
  overflow: hidden

  &.card-horizontal
    .card-picture
      float: left
      max-width: 10rem
      margin: 2rem
</style>

