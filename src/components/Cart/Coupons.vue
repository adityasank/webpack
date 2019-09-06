<template>
  <div>
    <div class="mr-2 card">
      <div class="card-header font-weight-bold">
        <h5>Price Details</h5>
      </div>

      <div class="card-body">
        <div>
          <b-form-group class="mb-2">
            <b-input-group>
              <b-form-input v-model="filter" placeholder="Coupons" />
              <b-input-group-append>
                <b-button variant="primary" onclick="this.blur();" class="btn btn-primary">Apply</b-button>
              </b-input-group-append>
            </b-input-group>
          </b-form-group>
        </div>
        <b-button block onclick="this.blur();" class="offer mt-2" variant="outline-primary">
          <b-img class="mr-2" src="/svg/gift.svg" width="20px"></b-img>ADD gift Wrap for 25 Bucks
        </b-button>
      </div>
    </div>
  </div>
</template>

