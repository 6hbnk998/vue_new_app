<template>
<form @submit.prevent>
            <h4>Создание поста</h4>
            <input v-bind:value="post.title" @input="post.title = $event.target.value" class="input" type="text" placeholder="Название">
            <input v-bind:value="post.body" @input ="post.body = $event.target.value" class="input" type="text" placeholder="Описание">
            <my-button 
            class="btn" 
            style="align-self:flex-end; margin-top: 15px;"
            @click="createPost"
            >
            Создать
        </my-button>
        </form>
</template>

<style>
form{
    display: flex;
    flex-direction: column;
}
.input{
    width: 100%;
    border: 3px solid rgb(158, 166, 224);
    padding: 10px 15px;
    margin-top: 15px;
}

</style>


<script>
import MyButton from '@/components/UI/MyButton'
export default{
    components:{
        MyButton
    },
    data(){
        return{
            post:{
                title:'',
                body:'',
            }
        }
    },
    methods:{
        createPost(){
            this.post.id = Date.now();
            this.$emit('create',this.post)
            this.post={
                title:'',
                body:''
            }
        },
    }
}
</script>