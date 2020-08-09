<template>

    <StackLayout class='todo-item'
        v-bind:class="{'is-complete':todo.completed}">

        <GridLayout columns="100,*,100" backgroundColor="white">

            <check-box :checked="true" @checkedChange="isChecked = $event.value"  col="0"/>
            <Label text="todo" width="*" height="50" col="1"
                backgroundColor="green" />
            <button @click="" class="del" col="2">x</button>
        </GridLayout>
    </StackLayout>

</template>

<script>
    export default {
        name: "TodoItem",
        props: ["todo"],
        methods: {
            markComplete() {
                this.todo.completed = !this.todo.completed;
            }
        }
    };
</script>

<style scoped>
    .todo-item {
        background: #f4f4f4;
        padding: 10px;
        border-bottom: 1px #cc dotted;
    }

    .is-complete {
        text-decoration: line-through
    }

    .del {
        background: #ff0000;
        color: #fff;
        border: none;
        padding: 4px 9px;
        border-radius: 50%;
        cursor: pointer;
        float: right;
    }

    .listItem {
        padding: 20;
        padding-left: 50;
        font-size: 20;
        background-color: white;
    }
</style>