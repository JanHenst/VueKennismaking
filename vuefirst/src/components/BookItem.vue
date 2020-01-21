<template>
    <div class="book-item" v-bind:class="{'is-complete':book.completed}">
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{book.title}}
            <button @click="$emit('del-book', book.id)" class="del">X</button>
        </p>
    </div>
</template>

<script>
export default {
    name: "BookItem",
    props: ["book"],
    methods: {
        markComplete() {
            this.book.completed = !this.book.completed
        }
    }
}
</script>

<style scoped>
    .book-item {
        background: #f4f4f4;
        padding: 10px;
        border-bottom: 1px #ccc dotted;
    }

    .is-complete {
        text-decoration: line-through;
    }

    .del {
        background: #ff0000;
        color: #fff;
        border: none;
        padding: 5px 9px;
        border-radius: 50%;
        cursor: pointer;
        float: right;
    }
</style>