<template>
    <div>
        <v-container>
            <v-row class="text-center">
                <voteBox v-for="team in Teams" :key="team" :teamName="team"></voteBox>
            </v-row>
        </v-container>
    </div>
</template>

<script>
import voteBox from '@/components/voteBox.vue';
export default {
    
    data: () => ({
        covidData:null,
        Teams: ["Team A", "Team B", "Team C"],
    }),

    components: {
        voteBox
    },
};
</script>

<style>
</style>