<template>
    <div id="app">
        <ProductsList :products="products"/>
    </div>
</template>

<script>
    import ProductsList from './components/ProductsList';

    export default {
        name: 'App',
        components: {
            ProductsList
        },
        data() {
            return {
                products: [
                    { 
                      nome: "Batata",
                      preco: 2.80,
                      unidademedida: "KG"
                    },
                    { 
                      nome: "Cenoura",
                      preco: 1.70,
                      unidademedida: "KG"
                    },
                    { 
                      nome: "Ovos",
                      preco: 10.00,
                      unidademedida: "DZ"
                    },
                    { 
                      nome: "Refrigerante",
                      preco: 6.45,
                      unidademedida: "PET"
                    },
                    { 
                      nome: "Pao",
                      preco: 0.10,
                      unidademedida: "UN"
                    }
                ]
            }
        }
    }
</script>

<style>
    #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
    }

    h1 {
        color: darkgreen;
        font-weight: bold;
    }

    p {
        color: black;
    }

    ul{
        list-style-type:none;
    }

</style>
