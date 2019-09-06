<template>
  <div class="ml-2 font-weight-bold card">
    <div class="card-header font-weight-bold">
      <h5>Offer Aplicable</h5>
    </div>
    <div class="card-body">
      <div>
        <b-button class="offer" onclick="this.blur();" variant="outline-primary">Offer 1: 50% off on Axis Bank on Min Purchase of $199, T&C apply </b-button>
      </div>

      <b-button class="offer mt-2" onclick="this.blur();" variant="outline-primary">Offer 2 50% off on SBI Bank on Min Purchase of $99, T&C apply </b-button>
    </div>
  </div>
</template>
<style >
.offer {
  border: 1px dashed !important;
}
.offer:hover{
    background: transparent !important ;
    color: #727cf5 !important;
}
</style>

<style scoped>

</style>
