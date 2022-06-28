<template>
  <div class="row" id="home">
    <div class="previewTile col-12 col-lg-4" v-for="project in projects" :key="project.div_id">
      <a class="previewLink" v-bind:href="'#' + project.div_id">
        <div class="box d-flex justify-content-center align-content-center">
          <img class="previewImg" :src="project.image.filename + '/m/'" :alt="project.title">
        </div>
      </a>
    </div>
  </div>
</template>

<style lang="scss">
  #home {
    padding-top: 50px;
  }
  .previewTile {
    overflow: hidden;
    img{
      -webkit-transition: all 0.5s ease;
         -moz-transition: all 0.5s ease;
           -o-transition: all 0.5s ease;
          -ms-transition: all 0.5s ease;
              transition: all 0.5s ease;
      &:hover{
        margin-right: 5px;
      }
    }
  }
</style>

<script>
export default {
  props: {
    blok: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      projects : this.blok.project_list
    }
  }
}
</script>