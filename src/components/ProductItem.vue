<template>
    <div>
        <p>{{ item.nome }}</p>
        <p>{{ item.preco }}</p>
        <p>{{ item.unidademedida }}</p>
    </div>
</template>

<script>
    export default {
        name: 'ProductItem',
        props: {
            item: Object
        }
    };
</script>
