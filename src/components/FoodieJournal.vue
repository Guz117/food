<template>
  <div class="foodie-journal">
      <!-- <h5>FOODIE JOURNAL</h5>
      <ul>
        <li v-for="(journal, index) in journals"
            :key= "index">
            <img :src="journal.img" alt="">
            <h3>{{ journal.text }}</h3>
            <p>{{ journal.admin }}</p>
        </li>
      </ul> -->
  </div>
</template>

<script>
export default {
    name: 'FoodieJournal',
    data() {
        return {
            journals: [
                {
                    img: require('../assets/images/single-post-img3-200x132.jpg'),
                    text: 'Food Corner: Top Japanese restaurant for Sushi',
                    admin: 'By Admin | March 25th 2019'
                },
                {
                    img: require('../assets/images/fi-roundup-200x132.jpg'),
                    text: 'Roundup: My New Favourite Recipes For Heathy Living',
                    admin: 'By Admin | March 25th 2019'
                },
                {
                    img: require('../assets/images/fi-toasts-200x132.jpg'),
                    text: 'Why THese Toast with Tea Are My New Favourite',
                    admin: 'By Admin | March 25th 2019'
                }
            ],
        }
    }
}
</script>

<style lang="scss">
@import "../assets/scss/partials/_variables.scss";

    // .foodie-journal {
    //     top: -5px;
    //     width: 80%;
    //     margin: 0 auto;
    //     padding: 2em;
    //     background-color: yellowgreen;
    //     h5 {
    //         text-align: center;
    //         font-family: $fontFamily;
    //         padding-bottom: 1.5em;
    //     }
    //     ul {
    //         display: flex;
    //         justify-content: space-between;
    //         list-style: none;
            
    //         li {
    //             display: flex;
    //             flex-direction: column;
    //             justify-content: center;
    //             text-align: center;
    //             width: 30%;
    //             h3, p {
    //                 width: 95%;
    //             }
    //         }
    //     }
    // }

</style>