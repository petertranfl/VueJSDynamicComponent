<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button class="btn btn-primary" @click="selectedComponent = 'appBlue'; selectedTrist = 'Galaxy'">Load Blue Template</button>
                <button class="btn btn-success" @click="selectedComponent = 'appGreen'; selectedTrist = 'Candy'">Load Green Template</button>
                <button class="btn btn-danger" @click="selectedComponent = 'appRed'; selectedTrist = 'Demon'">Load Red Template</button>
                <hr>
                <component :is='selectedComponent'>
                    <p>Support for {{selectedTrist}} Trist!</p>
                </component>
                <!-- <app-blue v-if='selectedComponent = appBlue'>
                    <h1 slot='GalaxyTrist'>Support for Galaxy Trist!</h1>
                </app-blue>
                <app-green v-if='selectedComponent = appGreen'>
                    <h1 slot='DemonTrist'>Support for Demon Trist!</h1>
                </app-green>
                <app-red v-if='selectedComponent = appRed'>
                    <h1 slot='CandyTrist'>Support for Candy Trist!</h1>
                </app-red> -->
            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
        data: function() {
            return {
                selectedComponent: 'appGreen',
                selectedTrist: null
            }
        },
        components: {
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        }
    }
</script>

<style>
</style>
