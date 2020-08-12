<template>
    <div>
        <form @submit="onFormSubmit">
            <p>
                <label>Nome:</label>
                <input type="text" v-model="product.Name">
                {{firstNameError}}
            </p>

            <p>
                <label>Preço:</label>
                <input type="text" v-model="product.Price">
            </p>

            <p>
                <label>Unidade Medida:</label>
                <input type="text" v-model="product.Unit">
            </p>

            <button type="submit">Cadastrar</button>
        </form>

        <p>{{product.Name}} por apenas {{product.Price}} cada {{product.Unit}}.</p>
    </div>
</template>

<script>
    export default {
        name: 'ProductForm',
        props: {
            addProduct: Function
        },
        data () {
            return {
                product: {
                    Name: "",
                    Price: 0,
                    Unit: ""
                }
            }
        },
        methods: {
            onFormSubmit(e) {
                e.preventDefault();

                this.addProduct(this.product)
            }
        }
    };
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
