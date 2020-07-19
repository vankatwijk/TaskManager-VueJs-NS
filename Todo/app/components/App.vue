<template>
    <Page class="page" actionBarHidden="true">

        <GridLayout columns="*" rows="200, *, auto"
            backgroundColor="lightgray">

            <Label text="Task" class="title" row="0" backgroundColor="green" />
            <Label text="Label 5" row="1" backgroundColor="orange" />
            <StackLayout orientation="horizontal" row="2" backgroundColor="purple">
                <Label text="Label 1" width="*" height="50"
                    backgroundColor="red" />
                <Label text="Label 2" width="*" height="50"
                    backgroundColor="green" />
                <Label text="Label 3" width="*" height="50"
                    backgroundColor="blue" />
                <Label text="Label 4" width="*" height="50"
                    backgroundColor="yellow" />
            </StackLayout>
        </GridLayout>
    </Page>
</template>

<script>
    export default {
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
        padding:50;
        font-size:50;
    }
</style>