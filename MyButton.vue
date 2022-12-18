<template>
<button class="btn">
    <slot></slot>
</button>
</template>

<script>
export default{
    name:'my-button'
}
</script>



<style>
.btn{
    padding: 10px 15px;
    background: none;
    border: 3px solid rgb(158, 166, 224);
    color: rgb(158, 166, 224);
}
</style>