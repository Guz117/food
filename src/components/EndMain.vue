<template>
  <div class="end-main">
    <ul>
      <li v-for="(recepie, index) in recepies"
      :key= "index">
        <div class="img">
          <img :src="recepie.img" alt="">     
        </div>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
    name: 'EndMain',
    data() {
        return {
            recepies: [
                {
                    img: require('../assets/images/Yogurt-Nan-200x132.jpg'),
                    title: 'Lunch Favourite with Salad, Naan And Beans',
                    subTitle: 'Bakery, Featured, Healthy, Lates Recepies, Staff Picks',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
                {
                    img: require('../assets/images/Mixed-fruits-200x132.jpg'),
                    title: 'Lunch Favourite with Salad, Naan And Beans',
                    subTitle: 'Bakery, Featured, Healthy, Lates Recepies, Staff Picks',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
                {
                    img: require('../assets/images/r-rachel-park-366508-unsplash-min-200x132.jpg'),
                    title: 'Lunch Favourite with Salad, Naan And Beans',
                    subTitle: 'Bakery, Featured, Healthy, Lates Recepies, Staff Picks',
                    text: 'lorem' 
                },
                {
                    img: require('../assets/images/r-michelle-tsang-500721-unsplash-min-200x132.jpg'),
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


.end-main {
  width: 100%;
  padding-bottom: 2em;
  ul {
    width: 100%;
    display: flex;
    li {
      width: 25%;
      img {
        width: 100%;
      }
    }
    
  }
}
</style>