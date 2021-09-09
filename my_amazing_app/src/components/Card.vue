<template>
    <v-list>
        <v-list-item v-for="cardData in cardDatas" :key="cardData.text">
            <v-list-item-content>
                <v-card
                        class="mx-auto"
                        max-width="344"
                    > 
                        <v-img
                        src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                        height="200px"
                        ></v-img>

                        <v-card-title>
                        Top western road trips
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
                            @click="show = !show"
                        >
                            <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                        </v-btn>
                        </v-card-actions>

                        <v-expand-transition>
                        <div v-show="show">
                            <v-divider></v-divider>

                            <v-card-text>
                                {{cardData.text}}
                            </v-card-text>
                        </div>
                     </v-expand-transition>
                    </v-card>
            </v-list-item-content>
        </v-list-item>
    </v-list> 
</template>

<script>
    export default{
        data() {
                return {
                    cardDatas: [
                        {text: "card1"},
                        {text: "card2"},
                        {text: "card3"}
                    ]
                }
        }
    }
    
</script>
