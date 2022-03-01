<template>
   <div>
     <h1>PRODUCTS</h1>

 <!-- category -->
    <div class="container d-flex justify-content-end mb-3 mt-5 pt-4">
      <div class="d-flex w-25 ms-3">
        <label for="" class="form-label">Sort by category</label>
        <select
          class="form-select"
          name=""
          id="sortCategory"
          onchange="sortCategory()"
        >
        <option  style="color: goldenrod;" value="Nike">Nike</option>
        <option style="color: goldenrod;" value="Adidas">Adidas</option>
        <option style="color: goldenrod;" value="New Balance">New Balance</option>
        <option style="color: goldenrod;" value="Asics">Asics</option>
        </select>
      </div>
      <div class="d-flex w-25 ms-3">
        <label for="" class="form-label">Sort name</label>
        <select class="form-select" name="" id="sortName" onchange="sortName()">
          <option value="ascending">Ascending</option>
          <option value="descending">Descending</option>
        </select>
      </div>
      <div class="d-flex w-25 ms-3">
        <label for="" class="form-label">Sort price</label>
        <select
          class="form-select"
          name=""
          id="sortPrice"
          onchange="sortPrice()"
        >
          <option value="ascending">Ascending</option>
          <option value="descending">Descending</option>
        </select>
      </div>
    </div>
    <div id="products" class="container d-flex"></div>

<br>

    

    <section id="gallery" style="padding-bottom: 16px">
      <div class="container">
        <div class="row" v-if="products">
          <div
            v-for="(product, index) of products"
            :key="index"
            class="col-lg-4 mb-4"
          >
            <div class="card">
              <img :src="product.image" alt="" class="card-img-top" />
              <div class="card-body">
                <br />
                <h5 class="card-title">{{ product.title }}</h5>
                <p class="card-text">{{ product.description }}</p>
              </div>
              <div class="card-footer">
               <!-- github link ----------------------------------------->
                <button
                  type="button"
                  class="btn btn-muted btn-lg px-4 gap-3"
                  target="_blank"
                >
                  <a style="color: rgb(76, 86, 88)" 
                    ><i
                      class="bi bi-github"
                      style="font-size: 1em; padding-bottom: 400px"
                      >Github link</i
                    ></a
                  >
                </button>

             <!--netlify link ---------------------------------------- -->
                 <button
                  type="button"
                  class="btn btn-muted btn-lg px-4 gap-3"
                  target="_blank"
                >
                  <a style="color: rgb(76, 86, 88)" target="_blank" 
                    ><i
                      class="bi bi-github"
                      style="font-size: 1em; padding-bottom: 400px"
                      >Netlify link</i
                    ></a
                  >
                </button>
                <br>

                <small class="text-muted">{{ product.color }}</small>
              </div>
              
              <br>
              <br>
              <!-- <div class="card-body">
        <h5 class="card-title">Sunset</h5>
        <p class="card-text">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ut eum similique repellat a laborum, rerum voluptates ipsam eos quo tempore iusto dolore modi dolorum in pariatur. Incidunt repellendus praesentium quae!</p>
       <a href="" class="btn btn-outline-success btn-sm">Read More</a>
        <a href="" class="btn btn-outline-danger btn-sm"><i class="far fa-heart"></i></a>
      </div> -->
            </div>
          </div>
          <!-- <div class="col-lg-4 mb-4">
  <div class="card">
      <img src="../assets/NeededFiles/BMI.png" alt="" class="card-img-top">
       <div class="card-body">
            <h5 class="card-title">Carousels Practice</h5>
            <p class="card-text">This is a task where we practised carousels and modals.</p>
          </div>
          <div class="card-footer"><button type="button" class="btn btn-muted btn-lg px-4 gap-3">
            <a style="color: rgb(76, 86, 88);" href="https://github.com/BulelaG/carousels" target="_blank"><i  class="bi bi-github" style="font-size: 2em;padding-bottom: 400px;"></i></a>
           </button>
            <small class="text-muted">Last updated a week ago</small>
          </div>
     
      </div>
    </div>
    <div class="col-lg-4 mb-4">
    <div class="card">
      <img src="../assets/NeededFiles/carousel.png" alt="" class="card-img-top">
      <div class="card-body">
            <h5 class="card-title">Mock Portfolio</h5>
            <br>
            <p class="card-text">First ever portfolio created with Html and Css </p>
            
          </div>
          <div class="card-footer">
            <button type="button" class="btn btn-muted btn-lg px-4 gap-3">
              <a style="color: rgb(76, 86, 88);" href=" https://github.com/BulelaG" target="_blank"><i  class="bi bi-github" style="font-size: 2em;padding-bottom: 400px;"></i></a>
             </button>
            <small class="text-muted">Last updated 3 weeks ago</small>
          </div>

    
     </div>
    </div> -->
        </div>
      </div>
    </section>

    </div>
</template>

<script >
export default {

    
}
</script>

<style scoped>
#products {
  flex-wrap: wrap;
}

#products img {
  height: 300px;
  object-fit: contain;
}

.card {
  width: calc(100% / 4);
  margin-bottom: 10px;
  margin-right: 5px;
}

</style>