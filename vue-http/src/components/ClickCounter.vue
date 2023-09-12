<template>
    <div>
        <button @click="incrementCount">Clicked {{ count }} times</button>
    </div>
</template>

<script>
import CounterMixin from '../mixins/Counter'
    export default {
        name: "ClickCounter",
        mixins: [CounterMixin],
        // data() {
        //     return {
        //         count: 0
        //     }
        // },
        // methods: {
        //     incrementCount() {
        //         this.count++;
        //     }
        // }
    }
</script>

<style lang="scss" scoped>

</style>