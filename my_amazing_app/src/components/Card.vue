<template>
    <v-row
        class = "mb-6"
        no-gutters
    >
        <template v-for="(cardData,n) in cardDatas">
            <v-col  :key="n">

                <v-card
                    class="mx-auto"
                    max-width="344"
                > 
                    <v-img
                    :src = cardData.imageURL
                    height="200px"
                    ></v-img>

                    <v-card-title>
                        {{cardData.title}}
                    </v-card-title>

                    <v-card-subtitle>
                    {{cardData.text}}
                    </v-card-subtitle>

                    <v-card-actions>
                    <v-btn
                        color="orange lighten-2"
                        text
                    >
                        Explore
                    </v-btn>

                    <v-spacer></v-spacer>

                    <v-btn
                        icon
                        @click="cardData.show = !cardData.show"
                    >
                        <v-icon>{{ cardData.show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                    </v-btn>
                    </v-card-actions>

                    <v-expand-transition>
                    <div v-show="cardData.show">
                        <v-divider></v-divider>

                        <v-card-text>
                        I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
                        </v-card-text>
                    </div>
                    </v-expand-transition>
                </v-card>


            </v-col>
        </template>
    </v-row>
</template>

<script>
    export default{
        data() {

                return {
                    show: false,
                    cardDatas: [
                        {text: 'card1 text', title: 'Do you want to learn cook?', imageURL: 'https://cdn.vuetifyjs.com/images/cards/cooking.png', show : false},
                        {text: 'card2 text', title: 'Amazing bees and flowers' , imageURL: 'https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg', show : false},
                        {text: 'card3 text', title: 'Top western road trips' ,imageURL: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', show : false},
                        {text: 'card4 text', title: 'You should see this houses', imageURL: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', show : false},
                        {text: 'card5 text', title: 'Best airlines', imageURL: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', show : false},
                        {text: 'card6 text', title: 'You should see this places', imageURL: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg', show : false},
                        {text: 'card7 text', title: 'Turkish foods which you have to try', imageURL: 'https://cdn.vuetifyjs.com/images/cards/cooking.png', show : false},
                        {text: 'card8 text', title: 'Bees love this flowers so much', imageURL: 'https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg', show : false}
                    ]
                }
        }
    }
    
</script>
