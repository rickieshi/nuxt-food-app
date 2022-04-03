<template>
  <section class="restaurantinfo">
    <div v-for="store in fooddata" :key="store.id">
      <h2> {{ store.name }} </h2>
      <p> Delivery Time: {{store.deliveryTime }} </p>
      <p> Rating: {{store.rating}}</p>
      <p v-if="store.freeDelivery" class="label">
        <span>Free Delivery</span>
      </p>

      <div class="row">
        <div v-for="item in store.menu" :key="item.id" class="items"
          :style="`background: url(${item.img}) no-repeat center center`"
        >
            <div class="iteminfo">
                <div>
                    <h4> {{item.item}} </h4>
                    <p> {{priceFormatting(item.price)}} </p>
                </div>
                <button class="ghost">View Item</button>
            </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import {
  mapState
} from 'vuex';

export default {
  computed: {
    ...mapState([
      'fooddata',
    ])
  },
  methods: {
      priceFormatting (price) {
          return `$${price.toFixed(2)}`
      }
  }
};
</script>

<style lang="scss" scoped>

</style>