<template>
    <v-container mt-4 mb-16>
        <v-row>
            <v-col sm="10" offset-sm="1" >
                <h2 class="heading-3 light-blue--text text--accent-2">Popular Products <v-btn small color="success" to="store" text>view all</v-btn></h2>
                
            </v-col>
        </v-row>
        <v-row>
            <v-col sm="10" offset-sm="1">
                <v-row>
                    <v-col 
                        sm="6" 
                        md="4"
                        v-for="(product) in $store.state.products.slice(0, 12)"
                        :key="product.name"
                    >
                        <VerticalProduct :product="product" :addToCart="addToCart" />
                    </v-col>
                </v-row>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import VerticalProduct from '../cards/VerticalProduct';
export default {
    components: {
        VerticalProduct
    },
    data() {
        return {

        }
    },
    methods: {
        addToCart(index, quantity = 1) {
            this.$store.commit('addItemToCart', { itemId: index, quantity });
            this.$store.commit('updateSnackbar', { show: true });
        }
    }
}
</script>

<style scoped>

</style>