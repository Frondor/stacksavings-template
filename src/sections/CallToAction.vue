<template>
  <section class="row text-center">
    <div class="container position-relative" ref="container">
      <h2 class="mt-5 mb-4">Do you like what you see?</h2>
      <form class="offset-md-2 col-md-8 mb-4">
        <div class="form-row">
          <div class="col-12 col-md-9 mb-2 mb-md-0">
            <input type="email" class="form-control form-control-lg" name="email" placeholder="Your e-mail...">
          </div>
          <div class="col-12 col-md-3">
            <button type="submit" class="btn btn-block btn-lg btn-primary">
              Join us!
           </button>
         </div>
       </div>
     </form>
    </div>
  </section>
</template>

<script>
import ScrollReveal from 'scrollreveal'
export default {
  mounted () {
    const sr = new ScrollReveal({
      duration: 750,
      mobile: true
    })
    this.$nextTick(() => {
      sr.reveal(this.$refs.container)
    })
  }
}
</script>

<style lang="sass">
section
  background: url('/stacksavings-template/static/hero.jpg') center center no-repeat
  background-attachment: fixed
  min-height: 250px
  position: relative
  color: #FFF
  font-weight: bold

  &:before
    content: ''
    background: rgba(16, 0, 37, 0.32)
    position: absolute
    height: 100%
    width: 100%
</style>
