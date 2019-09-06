<template>
  <div>
    <b-row class="mt-2">
      <b-col md="8">
        <BankOffers />
      </b-col>

      <b-col md="4">
        <Coupons />
      </b-col>
    </b-row>

    <b-row>
      <b-col >
        <my-cart />
      </b-col>

    </b-row>
  </div>
</template>
<script>
import BankOffers from "@/components/Cart/BankOffers.vue";
import Coupons from "@/components/Cart/Coupons.vue";
import MyCart from "@/components/Cart/MyCart.vue";
export default {
  components: {
    BankOffers,
    Coupons,
    MyCart,
  }
};
</script>
