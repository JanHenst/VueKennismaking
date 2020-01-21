<template>
    <div class="book-item" v-bind:class="{'is-complete':book.completed}">
        <h2>
            {{book.title}}
        </h2>
        <p>
            <button @click="$emit('del-book', book.id)" class="del">X</button>
            <img v-bind:src="book.image">
        </p>
        <p class="description">
            {{book.description}}
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
    img {
        width: 150px;
    }

    .description {
        float: right;
        padding-bottom: 1em;
    }
</style>