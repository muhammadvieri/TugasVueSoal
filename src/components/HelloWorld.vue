<template>
  <div>
    <h1>{{ nama }}</h1>
    <input type="text" v-model="nama">
    <br><br>
    Nilai Anda : {{ nilai }}
    <br>    
    <h2>{{ soal1 }}</h2>
    <input type="radio" name="jawaban1" :disabled="checked" > Komnas anti kekerasan terhadap perempuan
    <input type="radio" name="jawaban1" :disabled="checked" @click="benar"> Pengadilan tata Negara
    <input type="radio" name="jawaban1" :disabled="checked"> Pengadilan HAM
    <h2>{{ soal2 }}</h2>
    <input type="radio" name="jawaban2" :disabled="checked2"> Jimmy Carter
    <input type="radio" name="jawaban2" :disabled="checked2"> Lyndon Johnson
    <input type="radio" name="jawaban2" :disabled="checked2" @click="benar2"> John F. Kennedy
    <h2>{{ soal3 }}</h2>
    <input type="radio" name="jawaban3" :disabled="checked3" @click="benar3"> Javascript
    <input type="radio" name="jawaban3" :disabled="checked3" > Python
    <input type="radio" name="jawaban3" :disabled="checked3"> Java
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      nama: 'Nama Anda',
      nilai: 0,
      soal1: '1. Berikut ini yang tidak termasuk lembaga peradilan HAM yaitu ... ',
      soal2: '2. Siapa Presiden Amerika Serikat Yang Tewas Dibunuh?',
      soal3: '3. Bahasa Pemrograman Yang Berbasis Web'
    }
  },
  methods:{
    benar(){
      this.nilai += 1,
      this.checked = true
    },
     benar2(){
      this.nilai += 1,
      this.checked2 = true
    },
     benar3(){
      this.nilai += 1,
      this.checked3 = true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
  font-size: 30px;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
