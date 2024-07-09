<script setup>
    const {data} = await useFetch('/api/habit')
    console.log(data)
</script>
<template>
    <h1>habit</h1>
    <pre>{{ data }}</pre>

</template>