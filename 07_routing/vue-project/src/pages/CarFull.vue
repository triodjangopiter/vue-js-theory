<template>
    <div>
        <h1>Full</h1>
        <h4>Car name {{name}} </h4>
        <h5>Car year {{year}}</h5>

        <div class="scroll"></div>
        <h6 id="scroll">Hello from the bottom</h6>
    </div>
</template>

<script>
    export default {
        computed: {
            year() {
                return this.$route.query.year;
            },
            name() {
                return this.$route.query.name;
            }
        },
        beforeRouteEnter: (to, from, next) => {
            // next() with true or false
        }
    }
</script>

<style scoped>
    .scroll {
        width: 100px;
        height: 1000px;
        background: #ccc;
    }
</style>

