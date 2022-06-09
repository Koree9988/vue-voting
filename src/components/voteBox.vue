<template>
  <div>
    <v-col >
      <v-card class="mx-auto" max-width="344" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <v-list-item-title class="text-h5 mb-1">
              <h3>{{ teamName }}</h3>
            </v-list-item-title>
            <v-list-item-subtitle>
              <h3>Score : {{ score }}</h3>
            </v-list-item-subtitle>
          </v-list-item-content>
          <!-- <v-list-item-avatar tile size="80" color="grey"></v-list-item-avatar> -->
        </v-list-item>

        <v-card-actions>
          <v-btn @click="addvote()" outlined rounded text> Vote </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </div>
</template>

<script>
export default {
  props: ["teamName"],
  data() {
    return {
      score: 0,
    };
  },
  methods: {
    addvote() {
      this.score++;
    },
  },
};
</script>

<style>
</style>