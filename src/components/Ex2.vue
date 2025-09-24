<script>
    export default { 
        data() {
            return {
                width: '200',
                height: '200',
                myImg: '/assets/me.png'
            }
        },
    }
</script>

<template>

    <!-- add code here -->
     <!-- : is short hand notation for vbind-->
     <img v-bind:src="myImg" v-bind:width="width" v-bind:height="height" />
   
</template>
