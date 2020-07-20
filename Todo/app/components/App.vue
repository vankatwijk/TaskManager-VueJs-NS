<template>
    <Page class="page" actionBarHidden="true">

        <GridLayout columns="*" rows="auto, *, auto"
            backgroundColor="lightgray">

            <Label text="My Task" class="title" row="0"
                backgroundColor="white" />
            <ScrollView orientation="vertical" row="1"
                backgroundColor="orange">


                <StackLayout orientation="vertical"
                    backgroundColor="lightgray">

                        <TodoItem v-for="x in 50" v-bind:todo="x"
                            v-on:del-todo="" />

                </StackLayout>

            </ScrollView>
            <StackLayout orientation="horizontal">

            </StackLayout>

            <GridLayout columns="*,*,*,*" row="2" backgroundColor="white">
                <Label text="p1" width="*" height="50" col="0"
                    backgroundColor="red" />
                <Label text="p2" width="*" height="50" col="1"
                    backgroundColor="green" />
                <Label text="p3" width="*" height="50" col="2"
                    backgroundColor="blue" />
                <Button text="+" class="addButton" @tap="onAddButtonTap"
                    col="3" />
            </GridLayout>

        </GridLayout>
    </Page>
</template>

<script>
    import TodoItem from "./TodoItem";
    export default {
        components: {
            TodoItem
        },
        methods: {
            onButtonTap() {
                console.log("Button was pressed");
            }
        },

        data() {
            return {};
        }
    };
</script>

<style scoped>
    .home-panel {
        vertical-align: center;
        font-size: 20;
        margin: 15;
    }

    .description-label {
        margin-bottom: 15;
    }

    .title {
        padding: 50;
        font-size: 50;
    }

    .addButton {
        height: 70;
        width: 70;
        margin: 10;
        font-size: 50;
        background-color: red;
        align: right;
    }
</style>