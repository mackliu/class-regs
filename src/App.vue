<script setup>

import { onMounted ,reactive } from 'vue';

import  axios  from 'axios'

const events=reactive([])



onMounted(()=>{

  axios.get('http://220.128.133.15/regs/api/json')
       .then(response=>{

        console.log(response)
       })


})


</script>

<template>
<ul>

</ul>
</template>


