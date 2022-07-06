<template>
    <div class="container pt-10">
        <div class="banner">
            <div class="d-flex flex-wrap main-banner">
                <div data-aos="fade-right" data-aos-duration="1000"  class="col-lg-5 col-12 banner-desc d-flex flex-column justify-content-center align-items-start">
                    <h1 class="pb-2">DPOKER</h1>
                    <h4 class="pb-3">FUN & PSYCHOLOGY TO EARN</h4>
                    <p>Chào mừng bạn đến với nền tảng Poker phi tập trung kết hợp với công nghệ DeFi tốt nhất trên thế giới. Chúng tôi tạo ra nền tảng này với mong muốn chiến thắng luôn thuộc về người chơi nhờ vào việc trở thành cổng trung gian đảm bảo lợi ích giữa nhà cái và người chơi. 
                    </p>
                    <button class="submit-btn">Đăng ký và chơi ngay</button>
                </div>
                <div data-aos="fade-left"  data-aos-duration="2000" class="col-lg-7 col-12 d-flex align-items-center">
                    <div class="banner-video" @click="playVideoo()">
                        <video id="vidTrailer" ref="vidTrailer" autoplay>
                            <source src="../assets/trainer.mp4" type="video/mp4">
                            <source src="../assets/trainer.mp4" type="video/ogg">
                            Your browser does not support HTML video.
                        </video>
                        <div class="d-flex justify-content-center align-items-center banner-video-play-btn">
                            <img src="../assets/play-button-arrowhead.png" alt="">
                            <p>Video Trailer</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'BannerComponent',
    methods: {
        playVideoo() {
            this.$refs.vidTrailer.play();   
        },
    },
    props: {
        msg: String
    }
}
</script>

<style>
    .pt-10 {
        padding-top: 100px;
    }
    .banner {
        padding: 70px 0;
    }
    .banner-desc {
        padding: 0 100px 0 0;
    }
    .banner-desc h1 {
        font-family: 'Chakra Petch';
        font-style: normal;
        font-weight: 700;
        font-size: 60px;    
        line-height: 34px;
        color: #FFD601;
    }
    .banner-desc h4 {
        font-family: 'Chakra Petch';
        font-style: normal;
        font-weight: 700;
        font-size: 17px;
        line-height: 18px;
        letter-spacing: 0.075em;
        color: #1A94FF;
        padding-top: 16px;
    }
    .banner-desc p {
        font-family: 'Chakra Petch';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 26px;
        color: #FFFFFF;
        padding-top: 40px;
    }
    .submit-btn {
        padding: 16px 40px;
        background-color: #FFD601;
        color: #2E2E2E;
        border-radius: 5px;
        font-weight: 700;
        font-size: 20px;
        line-height: 24px;
        margin-top: 20px;
        transition: transform .3s;
    }
    .submit-btn:hover {
        cursor: pointer;
        transform: scale(1.05);
    }
    .banner-video {
        background: rgba(0, 0, 0, 0.2);
        backdrop-filter: blur(56px);
        padding: 16px;
        margin: 0 0 40px 30px;
        border-radius: 12px;
        border: 1px solid #4d4d4d;
    }
    .banner-video:hover {
        cursor: pointer;
    }
    .banner-video video {
        width: 100%;    
    }
    .banner-video img {
        width: 30px;
        height: 30px;
    }
    .banner-video p {
        font-style: normal;
        font-weight: 600;
        font-size: 24px;
        line-height: 25px;
        color: white;
        padding-left: 15px;
        margin: 0;
    }
    .banner-video-play-btn {
        padding-top: 14px;
        transition: transform 0.3s;
    }
    .banner-video-play-btn:hover {
        cursor: pointer;
        transform: scale(1.1);
    }
    @media(max-width: 1200px) {
        .pt-10 {
            padding-top: 0px;
        }
        .banner-desc h1 {
            padding-top: 50px;
        }
        .banner-video {
            margin: 0;
            margin-top: 30px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        .banner-desc {
            padding-right: 30px;
        } 
    }
    @media(max-width:768px) {
        .main-banner {
            padding: 0 1em;
        }
        .submit-btn {
            width: 100%;
        }
    }
    @media(max-width: 500px) {
        .banner-desc {
            padding-right: 0;
        } 
    }
</style>