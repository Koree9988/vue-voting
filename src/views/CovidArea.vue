<template>
    <div>
        <v-container>
            <v-row>
                <covidDataVue></covidDataVue>
            </v-row>
        </v-container>
    </div>
</template>

<script>
import axios from 'axios';
import covidDataVue from '@/components/covidData.vue';
export default {
    mounted() {
        const url = 'https://covid19.ddc.moph.go.th/api/Cases/today-cases-by-provinces'
        axios.get(url)
            .then(function (response) {
                console.log(response);
                this.covidData = response.data
            })
            .catch(function (error) {
                console.log(error);
            })
    },
    data: () => ({
        covidData:null,
        
    }),

    components: {
        covidDataVue
    },
};
</script>

<style>
</style>