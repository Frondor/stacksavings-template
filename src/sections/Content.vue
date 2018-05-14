<template>
  <main class="container-fluid" id="content">
    <div class="row">
      <div class="col-xs-12 col-md-5" id="featured">
        <card class="bg-white"
          v-for="n in 2" :key="n"
          title="Some cool title goes here"
          img="http://placehold.it/300">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium at distinctio impedit, aperiam velit repellendus incidunt ipsa quidem iste.
          <a class="btn" slot="footer">
            Go in
          </a>
        </card>
      </div>
      <div class="col-xs-12 col-md-7">
        <card v-for="n in 3" :key="n"
          title="Some cool title goes here"
          img="http://placehold.it/300"
          panorama flat >
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium at distinctio impedit, aperiam velit repellendus incidunt ipsa quidem iste.
          <a class="btn" slot="footer">
            Go in
          </a>
        </card>
      </div>
    </div>
  </main>
</template>

<script>
import Card from '../components/card'

export default {
  components: { Card }
}
</script>
