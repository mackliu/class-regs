<script setup>

import { onMounted ,reactive } from 'vue';

import  axios  from 'axios'

const events=reactive([])



onMounted(()=>{

  axios.get('https://wda.mackliu.com/regs/api/json')
       .then(response=>{

        console.log(response)
       })


})


</script>

<template>
<ul>

</ul>
</template>


