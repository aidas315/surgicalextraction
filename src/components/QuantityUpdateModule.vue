<template>
    <div class="field has-addons">
        <div class="control">
            <input class="input" type="text" v-model="quantity" style="min-width: 100px">
        </div>
        <div class="control">
            <a class="button is-info" @click.prevent="$root.addToCart($event, product, quantity )">
                Update
            </a>
        </div>
    </div>
</template>

<script>
export default {
    props: ['cartStore'],
    data() {
        return {
            quantity: 10,
            product: null,
        }
    },
    created() {
        this.quantity = this.$props.cartStore.quantity
        this.product = this.$props.cartStore.product
    }
}
</script>
