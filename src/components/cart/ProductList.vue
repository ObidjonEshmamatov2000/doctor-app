<template>
    <v-container>
        <v-row
            v-for="product in $store.state.products"
            :key="product.name"
        >
            <HorizontalProduct :product="product" btnAction="remove" />
        </v-row>
    </v-container>
</template>

<script>
import HorizontalProduct from '../cards/HorizontalProduct';

export default {
    components: {
        HorizontalProduct
    },
    methods: {
        removeFromCart() {
            
        }
    }
}
</script>