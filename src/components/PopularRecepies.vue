<template>
  <div class="popular-recepies">
      <div class="title">
          <h5>POPULAR RECEPIES</h5>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Doloremque dolorum veritatis reiciendis dolor laborum voluptas ipsa qui, nisi dignissimos unde illum aliquam.</p>
      </div>
      <div class="cont">
        <div class="cont-left">
            <div class="img">
                <img :src="require('../assets/images/Yogurt-Nan-1200x790.jpg')" alt="">
            </div>
            <div class="text">
                <div class="cont-text">
                    <h5 class="recepies-title">{{ recepies[0].title }}</h5>
                    <p class="sub-title">{{ recepies[0].subTitle }}</p>
                    <p class="text-string">{{ recepies[0].text }}</p>
                    <button>LEARN MORE</button>
                </div>
            </div>
        </div>
        <div class="cont-right">
            <ul>
                <li v-for="(recepie, index) in recepies"
                    :key= "index">
                    <img :src="recepie.img" alt="">     
                </li>
            </ul>

        </div>  
      </div>
  </div>
</template>

<script>
export default {
    name: 'PopularRecepies',
    data() {
        return {
            recepies: [
                {
                    img: require('../assets/images/Mixed-fruits-1200x790.jpg'),
                    title: 'Lunch Favourite with Salad, Naan And Beans',
                    subTitle: 'Bakery, Featured, Healthy, Lates Recepies, Staff Picks',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
                {
                    img: require('../assets/images/r-rachel-park-366508-unsplash-min-1200x790.jpg'),
                    title: 'Lunch Favourite with Salad, Naan And Beans',
                    subTitle: 'Bakery, Featured, Healthy, Lates Recepies, Staff Picks',
                    text: 'lorem' 
                },
                {
                    img: require('../assets/images/r-michelle-tsang-500721-unsplash-min-1200x790.jpg'),
                    title: 'Lunch Favourite with Salad, Naan And Beans',
                    subTitle: 'Bakery, Featured, Healthy, Lates Recepies, Staff Picks',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
                {
                    img: require('../assets/images/quick-summer-drink-460x295.jpg'),
                    title: 'Lunch Favourite with Salad, Naan And Beans',
                    subTitle: 'Bakery, Featured, Healthy, Lates Recepies, Staff Picks',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
                {
                    img: require('../assets/images/r-maarten-van-den-heuvel-400626-unsplash-min-460x295.jpg'),
                    title: 'Lunch Favourite with Salad, Naan And Beans',
                    subTitle: 'Bakery, Featured, Healthy, Lates Recepies, Staff Picks',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
                {
                    img: require('../assets/images/perfect-cosmopolitan-460x295.jpg'),
                    title: 'Lunch Favourite with Salad, Naan And Beans',
                    subTitle: 'Bakery, Featured, Healthy, Lates Recepies, Staff Picks',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
                {
                    img: require('../assets/images/fi2x-6-460x295.jpg'),
                    title: 'Lunch Favourite with Salad, Naan And Beans',
                    subTitle: 'Bakery, Featured, Healthy, Lates Recepies, Staff Picks',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
                {
                    img: require('../assets/images/r-brooke-lark-96398-unsplash-min-460x295.jpg'),
                    title: 'Lunch Favourite with Salad, Naan And Beans',
                    subTitle: 'Bakery, Featured, Healthy, Lates Recepies, Staff Picks',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.'
                },
            ],
        }
    }
}
</script>

<style lang="scss">
@import "../assets/scss/partials/_variables.scss";

.popular-recepies {
    background-color: $cararra;
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

.cont {
    width: 80%;
    margin: 0 auto;
    margin-top: 2em;
    display: flex;
    justify-content: space-between
}

.cont-left {
    width: 48%;
    height: 100%;
    background-color: white;
    .img {
        width: 100%;
        img {
            width: 100%;
            object-fit: cover;
        }
    }

    .cont-text {
        width: 90%;
        margin: 0 auto;
        padding-bottom: 1em;
        .recepies-title {
        font-size: 1.2em;
        }

        p {
            font-family: $fontFamily;
            font-size: 0.7em;
        }

        .sub-title {
            padding-top: 1em;
        }
            .sub-title::after {
                content: '';
                display: inline-block;
                width: 90%;
                height: 1px;
                background-color: $silverChalice;
                margin: 1em;
            }

        .text-string {
            padding-top: 1em;
        }

        button {
            color: $springWood;
            background-color: $orange;
            padding: 0.5em;
            border: 0;
            font-size: 0.7em;
            margin-top: 2em;
        }
    }
}


.cont-right {
    width: 48%;

        ul {
            width: 100%;
            margin: 0 auto;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 5px;
            list-style: none;
    
            li {
                width: 49%;
                height: 125px;
                img {
                    width: 100%;
                    object-fit: cover;
                }
            }
        }

    

    
}



</style>