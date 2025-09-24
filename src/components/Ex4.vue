<script>
    export default { 
        data() {
            return {
                // Add code here
                change: true,
                id: "demo1"
            }
        },
        methods: { 
   			// Add code here
            changecolor (){
                this.change = !this.change
                }
         }
	}
    
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div  v-bind:class="change ? 'blueBox' : 'redBox'" @click="changecolor" :id="id" class="m-2">
            div ID : {{id}} 
        </div>
    <button v-bind:class="change ? 'btn btn-primary' : 'btn btn-danger'" type="button" @click="changecolor">Change color</button>
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
