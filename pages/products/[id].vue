<template>
    <div>
        <p>
            <h1>{{ data.title }}</h1>
            <p>{{ data.description }}</p>
        </p>
    </div>
</template>
<script lang="ts" setup>
interface product{
    title:string,
    description:string
}
const { id } = useRoute().params;
const url = "https://fakestoreapi.com/products/" + id
const { data} = await useFetch(url);
</script>