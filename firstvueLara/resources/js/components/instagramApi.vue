<template>
    <div>
        <h2>Name:{{displayData.data.full_name}}</h2>
        <h2>User statistics:</h2>
        <p>Posts:{{displayData.data.counts.media}}</p>
        <p>Follows:{{displayData.data.counts.follows}}</p>
    </div>
</template>

<script>
    import axios from 'axios';

    export default {
        name:"instagramapi",
        data() {
            return {
                displayData:null
            }
        },

        created() {
            axios
                .get('https://api.instagram.com/v1/users/self/?access_token=2078563806.90bb63f.b819933e66074f7491238f11ab1cd4c6')
                .then(response => (this.displayData= response.data))
                .catch((error) => {
                if (error.response) {
                    // The request was made and the server responded with a status code
                    // that falls out of the range of 2xx
                     console.log(error.response.data);
                     console.log(error.response.status);
                     console.log(error.response.headers);
                } else if (error.request) {
                    // The request was made but no response was received
                    // `error.request` is an instance of XMLHttpRequest in the browser and an instance of
                    // http.ClientRequest in node.js
                    console.log(error.request);
                } else {
                    // Something happened in setting up the request that triggered an Error
                    console.log('Error', error.message);
                }
                console.log(error.config);
            });
        },
    }
</script>

<style scoped>
div{display: flex;}
    h1{display: flex}
</style>
