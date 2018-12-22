<template>
    <v-layout justify-center>
    <v-flex xs12 sm6>
      <v-toolbar color="indigo" dark>
        <v-toolbar-side-icon></v-toolbar-side-icon>
        <v-toolbar-title>Discover</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn icon>
          <v-icon>search</v-icon>
        </v-btn>
      </v-toolbar>

      <v-card>
        <v-container
          fluid
          grid-list-md
        >
          <v-layout row wrap>
            <v-flex
              v-for="card in cards"
              :key="card.blood_group"
              v-bind="card.blood_group"
            >
              <v-card>
                <v-card-actions>
                </v-card-actions>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
    data () {
        return{
            cards: [
              {  blood_group : 'A+', quantity: 3 },
              {  blood_group : 'B+', quantity: 8 },
              {  blood_group : 'O+', quantity: 2 },
              {  blood_group : 'AB+', quantity: 5 },
              {  blood_group : 'A-', quantity: 9 },
              {  blood_group : 'B-', quantity: 6 },
              {  blood_group : 'O-', quantity: 8 },
              {  blood_group : 'AB-', quantity: 3 }
            ]
        }
    }
}
</script>