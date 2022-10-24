<template>
  <section
    class="p-0 bg-img cover-background"
    style="background-image: url(https://bootdey.com/img/Content/bg1.jpg)"
  >
    <div class="container-fluid d-flex flex-column">
      <div class="row align-items-center justify-content-center min-vh-100">
        <div class="col-md-9 col-lg-6 my-5">
          <div class="text-center error-page">
            <h1 class="mb-0 text-secondary">404</h1>
            <h2 class="mb-4 text-white">Sorry, something went wrong!</h2>
            <p class="w-sm-80 mx-auto mb-4 text-white">
              This page is incidentally inaccessible because of support. We will
              back very before long much obliged for your understanding
            </p>
            <NuxtLink to="/">
              <button type="button" class="btn btn-outline-primary">
                Back to Home
              </button>
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
body {
  margin-top: 20px;
}
.cover-background {
  position: relative ;
  background-size: cover ;
  overflow: hidden ;
  background-position: center ;
  background-repeat: no-repeat ;
}
.p-0 {
  padding: 0 ;
}
section {
  padding: 120px 0;
  overflow: hidden;
  background: #fff;
}

.error-page {
  background-color: #bababa4a;
  -webkit-backdrop-filter: blur(9px);
  backdrop-filter: blur(15px);
  border: 1px solid rgba(234, 234, 235, 0.2);
  padding: 80px 20px;
}
.text-center {
  text-align: center;
}
.error-page h1 {
  font-size: 200px;
  line-height: 1;
  font-weight: 600;
}
.text-secondary {
  color: #15395a ;
}
.mb-4 {
  margin-bottom: 1.5rem ;
}
</style>
