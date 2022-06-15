<template>
    <div class="media-shout">
        <div class="container">
            <div class="d-flex align-items-center justify-content-center">
                <div class="col-lg-9 d-flex flex-wrap media-shout-item">
                    <div v-for="mediaItem in mediaShouts" v-bind:key="mediaItem.id" class="col-lg-4 col-sm-6 col-12 p-3">
                        <img class="p-2" :src="require('../assets/' + mediaItem.imgURL)" v-bind:alt="mediaItem.desc">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "MediaShoutComponent",
    data() {
        return {
            mediaShouts: [
                {
                    "id": 0,
                    "imgURL": "media-0.png",
                    "desc": "Coin 0"
                },
                {
                    "id": 1,
                    "imgURL": "media-1.png",
                    "desc": "Coin 1"
                },
                {
                    "id": 2,
                    "imgURL": "media-2.png",
                    "desc": "Coin 2"
                },
                {
                    "id": 3,
                    "imgURL": "media-3.png",
                    "desc": "Coin 3"
                },
                {
                    "id": 4,
                    "imgURL": "media-4.png",
                    "desc": "Coin 4"
                },
                {
                    "id": 5,
                    "imgURL": "media-5.png",
                    "desc": "Coin 5"
                }
            ]
        } 
    }
}
</script>

<style>
    .media-shout {
        background: rgba(250, 250, 250, 0.1);
        backdrop-filter: blur(90px);
        padding: 55px;
        margin-bottom: 120px;
    }
    .media-shout-item img {
        width: 100%;
        height: 100%;
    }
    /* Mobile */
    @media(max-width: 768px) {
        .media-shout-item .px-5 {
            padding-left: 0 !important;
            padding-right: 0 !important;
        }
    }
</style>