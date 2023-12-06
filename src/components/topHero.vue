<template>
    <div class="container">
        <h1>Top 5 Companies and their revenues</h1>
    </div>
</template>
<style scoped>
.container{
    background-image: url('https://www.commercialcafe.com/blog/wp-content/uploads/sites/10/2020/09/most-popular-office-buildings-featured.jpg');
    height: 400px;
    width: auto;
    background-size: cover;
    background-position: center;
}
h1{
    margin-top: 10px;
}

@media screen and (max-width: 600px) {
.container{
    width: 100%;
}

}

</style>
<script>
    export default{
        name : 'tophero'
    }
</script>