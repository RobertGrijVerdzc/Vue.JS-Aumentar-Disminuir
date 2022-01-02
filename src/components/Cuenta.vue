<template>
  <h1>Tipo de Cuenta: {{tipo}} </h1>
  <h2>{{ saldo }}</h2>
  <div v-for="(servicio, index) in  servicios" :key="index">
      {{ index + 1 }} - {{ servicio }}
  </div>
  <AccionSaldo texto="Aumentar"  @accion="aumentar()" />
  <AccionSaldo texto="Dismunuir"  @accion="menosaldo()" :desactivar="desactivar"/>
</template>

<script>


import AccionSaldo from './AccionSaldo.vue'

export default {
    name: 'Cuenta',
     components: {
         AccionSaldo,
    },
    data() {
        return {
            saldo: 1000,
            tipo: 'visa',
            estado: true,
            servicios: [
                'giro',
                'abono',
                'transferencias'
            ],
            desactivar: false

        }
    },
    methods: {
        aumentar(){
                this.saldo = this.saldo + 100,
                this.desactivar = false
        },
        menosaldo(){
            if(this.saldo >= 100){
                this.saldo = this.saldo - 100
            } else{
                this.desactivar = true,
                console.log("Saldo negativo");
            }
        }
    },
}
</script>
    
<style>

</style>