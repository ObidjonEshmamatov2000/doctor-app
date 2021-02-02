<template>
    <div class="text-center">
        <v-overlay :value="overlay" class="flex-column">
            <p>Processing order...</p>
            <v-progress-circular indeterminate size="64" />
        </v-overlay>

        <v-container v-if="!overlay" pt-12>
            <v-row>
                <v-col>
                    <h2>Thank you for your purchase! It will be shipped soon.</h2>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>
export default {
    data() {
        return {
            overlay: false
        }
    },
    mounted() {
        setTimeout(() => {
            this.overlay = false
        }, 3000)
    },
    beforeMount() {
        this.overlay = true
    }
}
</script>

<style scoped>

</style>