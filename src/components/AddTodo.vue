<template>
<!--@author Isac Canedo-->
    <div>
        <br>
        <div class="add">
            <form @submit="onSubmit">
                <input type="text" v-model="title" placeholder="Adicionar NOVO..." />
                <input type="submit" value="Criar" />
            </form>
        </div>
    </div>
</template>

<script>
import { mapActions } from 'vuex';
export default {
    name: 'AddTodo',
    data() {
        return {
            title: ''
        }
    },
    methods: {
        ...mapActions(['addTodo']),
        onSubmit(e) {
            e.preventDefault();
            this.addTodo(this.title);
        }
    }
}
</script>

<style scoped>
    form { display: flex; }
    input[type="text"] {
        flex: 10;
        padding: 10px;
        border: 1px solid #41b883;
        outline: none;
    }

    input[type="submit"] {
        flex: 2;
        background-color: #41b883;
        color: #fff;
        border: 1px #41b883;
        cursor: pointer;
    }
</style>
