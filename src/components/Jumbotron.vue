<template>
    <div class="jumbotron">
        <div class="jumbotron-text">
            <div class="jumbotron-text-center">
            <h1>Food Corner: Top Jappanese Restaurant for Shushi</h1>
            <p>March 25, 2019</p>
            </div>
        </div>
    </div>
  
</template>

<script>
export default {
    name: 'Jumbotron'
}
</script>

<style lang="scss">
@import "../assets/scss/partials/_variables.scss";

    .jumbotron {
        height: 500px;
        background: url('../assets/images/single-post-img3-1200x790.jpg');
        background-size: cover;
        background-position-y: center;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .jumbotron-text {
        width: 40%;
        padding: 2em 0;
        background-color: $springWood;
        display: flex;
        justify-content: center;
        .jumbotron-text-center {
            width: 80%;
            h1 {
                text-align: center;
            }
            p {
                padding-top: 1em;
                text-align: center;
            }
        }
    }
</style>