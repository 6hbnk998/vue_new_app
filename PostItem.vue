<template>
<div class="post">
    <div>
    <div><strong>Название:</strong>{{post.title}}</div> 
    <div><strong>Описание:</strong>{{post.body}}</div> 
</div>
<div class="post__btn">
<my-button>Удалить</my-button>
</div>
</div>
</template>

<script>

export default{
    props:{
        post:{
            type:Object,
            required:true,
        }
    }
}
</script>

<style>
.post{
    padding: 15px;
    border: 3px solid rgb(180, 186, 230);
    margin: 15px 1px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>