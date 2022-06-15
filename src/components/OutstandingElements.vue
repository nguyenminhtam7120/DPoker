<template>
    <div id="outstandElement" class="outstand-element">
        <div class="container banner">
            <div class="outstand-elements p-3">
                <h4 class="title-desc">CÁC YẾU TỐ NỔI BẬT</h4>
                <div class="outstand-box d-flex flex-wrap">
                    <div v-for="itemStand in listStanding" v-bind:key="itemStand.id" class="col-lg-4 col-sm-6 col-12 pe-4 pb-5">
                        <div class="outstand-card">
                            <img :src="require('../assets/' + itemStand.imgURL)" alt="">
                            <div class="outstand-card-desc">
                                <h5>{{itemStand.title}}</h5>
                                <div class="an">
                                    <p class="px-4">{{itemStand.desc}}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'OutstandingElements',
    data() {
        return {
            listStanding:[
                {
                    "id": 1,
                    "imgURL": "special-1.png",
                    "title": 'KIẾM TIỀN THẬT',
                    "desc": 'Với cơ chế Play-To-Earn, bạn có thể thoải mái kiếm tiền bằng cách thi đấu trực tuyến với những người chơi trên toàn thế giới.'
                },
                {
                    "id": 2,
                    "imgURL": "special-2.png",
                    "title": 'NFT AVATAR',
                    "desc": 'Tăng thêm thu nhập với hình đại diện của chính bạn. Tăng cường nhận diện thương hiệu cá nhân'
                },
                {
                    "id": 3,
                    "imgURL": "special-3.png",
                    "title": 'VIDEO CALL',
                    "desc": 'Tạo cơ hội cho các người chơi tương tác trực tiếp với nhau. Xóa bỏ khoảng cách người chơi trong thế giới Metaverse'
                },
                {
                    "id": 4,
                    "imgURL": "special-4.png",
                    "title": 'METAVERSE',
                    "desc": 'Gặp gỡ bạn bè cũng như đối mặt với các đối thủ trong thế giới ảo 3D.'
                },
                {
                    "id": 5,
                    "imgURL": "special-5.png",
                    "title": 'PRIVATE NETWORK',
                    "desc": 'Trở thành người xây dựng mạng lưới riêng và mời người chơi tham gia các trò chơi độc quyền của bạn. Trở thành người xây dựng mạng lưới riêng và mời người chơi tham gia các trò chơi độc quyền của bạn. Trở thành người xây dựng mạng lưới riêng và mời người chơi tham gia các trò chơi độc quyền của bạn. Trở thành người xây dựng mạng lưới riêng và mời người chơi tham gia các trò chơi độc quyền của bạn.Trở thành người xây dựng mạng lưới riêng và mời người chơi tham gia các trò chơi độc quyền của bạn.Trở thành người xây dựng mạng lưới riêng và mời người chơi tham gia các trò chơi độc quyền của bạn.Trở thành người xây dựng mạng lưới riêng và mời người chơi tham gia các trò chơi độc quyền của bạn '
                }
            ]
        }
    },
    methods: {

    },
    props: {
        msg: String,
    },
}
</script>

<style>
    .outstand-element {
        background-image: url('../assets/final-bg-2.png');
        background-repeat: no-repeat;
        background-size: 100% 100%;
    }
    .outstand-element .banner{
        padding: 50px 0;
    }
    .title-desc {
        font-family: 'Chakra Petch';
        font-style: normal;
        font-weight: 700;
        font-size: 38px;
        line-height: 64px;
        font-feature-settings: 'pnum' on, 'lnum' on;
        color: #FFD601;
        margin-bottom: 48px;
    }
    .outstand-card {
        padding: 12px;
        background: rgba(0, 0, 0, 0.2);
        backdrop-filter: blur(56px);
        border-radius: 12px;
        border: 2px solid rgba(255, 255, 255, .2);
    }
    .outstand-card:hover {
        cursor: pointer;
        border: 2px solid #FFD601;
    }
    .outstand-card img {
        width: 100%;
    }
    .outstand-card-desc {
        text-align: center;
        min-height: 120px;
    }
    .outstand-card-desc h5 {
        font-family: 'Chakra Petch';
        font-style: normal;
        font-weight: 700;
        font-size: 24px;
        line-height: 22px;
        color: #FFD601;
        margin: 30px 0 20px;
    }
    .outstand-card-desc .an,
    .reasion-card-desc .an {
        display: block;
        display: -webkit-box;
        height: 16px*1.3*3;
        font-size: 16px;
        line-height: 1.3;
        -webkit-line-clamp: 3;
        -webkit-box-orient: vertical;
        overflow: hidden;
        text-overflow: ellipsis;
        margin-top:10px;
    }
    .outstand-card-desc p {
        font-family: 'Chakra Petch';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 22px;
        color: #FFFFFF;
    }
    /* Mobile */
    @media (max-width: 768px) {
        .outstand-box > .pe-4 {
            padding-left: 1rem !important;
            padding-right: 1rem !important;
        }
    }
</style>