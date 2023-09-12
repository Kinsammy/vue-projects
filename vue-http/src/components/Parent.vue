<template>
    <div>
        Parent Conponent
        <button @click="showChild = !showChild">Toggle Click</button>
        <child v-if="showChild" />
    </div>
</template>

<script>
import Child from './Child.vue'
    export default {
        name: "Parent",
        components: { Child },
        data() {
            return {
                showChild: true,
            }
        },
        beforeCreate(){
            console.log('Parent beforeCreate()')
        },
        created(){
            console.log('Parent created()')
        },
        beforeMount(){
            console.log('Parent beforeMount()')
        },
        mounted(){
            console.log('Parent mounted()')
        },
        beforeUpdate(){
            console.log('Parent beforeUpdate()')
        },
        updated(){
            console.log('Parent updated()')
        }
        
    }
</script>

<style scoped>

</style>