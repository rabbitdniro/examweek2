<script setup>
    import {reactive} from "vue";

    const userData = reactive(
        {
            id: "",
            quote: "",
            anime: "",
            character: ""
        }
    )

    const apiUrl = "https://animechan.xyz/api/random";

    async function getApiData() {
    const response = await fetch(apiUrl);
    const received = await response.json();
    userData.id = received.id;
    userData.quote = received.quote;
    userData.anime = received.anime;
    userData.character = received.character;
    }

</script>

<template>
    <div class="container mt-5">
        <hr>
        <div class="row">
            <h1>Data from API</h1>
        </div>

        <div class="row">
            <div class="col">
                <button @click="getApiData()" type="button" class="btn btn-outline-primary">Show Data</button>
            </div>
        </div>

        <div class="card mt-3" style="width: 25rem; border: none;">
            <div class="row mt-3">
                <div class="col">
                    <div v-for="(value, key, index) in userData" :key="index">
                        <p class="text-start">{{ key }} <span>: {{ value }}</span></p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
</style>