<template>
  <div class="container">
    <h4>Adding New Order</h4><br/>
    <form action="">
      <label for="symbol">Symbol</label>
      <input type="text" id="symbol" /><br/>
      <label for="shares">Shares</label>
      <input type="text" id="shares" /><br/>
      <label for="unit">Unit Price</label>
      <input type="text" id="unit" /><br/>
      <label for="total">Total Price</label>
      <input type="text" id="total" /><br/>
      <label for="date">Date</label>
      <input type="date" id="date" /><br/>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Order',
}
</script>

<style>

</style>