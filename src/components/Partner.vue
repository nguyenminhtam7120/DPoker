<template>
    <div class="container">
        <h4 data-aos="zoom-in" data-aos-duration="2000" class="title-desc text-center title-special">ĐỐI TÁC CỦA DPOKER</h4>
    </div>
    <div class="media-shout">
        <div class="container">
            <div class="d-flex align-items-center justify-content-center">
                <div class="col-lg-9 d-flex flex-wrap media-shout-item">
                    <div data-aos="zoom-in" data-aos-duration="2000" v-for="partner in partners" v-bind:key="partner.id" class="col-lg-3 col-sm-6 col-12 p-3">
                        <img class="p-2" :src="require('../assets/' + partner.imgURL)" v-bind:alt="partner.desc">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "PartnerComponent",
    data() {
        return {
            partners: [
                {
                    "id": 0,
                    "imgURL": "partner-1.png",
                    "desc": "Partner 1"
                },
                {
                    "id": 1,
                    "imgURL": "partner-2.png",
                    "desc": "Partner 2"
                },
                {
                    "id": 2,
                    "imgURL": "partner-3.png",
                    "desc": "Partner 3"
                },
                {
                    "id": 3,
                    "imgURL": "partner-4.png",
                    "desc": "Partner 4"
                }
            ]
        }
    }
}
</script>

<style>

</style>