<template>
<div>
    <v-app-bar color="pink accent-4 white--text" class="px-md-10 px-sm-5">
        <v-toolbar-title>Hop Shop</v-toolbar-title>
        <v-spacer></v-spacer>
        <span class="hidden-sm-and-up">
            <v-btn color="grey--text text--lighten-5" @click="drawer = !drawer" text>
                <v-icon color="grey lighten-5">fa-bars</v-icon>
            </v-btn>
        </span>

        <v-toolbar-items class="hidden-xs-only">
            <v-btn class="grey--text text--lighten-5" to="/" text>
                <v-icon small left>fa-home</v-icon>
                Home
            </v-btn>
            <v-btn class="grey--text text--lighten-5" to="store" text>
                <v-icon small left>fa-shopping-basket</v-icon>
                Store
            </v-btn>
            <v-btn class="grey--text text--lighten-5" to="cart" text>
                <v-icon small left>fa-shopping-cart</v-icon>
                Cart
            </v-btn>
        </v-toolbar-items>
    </v-app-bar>

    <v-navigation-drawer
        v-model="drawer"
        absolute
        temporary
        right
        class="transition red lighten-4 grey--text text--lighten-5 pt-8"
    >
        <v-list>
            <v-list-item
                v-for="item in items"
                :key="item.title"
                :to="item.link"
                link
            >
                <v-btn text block>
                    <v-icon class="mr-5" small right>fa-{{item.icon}}</v-icon>
                    {{ item.title}}
                </v-btn>
            </v-list-item>
        </v-list>
    </v-navigation-drawer>
</div>

</template>

<script>
export default {
    data() {
        return {
            drawer: false,
            items: [
                { title: 'Home', link: '/', icon: 'home'},
                { title: 'Store', link: '/store', icon: 'shopping-basket'},
                { title: 'Cart', link: '/cart', icon: 'shopping-cart'},
            ]
        }
    }
}
</script>

<style scoped>
    .transition {
        transition: .5s ease all;
    }
</style>