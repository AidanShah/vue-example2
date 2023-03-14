<script>
import NavBar from './NavBar.vue'
import CartItem from './CartItem.vue'

export default {
    data() {
        return {
            hotdog: "default",
            numDresses: 0,
            currentCart: {}
        }
    },
    components: { NavBar,CartItem }, 
    methods:{
        addHotDog(){
            if("hotdog" in this.currentCart){
                this.currentCart["hotdog"]["quantity"] += 1;
            }
            else{
                this.currentCart["hotdog"] = {"product":"hotdog","quantity":1,"price":1}
            }
        },
        addHotDogWeb(){
            if("hotdogwebsite" in this.currentCart){
                this.currentCart["hotdogwebsite"]["quantity"] += 1;
            }
            else{
                this.currentCart["hotdogwebsite"] = {"product":"hotdogwebsite","quantity":1,"price":14012}
            }
        },
        addFord(){
            if("ford" in this.currentCart){
                this.currentCart["ford"]["quantity"] += 1;
            }
            else{
                this.currentCart["ford"] = {"product":"ford","quantity":1,"price":33695}
            }
        },
        addVueLogo(){
            if("vuelogo" in this.currentCart){
                this.currentCart["vuelogo"]["quantity"] += 1;
            }
            else{
                this.currentCart["vuelogo"] = {"product":"vuelogo","quantity":1,"price":10000000}
            }
        },
        test(){
            this.currentCart["vuelogo"] = {"product":"vuelogo","quantity":1,"price":10000000}
        }
    }
}
</script>

<template>
    <body>
        <NavBar></NavBar>
        <h4>Hotdog Sale</h4>
        <p>{{ currentCart }}</p>
        <CartItem>
            <body><h1>Vue Logo</h1>
            <img alt="Vue logo" class="logo" src="../assets/logo.svg" width="150" height="150" />
            <br>
            <p>This item is worth 10 million hot dogs.</p>
            <br>
            <button @click="addVueLogo()">Add to Cart</button>
            <br>
            <p>Price: $10,000,000</p>
            </body>
        </CartItem>
        <br>
        <CartItem>
            <body><h1>Hot Dog</h1>
            <img alt="Vue logo" class="logo" src="https://images.squarespace-cdn.com/content/v1/5dd8630d09ab5908e35b35a0/1574463308006-PDSJDF9EEEB0TJG7TL1N/img-HotDogStock-1080x675.png?format=1000w" width="150" height="150" />
            <br>
            <p>This item is worth 1 hot dog.</p>
            <br>
            <button @click="addHotDog()">Add to Cart</button>
            <br>
            <p>Price: $1</p>
            </body>
        </CartItem>
        <br>
        <CartItem>
            <body><h1>Hot Dog Website</h1>
            <img alt="Vue logo" class="logo" src="../assets/pictureofhotdog.png" width="150" height="150" />
            <br>
            <p>This item is worth almost 12 hot dogs.</p>
            <br>
            <button @click="addHotDogWeb()">Add to Cart</button>
            <br>
            <p>Price: $14,012</p>
            </body>
        </CartItem>
        <br>
        <CartItem>
            <body><h1>FordF150</h1>
            <img alt="Vue logo" class="logo" src="../assets/fordf150.png" width="150" height="150" />
            <br>
            <p>This item is worth 33,695 hot dogs.</p>
            <br>
            <button @click="addFord()">Add to Cart</button>
            <br>
            <p>Price: $33,695</p>
            </body>
        </CartItem>
        <button @click="this.currentCart= {}">Reset Cart</button>
    </body>
</template>

<style scoped></style>
