<template>

    <StackLayout class='todo-item' v-bind:class="{'is-complete':task.completed}">

        <GridLayout columns="100,*,100" backgroundColor="white">

            <check-box :checked="task.completed" @checkedChange="markComplete($event.value)"  col="0"/>
            <StackLayout width="*" height="50" col="1" >
                <StackLayout>
                     <Label :text="task.title" backgroundColor="green" />
                </StackLayout>
                <StackLayout>
                     <Label :text="task.datetime" backgroundColor="green" />
                </StackLayout>
            </StackLayout>
           
            <button class="del" col="2">x</button>
        </GridLayout>
    </StackLayout>

</template>

<script>
    export default {
        name: "TodoItem",
        props: ["task"],
        methods: {
            markComplete(state) {
                this.task.completed = state;
            }
        }
    };
</script>

<style scoped>
    .todo-item {
        background: #f4f4f4;
        padding: 10px;
        border-bottom: 1px #ccc dotted;
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