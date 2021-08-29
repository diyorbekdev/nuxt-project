<template>
  <div>
    <b-button id="show-btn" @click="showModal">Rent</b-button>

    <b-modal ref="my-modal" hide-footer title="Using Component Methods">
      <div class="d-block text-center">
        <div class="flex">
          <div class="flex-text">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Est, dicta? Praesentium et exercitationem, excepturi blanditiis, veritatis quam temporibus soluta possimus, ea impedit asperiores. Perferendis nostrum amet cupiditate nihil facere iste.
          </div>
          <div class="flex-cal">
            <vc-date-picker
            :value="null"
            color="red"
            is-dark
            is-range
            ></vc-date-picker>
          </div>
        </div>
      </div>
      <b-button class="mt-3" block 
      @click="() => {
        addItem(product.id)
        hideModal()
      }"

      >Order</b-button>
    </b-modal>
  </div>
</template>

<script>
import {mapMutations} from "vuex"
  export default {
    props: ['product'],
    methods: {
      showModal() {
        this.$refs['my-modal'].show()
      },
      hideModal() {
        this.$refs['my-modal'].hide()
      },
      ...mapMutations(['addItem'])

    }
  }
</script>

<style scoped>
#show-btn {
  width: 100%;
  margin-top: 25px;
  background: #E7512B;
  padding: 10px;
  font-size: 18px;  
  border: 1px solid transparent;
  border-radius: 15px;
  font-weight: 700;
}

.mt-3 {
  background: tomato;
  padding: 10px;
  font-weight: 700;
  border-radius: 15px;
  border: 1px solid transparent;
}

.mt-3:hover {
  background: rgb(211, 59, 33);
}
#show-btn:hover {
  background: #585954;
}

.flex {
  display: flex;
  flex-direction: row;
}

.flex .flex-text {
  flex: 1;
  padding: 5px;
}

.flex .flex-cal {
  flex: 1;
  padding: 5px;
}
</style>