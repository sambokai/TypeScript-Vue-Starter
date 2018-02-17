<template>
    <div>
        Name: <input v-model="name" type="text">
        <h1>Hello Decorator Component</h1>
        <hello-decorator :name="name" :initialEnthusiasm="5" ></hello-decorator>
    </div>
</template>

<script lang="ts">


    import {Vue, Component, Prop, Provide} from "vue-property-decorator";
    import HelloDecorator from './components/HelloDecorator.vue'

    @Component({
        components: {
            HelloDecorator
        }
    })
    export default class App extends Vue {
        @Provide() name: string = "World";
    }
</script>

<style scoped>

</style>