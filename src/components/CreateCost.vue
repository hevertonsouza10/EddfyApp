<script setup>
import { ref } from 'vue';


const nestedRouteItems = ref([
    {
        label: 'Identificação de Custo',
        to: '/uikit/menu'
    },
    {
        label: 'Valores e Prazos',
        to: '/uikit/menu/seat'
    },
    {
        label: 'Informações Adicionais',
        to: '/uikit/menu/payment'
    },
    {
        label: 'Confirmação de Reg',
        to: '/uikit/menu/confirmation'
    }
]);


</script>

<template>
    <div class="grid p-fluid">

        <div class="col-12 md:col-20dw">
            <div class="card card-w-title">
                <h5>Novo Custo</h5>
                <Steps :model="nestedRouteItems" :readonly="false" />
                <router-view />
            </div>
        </div>
    </div>
</template>
