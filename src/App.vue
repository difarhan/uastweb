<script>
      export default{

        data(){
        return{
          dataMahasiswa:[],
          nama: "",
          nim: "",
          email: ""
        }
      },
        methods:{
          simpanData(){
            var mahasiswa={
              nama:this.nama,
              nim: this.nim,
              email: this.email
            }
            this.dataMahasiswa.push(mahasiswa);
        }
      }
      }
</script>

<template>
  <!-- <div class="container"> -->
    <nav class="navbar navbar-expand-sm navbar-light bg-body">
      <router-link class="nav-item nav-link" to="/"> 
        <a href="#" class="navbar-brand fw-bold mx-4"> 
          <img src ="https://www.freepnglogos.com/uploads/logo-keren-png/radio-skull-drawing-clip-art-10.png"
      width="60" height="60"></a> </router-link>
      
    <button class="navbar-toggler" 
    type="button" 
    data-toggle="collapse" 
    data-target="#navbarNavAltMarkup" 
    aria-controls="navbarNavAltMarkup" 
    aria-expanded="false" 
    aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  
  <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
    <div class="navbar-nav ml-auto"> 
      <router-link class="nav-item nav-link" to="/about">About</router-link>
      <router-link class="nav-item nav-link" to="/coba">Coba</router-link>
    </div>
      <div class="navbar-nav ms-auto"> 
      <router-link class="nav-item nav-link" to="/fromdata">From data</router-link>
      <router-link class="nav-item nav-link" to=""></router-link>
    </div>
  </div>
</nav>
  <router-view/>
  <!-- </div> -->
</template>


<!-- <style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style> -->
