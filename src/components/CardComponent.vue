<template>
    <div class="card-wrapper">
        <div class="img-card-wrapper">
            <img :src="img" :alt="title">
        </div>
        <div>
            <p class="font-my-light text-center pt-3">
                {{ title }}
            </p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'CardComponent',
        props: {
            img: String,
            title: String
        },
        data() {
            return {
            }
        }
    }
</script>

<style lang="scss" scoped>

.card-wrapper {
    width: 180px;
    height: 250px;
}
.img-card-wrapper {
    height: 200px;
    overflow: hidden;
}

</style>