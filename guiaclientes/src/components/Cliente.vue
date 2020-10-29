<template>
        <div :class="{'cliente': !isPremium,'cliente-premium': isPremium}" >
      <!--  <input type="text" v-model="nome">
                <hr>
                <input type="text" v-model="descricao">
        <h2 id="cliente-nome">Cliente : {{nome}}</h2>
        <h3>Descrição : {{descricao}}</h3>
  
        <h4>Nome: {{cliente.nome}}</h4>
        <hr>
        <p>{{descricao}}</p>
        <hr>
        <p>Número: {{numero}}</p>
        <p>Email: {{cliente.email}}</p>
        <p>Idade :{{cliente.idade}}</p>
        <p v-if="showIdade == true">Idade :{{cliente.idade}}</p>
  -->

        <h4>Nome: {{cliente.nome}}</h4>
        <hr>
        
        <p>Email: {{cliente.email}}</p>
         <p>Idade: {{cliente.idade}}</p>
        <button @click="mudarCor($event)">Mudar Cor</button>
    </div>
</template>

<script>
export default {
        data(){
                return{
                     isPremium: false
                     //   numero:"24",
                      
                   //     descricao:"era um maluco muito doido",
                     //   idade:20
                }
                
        },props:{
                 //nome: String,
                 //email: String,
                 //idade: Number,
                 cliente: Object,
                 showIdade:Boolean    
                },
                methods:{
                        mudarCor: function($event){
                                console.log($event);
                                this.isPremium = !this.isPremium;
                           /*if(this.isPremium == false){
                                      this.isPremium = true;
                              }else{
                                        this.isPremium = false;  
                              }
                              */
                        }
                }
}
</script>

<style scoped>
        .cliente{
               background-color: #ECE5E3;
                max-width: 600px;
                height: 250px;
                padding: 1%;
                margin-top: 2%;
        }

        .cliente-premium{
                background-color: black;
                color: yellow;
                max-width: 600px;
                height: 250px;
                padding: 1%;
                margin-top: 2%;
        }

       
</style>