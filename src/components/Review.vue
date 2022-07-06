<template>
    <div class="container-fluid banner">
        <div class="d-flex flex-wrap justify-content-center review">
            <div data-aos="fade-up" data-aos-duration="1000" class="col-lg-6 col-12 review-img">
                <img src="../assets/review.png" alt="">
            </div>
            <div data-aos="fade-up" data-aos-duration="1000" class="review-content col-lg-6 col-12 px-5">
                <div class="d-flex flex-column justify-content-between align-items-start pe-5">
                    <h4 class="title-desc">GIỚI THIỆU VỀ DPOKER </h4>
                    <p class="reivew-company-content">Được phát triển bởi đội ngũ những người yêu thích Poker truyền thống, DPOKER  được tạo ra như
                        là một nền tảng dựa trên công nghệ blockchain mang tính cách mạng khi kết hợp yếu tố Phi Tập Trung.
                        <br/>
                        <br/>
                        DPOKER sẽ cung cấp trải nghiệm chơi trò chơi gambling trực tuyến hấp dẫn, sáng tạo và an toàn nhất cho tất cả các cộng đồng yêu thích tiền điện tử và poker. Mọi chuyện sẽ trở nên dễ dàng khi bạn có thể tham gia Dpoker với đa số loại tiền điện tử phổ biến hiện nay.
                        <br/>
                        <br/> Chúng tôi sẽ tạo ra một nền tảng Poker phi tập trung sở hữu đa dạng đối tượng người dùng lớn nhất trên thế giới bằng cách xóa bỏ các hạn chế về độ tuổi tham gia, quốc tịch người chơi, vấn đề về luật pháp.
                    </p>
                    <button class="submit-btn">Đăng ký và chơi ngay</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ReviewComponent',
    props: {
        msg: String
    }
}
</script>

<style>
    .review-img img {
        width: 100%;
    }
    .review-content h4 {
        margin-bottom: 20px;
    }
    .review-content .submit-btn {
        margin-left: 1.5rem;
    }
    .reivew-company-content {
        font-family: 'Chakra Petch';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 24px;
        color: #FFFFFF;
        padding-left: 1.5rem;
    }
    /* < PC */
    @media(max-width: 1200px) {
        .review .px-5{
            padding: 0 1.5rem !important;
        }
        .title-desc {
            padding-top: 1rem;
        }
    }
    /* Mobile */
    @media (max-width: 500px) {
        .review-content .pe-5 {
            padding: 0 !important;
        }
        .reivew-company-content {
            padding-left: 0 !important;
        }
        .submit-btn .ms-3 button {
            margin: 10px 0 !important;
        }
    }
</style>