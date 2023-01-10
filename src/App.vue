<script setup>

import { onMounted ,reactive } from 'vue';

import  axios  from 'axios'

const events=reactive([])



onMounted(()=>{

  axios.get('https://kktix.com/events.json')
       .then(response=>{
        return response.data;
       })
       .then(data=>{
          data.entry.forEach(e=>{
            events.push(e)
          })
       })

})


</script>

<template>
<ul>
  <li v-for="e,i in events " :key="i">
    {{ e.author.name }}
  </li>
</ul>
</template>


