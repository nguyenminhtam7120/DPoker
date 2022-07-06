<template>
    <h4 data-aos="zoom-in" data-aos-duration="2000" class="title-desc text-center title-special pb-2">BACKER CỦA CHÚNG TÔI</h4>
    <div class="media-shout">
        <div class="">
            <div class="container">
                <div class="d-flex align-items-center justify-content-center">
                    <div class="col-lg-9 d-flex flex-wrap media-shout-item">
                        <div data-aos="zoom-in" data-aos-duration="2000" v-for="backer in backers" v-bind:key="backer.id" class="col-lg-3 col-sm-6 col-12 p-3">
                            <img class="p-2" :src="require('../assets/' + backer.imgURL)" v-bind:alt="backer.desc">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "BackerComponent",
    data() {
        return {
            backers: [
                {
                    "id": 0,
                    "imgURL": "backer.png",
                    "desc": "Partner 1"
                },
                {
                    "id": 1,
                    "imgURL": "backer.png",
                    "desc": "Partner 2"
                },
                {
                    "id": 2,
                    "imgURL": "backer.png",
                    "desc": "Partner 3"
                },
                {
                    "id": 3,
                    "imgURL": "backer.png",
                    "desc": "Partner 4"
                }
            ]
        }
    }
}
</script>

<style>

</style>