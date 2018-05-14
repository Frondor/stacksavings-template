<template>
  <nav class='navbar navbar-expand-lg navbar-light bg-light'>
    <a class='navbar-brand' href='#'>Navbar</a>
    <button class='navbar-toggler' type='button' @click='toggle'>
      <span class='navbar-toggler-icon'></span>
    </button>

    <div class='navbar-collapse' :class='classes'>
      <ul class='navbar-nav mr-auto mt-2 mt-lg-0'>
        <li class='nav-item active'>
          <a class='nav-link' href='#'>Home <span class='sr-only'>(current)</span></a>
        </li>
        <li class='nav-item'>
          <a class='nav-link' href='#'>Link</a>
        </li>
        <li class='nav-item'>
          <a class='nav-link disabled' href='#'>Disabled</a>
        </li>
      </ul>
      <!-- <form class='form-inline my-2 my-lg-0'>
        <input class='form-control mr-sm-2' type='search' placeholder='Search'>
        <button class='btn btn-outline-success my-2 my-sm-0' type='submit'>Search</button>
      </form> -->
    </div>
  </nav>

</template>

<script>
export default {
  data () {
    return {
      collapsed: true,
      collapsing: false // not implemented
    }
  },
  computed: {
    classes () {
      let classes = this.collapsing ? 'collapsing' : 'collapse'
      if (!this.collapsed) classes += ' show'
      return classes
    }
  },
  methods: {
    toggle () {
      this.collapsed = !this.collapsed
    },
    onEnter () { // not implemented
      this.collapsing = true
    },
    afterEnter () { // not implemented
      this.collapsing = false
    }
  }
}
</script>
