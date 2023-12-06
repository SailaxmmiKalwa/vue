<template>
    <div class="cards-container">
        <cardComponent
            v-for="(company, i) in companieslist"
            :id = companieslist[i].id
            :companiesList = companieslist
        />
    </div>
</template>

<style scoped>
.cards-container{
    margin-left: 10px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
}

@media screen and (max-width: 600px) {
.cards-container{
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    justify-content: center;
}
}

</style>

<script>
import cardComponent from './cardComponent.vue';

export default {
  name: 'cardsList',
  components: {
    cardComponent
    },
    props : ['companieslist']
}
</script>