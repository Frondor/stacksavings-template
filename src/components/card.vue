<template>
  <article class="card-article mb-5 p-0 rounded" :class="classes">
    <div class="card-picture" :style="imgRight ? {float: 'right'} : {}">
      <a href="#">
        <img :src="img" class="img-fluid">
      </a>
    </div>
    <header class="m-0 mt-4">
      <h3 class="m-0 pl-3 pr-3">{{ title }}</h3>
    </header>
    <p class=" pl-3 pr-3 pt-2" v-if="$slots.default">
      <small>
        {{ $slots.default[0].text.slice(0, 100) + '...' }}
      </small>
    </p>
    <footer class="pl-3 pr-3 pt-2 blockquote-footer">
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
    img: String,
    imgRight: Boolean
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
  header
    margin-top: 2rem
</style>

