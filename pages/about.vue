<template>
  <div class="about">
    <div class="row d-flex">
      <div class="col-6 col-md-4 col-lg-3">
        <img src="~/assets/img/seba.jpg" />
      </div>
      <div class="col-10 col-md-5 col-lg-4 py-3">
        <h2>About Me</h2>
        <p>I am the kind of person that wants to help people and lead them to better places. I pour my heart and soul into everything I do, so that I know that I did my best. These values are at the core of who I am and who I continue to strive to be.</p>
        <p class="m-0">As a designer, I am able to channel my values into my work. Every phase, from planning to implementing, is done with care and with consideration of who the design is for. That is what I believe Interaction Design is all about.</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">

.about {
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
    p {
      font-family: $lato-m;
      font-size: 1rem;
      color: white;
    }
  }
}

</style>
