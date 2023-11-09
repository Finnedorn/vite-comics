<template>
  <header class="bg-my-white">
    <div class="container d-flex justify-content-between py-3">
      <!--logo-->
      <div class="logo-wrapper">
        <img src="/img/dc-logo.png" alt="dc-logo">
      </div>
      <!--navbar-->
      <nav class="navbar navbar-expand-lg">
        <div class="container-fluid">
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarScroll" aria-controls="navbarScroll" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarScroll">
            <ul class="navbar-nav me-auto my-2 my-lg-0 navbar-nav-scroll" style="--bs-scroll-height: 100px;">
              <li class="nav-item nav-font me-4" v-for="(el) in navbarArr">
                <a class="nav-link active" aria-current="page" href="#">{{el}}</a>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderApp",
  components: {
  },
  data() {
    return {
      navbarArr: [
        'CHARACTERS',
        'COMICS',
        'MOVIES',
        'TV',
        'GAMES',
        'COLLECTIBLES',
        'VIDEOS',
        'FANS',
        'NEWS',
        'SHOP'
      ]
    }
  }

};
</script>

<style lang="scss" scoped>
.nav-font {
  font-size: 0.7rem;
  font-weight: bolder;
  transform: scale(1,1.2);
}

</style>
