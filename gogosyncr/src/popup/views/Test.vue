<template>
    <div>
        <h1>Test</h1>

        <button type="button" class="btn btn-primary" @click="testRequest()">TEST</button>

        <p>{{ data }}</p>
    </div>
</template>

<script>
export default {
    name: 'Test',

    data: function() {
        return {
            data: {},
        }
    },

    
    methods: {
        testRequest: function() {
            console.log('sending request');
            axios.get('http:localhost:3000/rooms/create')
                .then(response => this.data = response)
                .catch(error => console.log(error));
        }
    }
    


}
</script>

<style lang="scss" scoped>
p {
	font-size: 20px;
}
</style>
