<template>
  <div class="container-fluid bg-dark text-white-50">
    <div class="row">
     <div class="col-xs-12 col-md-6 col-lg-7">
      <div class="row">
         <div class="col-xs-6 col-sm-4" v-for="n in 3" :key="n">
           <p class="lead font-weight-light">
             Menu {{ n }}
           </p>
           <ul class="list-unstyled">
             <li v-for="nn in 5" :key="nn">
              <a href="#">Lorem ipsum</a>
             </li>
           </ul>
         </div>
      </div>
     </div>
     <div class="col-xs-12 col-md-6 col-lg-5">
       <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Perspiciatis facere, iste? Consectetur, reprehenderit, cumque? Dolores obcaecati et vitae, porro earum tenetur illo, iste, minima minus expedita repellendus error natus quos.</p>
     </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>
