<template>
    <div class="text-center my-3">
        <img :src="require('../assets/images/' + path + '')" :alt="name" class="w-56 mx-auto rounded-full">
            <h5 class="mt-3 text-center text-xl font-bold">{{ name }}</h5>
            <p>{{ rank }}</p>
    </div>
</template>

<script>
export default {
    name: 'User',
    props: {
        path: String,
        name: String,
        rank: String
    }
}
</script>