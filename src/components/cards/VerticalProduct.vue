<template>
    <v-card class="my-sm-2 rounded cyan lighten-5" outlined>
        <v-img :src="product.image" height="200" />
        <v-card-title>{{ product.name }}</v-card-title>
        <v-card-subtitle>${{ product.price }}</v-card-subtitle>
        <v-card-actions>
            <v-btn @click="addToCart" color="success" outlined>
                <v-icon small left>fa-plus</v-icon>
                Add to Card
            </v-btn>
        </v-card-actions>
    </v-card>
</template>

<script>
export default {
    props: {
        product: Object,
        addToCart: Function
    }
}
</script>

<style scoped>
    .rounded {
        transition: .4s ease all;
    }
    .rounded:hover {
        transform: scale(1.1);
    }
</style>