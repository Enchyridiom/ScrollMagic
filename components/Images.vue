<template>
    <div>
        <img :src="source" alt="demo">
    </div>
</template>

<script>
export default{
    props: ["source", "demo"]
}
</script>

<style>
</style>