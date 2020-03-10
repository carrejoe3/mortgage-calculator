<template>
  <v-container class="calculatorContainer">
    <div class="inputField">
      <div class="label">Mortgage Amount</div>
      <v-text-field v-model="mortgageAmount" outlined type="number">
        <v-icon slot="append" color="$grey">mdi-cash-usd-outline</v-icon>
      </v-text-field>
    </div>
    <div class="inputField">
      <div class="label">Interest rate</div>
      <v-text-field v-model="interestRate" outlined type="number">
        <v-icon slot="append" color="$grey">mdi-percent</v-icon>
      </v-text-field>
    </div>
    <div class="inputField">
      <div class="label">Mortgage period (years)</div>
      <v-text-field v-model="mortgagePeriod" outlined type="number"></v-text-field>
    </div>
    <div class="resultsSection">
      <div class="totalCostContainer">
        <div>Total cost of mortgage:</div>
        <div>{{ totalCost | toCurrency }}</div>
      </div>
      <div class="monthlyPaymentsContainer">
        <div>Monthly payments:</div>
        <div>{{ monthlyPayments | toCurrency }}</div>
      </div>
    </div>
  </v-container>
</template>

<script>
export default {
  name: 'Calculator',
  data: () => ({
    mortgageAmount: 0,
    interestRate: 3.92,
    mortgagePeriod: 0
  }),
  computed: {
    totalCost () {
      return 69
    },
    monthlyPayments () {
      return 69
    }
  }
}
</script>

<style lang="scss">

$grey: #50514F;

.calculatorContainer {
  color: $grey;
  .resultsSection {
    margin-top: 5%;
  }
  .label {
    font-size: 1em;
    color: $grey;
  }
  .inputField {
    margin-top: 2%;
    .col {
      padding-top: 0px;
      padding-bottom: 0px;
    }
  }
  .totalCostContainer, .monthlyPaymentsContainer {
    display: flex;
    justify-content: space-between;
  }
}
</style>
