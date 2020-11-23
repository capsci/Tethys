<template>
  <div justify="center">
    
    <v-dialog
      v-model="addorder"
      max-width="600px">
      <template v-slot:activator="{ on }">
        <v-btn
          v-on="on"
          color="success"
           raised dark elevation="13">
          <v-icon>
            fa-cart-plus
          </v-icon> Add New Transaction
        </v-btn>
      </template>
      <v-card>
      <v-card-title>
        <span class="headline">Add New Order</span>
      </v-card-title>
      <v-card-text>
      <v-row>
      <v-col>
        <v-text-field
          v-model="symbol"
          label="Name"
          filled rounded dense
          required />
      </v-col>
      </v-row>
      <v-row>
      <v-col>
        <v-text-field
          v-model="shares"
          label="Shares"
          filled rounded dense
          required />
      </v-col>
      </v-row>
      <v-row>
      <v-col>
        <v-text-field
          v-model="unit"
          label="Unit Price"
          filled rounded dense
          />
      </v-col>
      </v-row>
      <v-row>
      <v-col>
        <v-text-field
          v-model="total"
          label="total"
          filled rounded dense
          required />
      </v-col>
      </v-row>
      <v-row>
      <v-col>
        <v-text-field
          label="Date"
          :value="date"
          filled rounded dense
          readonly required />
        <v-date-picker
          v-model="date"
          @input="datemenu = false" />
      </v-col>
      </v-row>
      </v-card-text>
      <v-card-actions>
        <v-spacer />
        <v-btn
          color="blue darken-1"
          text
          @click="addorder = false" >
          Close
        </v-btn>
        <v-btn
          color="blue darken-1"
          text
          @click="addorder = false" >
          Save
        </v-btn>
      </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  name: 'Order',
  data() {
    return {
      symbol: "",
      shares: 0.0,
      unit: 0.0,
      price: 0.0,
      total: 0.0,
      date: null,
      
      addorder: false,
      datemenu: false,
    }
  },
}
</script>

<style>

</style>