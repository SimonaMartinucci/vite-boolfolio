<script>

    import { store } from '@/store/store';
    import axios from 'axios';

    export default{

        data() {
            return {
                projects: [],
            }
        },

        methods: {
            getApi() {
                axios.get(store.apiUrl + 'projects')
                    .then(response => {
                        // console.log(response.data);
                        this.projects = response.data;
                        // console.log(this.projects);
                            
                    })
            }
        },

        mounted() {
            this.getApi();
        }
    }

</script>

<template>

    <div class="container py-4">

        <h1 class="mb-3">I miei progetti</h1>

        <ul>
            <li class="lh-lg" v-for="project in projects" :key="project.id">{{ project.title }}</li>
        </ul>

    </div>

</template>

<style lang="scss">

</style>