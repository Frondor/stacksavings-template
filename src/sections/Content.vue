<template>
  <main class="container-fluid" id="content">
    <div class="row">
      <div class="col-xs-12 col-md-5" id="featured">
        <div class="row">
          <card v-for="n in 2" :key="n"
            title="Some short title goes here..."
            :img="`/static/feature-${n}.jpg`"
            class="bg-white col-xs-12 col-sm-6 col-md-12">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium at distinctio impedit, aperiam velit repellendus incidunt ipsa quidem iste.
            <div slot="footer" class="text-center pb-4">
              <a href="#" class="btn btn btn-lg btn-primary">
                Read more
              </a>
            </div>
          </card>
        </div>

      </div>
      <div class="col-xs-12 col-md-7">
        <card v-for="n in 4" :key="n"
          title="Some short title goes here..."
          :img="`/static/caption-${n}.jpg`"
          panorama flat :img-right="n % 2 === 0">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium at distinctio impedit, aperiam velit repellendus incidunt ipsa quidem iste.
          <template slot="footer">
            <a href="#">Read more...</a>
          </template>
        </card>
      </div>
    </div>

    <call-to-action />

    <div class="row captions">
      <div class="col" v-for="n in 2" :key="n">
        <figure>
          <img :src="`/static/stack-${n}.jpg`" class="img-fluid">
          <figcaption>
            <h2>{{ n % 2 ? 'Front' : 'Back'}} <span>End</span></h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
            <a href="javascript:;">Read more</a>
          </figcaption>
        </figure>
      </div>
    </div>
  </main>
</template>

<script>
import CallToAction from './CallToAction'
import Card from '../components/card'
import ScrollReveal from 'scrollreveal'

export default {
  components: { CallToAction, Card },
  mounted () {
    const sr = ScrollReveal({
      duration: 750,
      delay: 300,
      useDelay: 'onload',
      mobile: true
    })
    sr.reveal('.card-article')
  }
}
</script>
