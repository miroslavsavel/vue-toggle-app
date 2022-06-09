<template>
    <div>
        <div class="d-flex justify-content-center">
            <div @click="selectedComponent = 'One'" class="p-2 m-2 btn btn-primary">One</div>
            <div @click="selectedComponent = 'Two'" class="p-2 m-2 btn btn-primary">Two</div>
            <div @click="selectedComponent = 'Three'" class="p-2 m-2 btn btn-primary">Three</div>
        </div>
        <div class="d-flex justify-content-center">
            <keep-alive>
                <component :is="selectedComponent"></component>
            </keep-alive>
        </div>
    </div>
</template>

<script>
    import One from './components/OneComponent.vue';
    import Two from './components/TwoComponent.vue';
    import Three from './components/ThreeComponent.vue';

    export default {
        components: {One, Two, Three},

        data() {
            return {
                selectedComponent: 'One'
            }
        }
    }
</script> 
 
 
<style>


</style>