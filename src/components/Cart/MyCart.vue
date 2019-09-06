<template>
  <b-row>
    <b-col md="8">
      <div class="ml-2 font-weight-bold card">
        <div class="card-header">
           <b-row>
            <b-col >
              <b-text>  My Cart </b-text>
                </b-col>
     <b-col >
<div class= "form-inline">
                <b-img class="ml-5 mr-1" src="/svg/placeholder.svg" width="21px" >Delivery To</b-img>
            <v-select v-model="selected" placeholder="Enter Pincode " :options="['Address 1','address 2']"></v-select>
                </div>
                </b-col>
           
                </b-row>
              
          </div>
        <div class="card-body">
          <div>
            <div class="font-weight-normal">
              <b-row>
                <b-col md="4">
                  <b-img class="image1" :src="image"></b-img>

                  <b-input-group-append class="mt-2">
                    <b-button
                      variant="primary"
                      onclick="this.blur();"
                      size="sm"
                      class="mr-4"
                      v-on:click.prevent="increment"
                    >+</b-button>
                    <h5>{{ count }}</h5>
                    <b-button
                      size="sm"
                      onclick="this.blur();"
                      variant="primary"
                      class="ml-4"
                      v-on:click.prevent="decrement"
                    >-</b-button>
                  </b-input-group-append>
                </b-col>

                <b-col md="5">
                  <h4 class="ml-2 title">{{productName}}</h4>
                  <p class="ml-2 color">{{productColor}}</p>
                  <p class="ml-2 Seller">Seller : {{brand}}</p>

                  <h4 class="ml-2 price">
                    ${{actualPrice}}
                    <del class="ml-1 text-muted">${{originalPrice}}</del>
                    <h6 class="text-success">
                      <div>{{discount}}% off 1 offer Applied</div>
                    </h6>
                  </h4>
                  <b-input-group>
                    <div class="mt-4">
                      <b-button class="savefor float-left" size="sm">Save for later</b-button>

                      <b-button class="remove ml-2 float-right" size="sm">Remove</b-button>
                    </div>
                  </b-input-group>
                </b-col>

                <b-col md="3">
                  <h6 class="ml-2 delivery">Delivery By 24th Aug,2019</h6>
                  <h6 class="ml-2 delivery">10 days Replacement policy</h6>
                  <h6 class="ml-2 delivery text-success">Free Delivery</h6>
                </b-col>
              </b-row>
            </div>
          </div>
        </div>

        <div class="card-footer">
          <b-button class="remove">Remove All</b-button>
          <b-button class="float-right" onclick="this.blur();" variant="primary">Continue</b-button>
        </div>
      </div>
    </b-col>

    <b-col md="4">
      <div class="mr-2 card">
        <div class="card-header font-weight-bold">
          <h5>Price Details</h5>
        </div>

        <div class="card-body">
          <h5 class="font-weight-normal">
            Price
            <div class="font-weight-bold float-right">${{actualPrice}}</div>
          </h5>
          <h5 class="font-weight-normal">
            Tax
            <div class="font-weight-bold float-right">${{tax}}</div>
          </h5>
          <h5 class="font-weight-normal">
            Coupon Discount
            <div class="font-weight-bold float-right">{{discount}}%</div>
          </h5>
          <h5 class="font-weight-normal">
            Order Total
            <div class="font-weight-bold float-right">${{actualPrice}}</div>
          </h5>
          <h5 class="font-weight-normal">
            Delivery Charges
            <div class="font-weight-bold float-right">{{delivery}}</div>
          </h5>
        </div>

        <div class="card-footer">
          <h5>
            Total Payable
            <div class="font-weight-bold float-right">${{actualPrice}}</div>
          </h5>
          <h5
            class="mt-4 text-center text-success font-weight-normal"
          >You wil save $200 in this order</h5>
        </div>
      </div>
    </b-col>
  </b-row>
</template>
<script>
import vSelect from "vue-select";

export default {
  components: {
    'v-select': vSelect
  },

  data: () => {
    return {
      count: 0,
      originalPrice: 399,
      actualPrice: 199,
      productName: "Samsung Galaxy M30",
      productColor: "Matt Black",
      brand: "Samsung",
      tax: 0,
      discount: 50,
      delivery: "0",
      selectOption : ["Alwin X road,Hyderabad,500045", "Kukatpally,Hyderabad ,500045"],
      selected : '',
      image:"https://images.samsung.com/is/image/samsung/in-galaxy-m20-m205f-4gb-sm-m205fdagins-black-143690877?$PD_GALLERY_L_JPG$"
              
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      if (this.count > 0) {
        this.count--;
      }
    }
  }
};
</script>
<style>
.image1 {
  width: 200px !important;
  margin-left: -24px; 
}
.savefor {
  font-weight: bold !important;

  color: black !important;
  background: white !important;
  border: none !important;
  box-shadow: none !important;
}
.remove {
  font-weight: bold !important;
  color: rgb(243, 9, 87) !important;
  background: white !important;
  border: none !important;
  box-shadow: none !important;
}
.vs__dropdown-toggle{
  width: 300px !important;
  border-radius: 1px !important;
  height: 36px !important;
}
</style>