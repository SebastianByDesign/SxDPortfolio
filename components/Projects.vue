<template>
  <div class="projects">
    <div class="section" v-for="project in projects" :key="project.div_id">
      <div class="anchor" :id="project.div_id"></div>
      <div class="row justify-content-center py-2">
        <div class="col-11 col-md-10 col-lg-8">
          <img class="projectImg" :src="project.image.filename + '/m/'" :alt="project.title">
        </div>
      </div>
      <div class="row justify-content-center projectInfo py-3">
        <div class="col-11 col-md-5 col-lg-4 description">
          <h4>{{ project.title }}</h4>
          <h5>- {{ project.category }} -</h5>
          <p class="py-2">{{ project.info }}</p>
        </div>
        <div class="col-11 col-md-5 col-lg-4 software">
          <p>Made Using:</p>
          <ul>
            <li v-for="software in project.software_list" :key="software.name">
              <img class="px-3" :title="software.name" :src="software.image.filename + '/m/'" :alt="software.name">
            </li>
          </ul>
          <div>
            <a class="py-2" v-bind:href="project.div_id + '.pdf'">
              Read More
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
  .section {
    height: 100vh;
    margin-right: -15px;
    margin-left: -15px;
    display: flex;
    flex-direction: column;
    align-content: center;
    justify-content: center;
    .anchor {
      display: block;
      position: relative;
      top: -25vh;
      visibility: hidden;
    }
    .projectImg {
      width: 100%;
    }
    .projectInfo {
      .description {
        h4, h5 {
          font-family: "Lato Medium";
        }
        h4 {
          margin: 0;
        }
        h5 {
          color: #5CA6D7;
        }
        p {
          font-family: "Lato Light";
          font-size: 1.1rem;
        }
      }
      .software {
        text-align: center;
        p {
          font-size: 1.1rem;
          margin-bottom: 10px;
          font-family: "Lato Medium";
        }
        ul {
          display: flex;
          align-items: center;
          justify-content: space-around;
          list-style: none;
          padding: 0;
          li {
            width: 125px;
            img {
              width: 100%;
            }
          }
        }
        div {
          border: 1px solid #5CA6D7;
          &:hover {
            border: 1px solid black;
          }
          a {
            display: inline-block;
            width: 100%;
            text-decoration: none;
            font-family: "Lato Light";
            color: black;
            font-size: 1.1rem;
          }
        }
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