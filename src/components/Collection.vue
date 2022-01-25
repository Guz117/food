<template>
  <div class="collection">
      <div class="title">
        <h5>CULINARY COLLECTION</h5>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Doloremque dolorum veritatis reiciendis dolor laborum voluptas ipsa qui, nisi dignissimos unde illum aliquam.</p>
      </div>
      <div class="menu">
          <ul>
            <li class="culinary" v-for="(collection, index) in collections"
                :key= "index">
                <div class="img">
                    <img :src="collection.img" alt="">     
                    <p class="collection-text"><a href="#">{{ collection.text }}</a></p>
                </div>
            </li>
          </ul>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Collection',
    data() {
        return {
            collections: [
                {
                    img: require('../assets/images/drinks-recipes.png'),
                    text: 'DRINKS'
                },
                {
                    img: require('../assets/images/soups-recipes.png'),
                    text: 'SOUP'
                },
                {
                    img: require('../assets/images/baking-recipes.png'),
                    text: 'BAKERY'
                },
                {
                    img: require('../assets/images/dinner-recipes.png'),
                    text: 'DINNER'
                },
                {
                    img: require('../assets/images/healthy-recipes.png'),
                    text: 'HEALTHY'
                },
                {
                    img: require('../assets/images/staff-picks.png'),
                    text: 'STAF PICKS'
                },
                {
                    img: require('../assets/images/premium-recipes.png'),
                    text: 'APPETISER'
                },    
                {
                    img: require('../assets/images/quick-easy-recipes.png'),
                    text: 'QUICK & EASY'
                },
            ],
        }
    }
}
</script>

<style lang="scss">
@import "../assets/scss/partials/_variables.scss";

.collection {
     background-color: $cararra;
     padding-top: 5em;
}

.title {
    width: 50%;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    font-family: $fontFamily;
    p {
        font-size: 0.7em;
        padding-top: 1em;
        line-height: 2em;
        text-align: center;
    }
}

.menu {
    width: 80%;
    margin: 0 auto;
    margin-top: 2em;
    ul {
        list-style: none;
        display: flex;
        justify-content: center;
        justify-content: space-between;
        flex-wrap: wrap;
        gap: 20px;

        li:hover .collection-text a {
            background-color: $orange;
            color: white;
        }

        li {
            width: 150px;
            height: 90px;
            cursor: pointer;
            background-color: white;
            .img {
                width: 100%;
                height: 100%;
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;

                img {
                    width: 80%;
                    height: 70%;
                    object-fit: contain;
                }

                p {
                    font-size: 0.4em;
                    font-family: $fontFamily;
                    font-weight: bold;
                    a{
                        padding: 0 50px;
                        text-decoration: none;
                        color: $shark;
                    }
                }
            }
        }
    }
}


</style>