<template>
  <div class="contact">
    <div class="row d-flex">
      <div class="col-6 col-md-4 col-lg-3">
        <img src="~/assets/img/seba.jpg" />
      </div>
      <div class="col-10 col-md-5 col-lg-4 py-3">
        <h2>Get in Touch</h2>
        <p>I am currently accepting commission, collaborative or project work. If you are interested in working with me, or if you have any questions, please do not hesitate to contact me directly by <a class="blue" href="mailto:w_carrera@sebastiandesign.ca">email</a>, or through my social channels below.</p>
        <ul>
          <li>
            <a href="https://www.linkedin.com/in/waltersebastiancarrera/" target="_blank" rel="noopener noreferrer">
              <span><font-awesome-icon :icon="['fab', 'linkedin']"/></span>
            </a>
          </li>
          <li>
            <a href="https://github.com/sebastianbydesign/" target="_blank" rel="noopener noreferrer">
              <span><font-awesome-icon :icon="['fab', 'github-square']"/></span>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss">

.contact {
  .row {
    min-height: 100vh;
    background-color: $gray;
    align-items: center;
    justify-content: center;
    @media (max-width: 767px) {
      align-content: center;
      align-items: baseline;
      padding-top: 50px;
    }
    img {
      width: 100%;
    }
    h2 {
      font-family: $axis-b;
      font-size: 1.35rem;
      color: $blue;
    }
    p, a {
      font-family: $lato-m;
      font-size: 1rem;
      color: white;
    }
    ul {
      list-style: none;
      padding: 0;
      li {
        display: inline-block;
        a {
          padding: 0px 10px 0 0;
          &:hover {
            color: $blue !important;
            text-decoration: none;
          }
          svg {
            height: 25px;
          }
        }
      }
    }
    .blue {
      color: $blue;
    }
  }
}

</style>
