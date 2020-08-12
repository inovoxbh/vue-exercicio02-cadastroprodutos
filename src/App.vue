<template>
    <div id="app">
        <ProductForm :addProduct="addProduct" />
        <ProductsList :products="products"/>
    </div>
</template>

<script>
    import ProductsList from './components/ProductsList';
    import ProductForm from './components/ProductForm';

    export default {
        name: 'App',
        components: {
            ProductsList,
            ProductForm
        },
        methods: {
          addProduct (product) {
            this.products = this.products.concat({
                name: product.Name,
                price: product.Price,
                unit: product.Unit
            });
          }
        },        
        data() {
            return {
                products: [
                    { 
                      name: "Batata",
                      price: 2.80,
                      unit: "KG"
                    },
                    { 
                      name: "Cenoura",
                      price: 1.70,
                      unit: "KG"
                    },
                    { 
                      name: "Ovos",
                      price: 10.00,
                      unit: "DZ"
                    },
                    { 
                      name: "Refrigerante",
                      price: 6.45,
                      unit: "PET"
                    },
                    { 
                      name: "Pão",
                      price: 0.10,
                      unit: "UN"
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
