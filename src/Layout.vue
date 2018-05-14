<template>
  <div id="app">
    <section-header></section-header>
    <section-content></section-content>
    <section-footer></section-footer>
  </div>
</template>

<script>
import SectionHeader from './sections/Header'
import SectionContent from './sections/Content'
import SectionFooter from './sections/Footer'


export default {
  name: 'Layout',
  components: {
    SectionHeader,
    SectionContent,
    SectionFooter
  }
}
</script>
