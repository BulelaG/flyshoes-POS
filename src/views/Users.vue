<template>

<!-- CODE for hiding this if not logged in -->




  <div class="users">
    <h1>Users</h1>

 <section id="gallery" style="padding-bottom: 16px">
      <div class="container">
        <div class="row" v-if="users">
          <div
            v-for="(user, index) of users"
            :key="index"
            class="col-lg-4 mb-4"
          >
            <div class="card">
              <img :src="user.img" alt="" class="card-img-top" />
              <div class="card-body">
                <br />
                <h5 class="card-title">{{ user.name }}</h5>
                <p class="card-text">{{ user.id }}</p>
              </div>
              <div class="card-footer">
                <br>
                <small class="text-muted">R{{ user.role }}</small>
              </div>
              
              <br>
              <br>
              
            </div>
          </div>
         
        </div>
      </div>
    </section>


  </div>
</template>

<script >
export default {

// GETT USER CODE HERE !!!!!!!!!!!!!!!!!!!!!!!


   data() {
    return {
      users: [
        {
        img: "https://i.postimg.cc/RVwWvkmR/A-Ma-Maniere-x-Nike-Air-Jordan-3.jpg",
        name: "Nike",
        role: "3500",
      },
       {
        img: "https://i.postimg.cc/RVwWvkmR/A-Ma-Maniere-x-Nike-Air-Jordan-3.jpg",
        name: "Nike",
        role: "3500",
      }

       
      ],
    };
  }



    
}
</script>


<style scoped>

.card {
border: 1px solid ;
  border-radius: 30px;
}

</style>