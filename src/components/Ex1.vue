<script>
    export default { 
        // Add Code Here
        // challenge: use array 
        data(){
            return {
                msg: "Choose your favourite fruit",
                fruit1: "apple",
                fruit2: "orange",
                fruit3: "peach",

                fruits: ["apple", "orange", "peach"]
            }
            
        } 
    }
</script>

<template>
    <div id="app">
        {{ msg }} </br>
        {{ fruit1 }} <input type="radio" name="fruit">
        {{ fruit2 }} <input type="radio" name="fruit">
        {{ fruit3 }} <input type="radio" name="fruit">
        <h3>Using Array</h3>
        {{msg}}<br>
        <span v-for="(fruit, index) in fruits" :key="index">
            {{ fruit }} <input type="radio" name="fruit">
        </span>

    </div>
</template>

<style scoped>
</style>
