<script>
export default {

  data() {
    return {
      
      menuItems: [
        {
          label: "Home",
          routeName: "home",
        },
        {
          label: "Ristoranti",
          routeName: "Restaurants",
        },
        {
          label: "Contattaci",
          routeName: "ContactUs",
        },


      ],
    };
  },
}

</script>
<template>
  <!-- <nav class="navbar navbar-expand-md navbar-light shadow-sm bg-body-tertiary d_flex introduction sticky-top  "
    style="background-color: #ef5117ff;">
    <div class="container d-flex justify-content-between">
      <div class="left-side">

       
        <router-link to="/home" class="navbar-brand d-flex align-items-center"><img src="/logo/4.png" alt=""
            class="logo"></router-link>

        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent" aria-expanded="false">
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav ml-auto ">
            <li class="nav-item  " v-for="(item, index) in menuItems" :key="index">


              <router-link :to="{ name: item.routeName }" class="nav-link nav-i text-white  ">
                {{ item.label }}
              </router-link>
            </li>
          </ul>
        </div>


        <ul>
            <li class="nav-item dropdown text-white navbar-nav ">
              <a class="nav-link dropdown-toggle text-white" href="#" role="button" data-bs-toggle="dropdown"
                aria-expanded="false">
                                  Benvenutə, (Nome Utente)
                                </a>
                                <ul class="dropdown-menu" style="background-color: #ef5117ff;">
             
                                  <li><router-link to="/dashboard" class="nav-link active text-white">Dashboard</router-link></li>
              
                                  <li><router-link to="/user.show" class="nav-link active text-white">Il tuo profilo</router-link></li>
                                  <li>
                                    <hr class="dropdown-divider" />
                                  </li>
                                  <li>
            
                                    <router-link to="/userLogin" class="nav-link active text-white">Logout</router-link>
                                  </li>

                                </ul>
                              </li>
                            </ul>
                          </div>
                          <div class="right-side ">
                            <ul>
                              <li><router-link to="/cart" class="nav-link active text-white" style=""><i
                                    class="fa-solid fa-cart-shopping"></i></router-link></li>
                            </ul>
                          </div>
                        </div>


                      </nav> -->


  <nav class="navbar navbar-expand-lg  bg-body-tertiary d_flex introduction sticky-top px-2 col-sm-12"
    style="background-color: #ef5117ff;">
    <div class="container-fluid">
      <a :href="'/'" class="navbar-brand d-flex align-items-center me-3"><img src="/logo/4.png" alt=""
          class="logo"></a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item animation" v-for="(item, index) in menuItems" :key="index">

            <router-link :to="{ name: item.routeName }" class="nav-link nav-i text-white  ">
              {{ item.label }}
            </router-link>
          </li>

        </ul>
        <div class="d-flex">
          <div class="me-4">
            <ul class="list-unstyled">
              <li class="nav-item animation">
                
                  <a class="nav-link text-white" href="http://localhost:8000/login" role="button">
                    Accedi
                  </a>
                
              </li>
            </ul>
          </div>
          <div>
            
              <a class="nav-item text-white animation" href="http://localhost:8000/register" role="button">Registrati</a>
          
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<style lang="scss">
.animation {
  position: relative;
  display: inline-block;
  text-decoration: none;
}

.animation::before,
.animation::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: 0;
  background-color: white;
  transition: all 0.3s ease-in-out;
}

.animation::before {
  left: 0;
}

.animation::after {
  right: 0;
}

.animation:hover::before,
.animation:hover::after {
  width: 50%;
}

.logo {
  object-fit: contain;
}
</style>