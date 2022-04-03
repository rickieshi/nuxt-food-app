<template>
    <div>
        <h1>Restaurant</h1>
        <ShopInfo/>
    </div>
</template>

<script>
import ShopInfo from '@/components/ShopInfo.vue';
    export default {
        name: 'RestaurantPage',
        components: {
            ShopInfo
        }
    }
</script>