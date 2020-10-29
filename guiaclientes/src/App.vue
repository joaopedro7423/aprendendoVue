<template>
  <div id="app">
    <h3>Cadastro</h3>
    <input type="text" placeholder="nome" v-model="nomeField"><br>
    <input type="email" placeholder="email" v-model="emailField"><br>
    <input type="number" placeholder="idade" v-nome="idadeField"><br> 
    <button @click="cadastrarUsuarios">Cadastrar</button>   


    <div v-for="(cliente,index) in clientes" :key="cliente.id">
      <h1>{{index}}</h1>
     <Cliente :cliente="cliente"/>
      <input type="text" v-model="cliente.nome">
    </div>
   
     </div>
</template>

<script>
import Cliente from './components/Cliente'

export default {
    name:'App',
    data(){
      return{
          nomeField:"",
          emailField:"",
          idadeField:0,
      clientes:[
        {
          id:1,
          nome:"JOOJ PEREIRA",
          email:"jooj@jooj.saa",
          idade: 99
        },{
          id:2,
 nome:"JOOJ PEREIR2A",
          email:"jooj2@jooj.saa",
          idade: 992
        },{
          id:3,
 nome:"JOOJ PEREI213R2A",
          email:"jooj3212@jooj.saa",
          idade: 992132
        }
      ]
          }
},
    components:{
      Cliente
    },
    methods:{
      cadastrarUsuarios: function(){
        this.clientes.push({nome: this.nomeField,email: this.emailField, idade: this.idadeField, id:Date.now()})
        this.nomeField="";
        this.emailField="";
        this.idadeField=0;
      }
    }
}
</script>

<style>
</style>
