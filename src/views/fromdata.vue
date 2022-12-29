
<template>
  <p></p>
<div class="container">
  <form>
    <h1 class="alert alert-success">Belajar From dan Vie event</h1>
    <p>Nama </p>
    <input v-model="nama" type="text" class="form-text">
    <!-- <p>masukan nama</p> -->
    <p>Nim</p>
    <input v-model="nim" type="text" class="form-text">
    <p>Email</p>
    <input v-model="email" type="text" class="form-text">
    <div class="mt-2">
    <button class="btn btn-info btn-md" type="submit" @click.prevent="simpanData">Simpan</button>
    </div>
  </form>
</div>



<table class="table">
  <thead>
    <tr>
      <th>Nama</th>
      <th>Nim</th>
      <th>email</th>
    </tr>
  </thead>
  <tbody>
    <tr :key="item.nama"  v-for="item in dataMahasiswa">
      <td>{{ item.nama }}</td>
      <td>{{ item.nim }}</td>
      <td>{{ item.email }}</td>
    </tr>
  </tbody>

</table>

</template>

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