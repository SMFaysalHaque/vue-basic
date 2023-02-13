<template>
    <h1>Home Component</h1>
    <h2>Email: {{ email }}</h2> <!-- in third bracket, all things are interpolation -->
    <h2>Mobile: {{ mobile }}</h2>
    <!-- <h2>Mobile: {{ mobile = 888888 }}</h2> In interpolation we can pass a value or we can check true or false -->
    <h2>Mobile: {{ mobile == 888888 }}</h2> <!-- In interpolation we can pass a value or we can check true or false -->
    <h3>Name: {{ getName() }}</h3> <!-- this is a function -->
    <h3>My Name is: {{ getMyName("Faysal Haque") }}</h3> <!-- this is a parameter -->

    <!-- how to work methods and how to pass it in interpolation with parameter -->
    <h1>Methods & Parameter:</h1>
    <h2>My First Name: {{ getFirstName() }}</h2>
    <h2>My Second Name with Parameter: {{ getSecondName('Haque') }}</h2>
    <h3>Get Data: {{ getData().name }}</h3>

</template>

<script>

export default {
    name: 'home-page',
    data(){
        return{
            email: 'faysal@gamil.com',
            mobile: 12345667890,
            getName: function(){
                return 'Faysal Haque';
            },
            getMyName: function(a){
                return a ;
            },
            getData(){
                return {
                    name: 'Faysal',
                    email: 'faysal_haque@gmail.com'
                }
            }
        }
    },

    methods: {
        getFirstName(){
            return "Faysal";
        },
        getSecondName(secondName){
            return secondName;
        }
    }

}
</script>

<style scoped>
h1{
    color: coral;
}
</style>
