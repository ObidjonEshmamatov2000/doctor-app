<template>
    <div>
        <!-- <v-sheet
            :height="sheetHeight"
            class="hidden-md-and-up"
        >
            <v-container class="fill-height"> 
                <v-row align="center" justify="center">
                    <h1 class="text-center display-1 ">
                        Welcome to Hop Shop
                    </h1>
                </v-row>
            </v-container>
        </v-sheet> -->

        <v-carousel 
        
        cycle
        show-arrows-on-hover
        :height="sheetHeight"
        >
            <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
            reverse-transition="fade-transition"
            transition="fade-transition"
            ></v-carousel-item>
        </v-carousel>
    </div>
    
</template>

<script>
export default {
    computed: {
        sheetHeight() {
            switch (this.$vuetify.breakpoint.name) {
                case 'xs' : return '300px'
                case 'sm' : return '300px'
                case 'md' : return '400px'
                case 'lg' : return '400px'
                case 'xl' : return '430xp'
            }
            return '250px'
        }
    },
    data () {
      return {
        items: [
          {
            src: 'https://images.pexels.com/photos/3962294/pexels-photo-3962294.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940.jpg',
          },
          {
            src: 'https://images.pexels.com/photos/868110/pexels-photo-868110.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940.jpg',
          },
          {
            src: 'https://images.pexels.com/photos/1087727/pexels-photo-1087727.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940.jpg',
          },
          {
            src: 'https://images.pexels.com/photos/2908975/pexels-photo-2908975.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940.jpg',
          },
        ],
      }
    }
}
</script>

<style scoped>

</style>