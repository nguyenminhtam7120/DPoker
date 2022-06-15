<template>
    <div class="container">
        <div class="footer">
        <img src="./../assets/mainlogo.png" alt="">
        <div class="d-flex flex-wrap">
            <div class="col-lg-7 col-12 d-flex flex-wrap px-4">
                <div class="col-sm-6 d-flex flex-column justify-content-center nav-items">
                    <a href="#">TRANG CHỦ</a>
                    <a href="#">CÁC YẾU TỐ NỔI BẬT</a>
                    <a href="#">TẠI SAO NÊN THAM GIA DPOKER</a>
                    <a href="#">ROADMAP</a>
                    <a href="#">FAQs</a>
                </div>
                <div class="col-sm-6 d-flex align-items-center footer-tags">
                    <ul>
                        <li><span>White paper</span></li>
                        <li><span>Điều khoản dịch vụ</span></li>
                        <li><span>Chính sách dự án</span></li>
                        <li><span>Trách nhiệm người chơi</span></li>
                    </ul>
                </div>
            </div>
            <div class="col-lg-5 col-12 px-4 footer-contact">
                <h3>LIÊN HỆ</h3>
                <div class="contact-box">
                    <form action="#">
                        <div class="d-flex pb-2">
                            <label for="fullName">Họ và tên: </label>
                            <input type="text" id="fullName">
                        </div>
                        <div class="d-flex py-2">
                            <label for="email">Email: </label>
                            <input type="text" id="email">
                        </div>
                        <div class="d-flex pt-2">
                            <label for="question">Câu hỏi: </label>
                            <input type="text" id="question">
                        </div>
                    </form>
                </div>
                <div class="d-flex justify-content-end btn-submit">
                    <button>Gửi</button>
                </div>
            </div>
        </div>
        <div class="footer-desc d-flex flex-wrap px-4">
            <div class="col-lg-7 col-12 pe-5">
                <h4>DPOKER</h4>
                <p class="pe-5">Dự án không được thiết kế với mục đích đánh bạc. Thay vào đó, nó tập trung vào tinh thần thể thao bằng cách chỉ cung cấp các giải đấu poker, sit & go và các trò chơi cạnh tranh tương tự. </p>
            </div>
            <div class="col-lg-5 col-12 ps-5 footer-update">
                <h3>CẬP NHẬT THÔNG TIN TẠI ĐÂY:</h3>
                <div class="social-media d-flex">
                    <img src="../assets/youtube.png" alt="">
                    <img src="../assets/telegram.png" alt="">
                    <img src="../assets/facebook.png" alt="">
                    <img src="../assets/twitter.png" alt="">
                    <img src="../assets/discord.png" alt="">
                </div>
            </div>
        </div>
    </div>
    <div class="trainslate px-4 mt-5">
        <div class="d-flex justify-content-end position-relative">
            <div @click="handleShowTranslate()" class="d-flex trainslate-box align-items-center justify-content-between px-3">
                <div class="d-flex align-items-center">
                    <img src="../assets/vietnam.png" alt="">
                    <p>Việt Nam</p>
                </div>
                <div class="down-arrow">
                    <img src="../assets/down-arrow.png" alt="">
                </div>
            </div>
            <div id="boxTranslate" ref="boxTranslate" class="box-translate-item" style="display: none">
                <div>
                    <div class="d-flex trainslate-box align-items-center px-3">
                        <img src="../assets/vietnam.png" alt="">
                        <p>Việt Nam</p>
                        <div class="down-arrow">
                        </div>
                    </div>
                    <div class="d-flex trainslate-box align-items-center px-3">
                        <img src="../assets/united-kingdom.png" alt="">
                        <p>English</p>
                        <div class="down-arrow">
                        </div>
                    </div>
                    <div class="d-flex trainslate-box align-items-center px-3">
                        <img src="../assets/japan.png" alt="">
                        <p>Japanese</p>
                        <div class="down-arrow">
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
    name: 'FooterComponent',
    methods: {
        handleShowTranslate() {
            if(this.$refs.boxTranslate.style.display == "none") {
                return this.$refs.boxTranslate.style.display = "block"; 
            } else {
                return this.$refs.boxTranslate.style.display = "none";
            }
        }
    },
    props: {
        msg: String
    }
}
</script>

<style>
    .footer {
        margin-top: 35px;
    }
    .nav-items a {
        font-weight: 400;
        font-size: 17px;
        line-height: 36px;
        letter-spacing: -0.165px;
        padding: 0;
        margin: 3px 0;
    }
    .footer > img {
        margin-bottom: 48px;
    }
    .footer span {
        background: #00A3FF;
        max-width: 100%;
        margin: 10px 0;
        border-radius: 5px;
        padding: 5px 10px;
        font-weight: 500;
        font-size: 16px;
        line-height: 24px;
        text-align: center;
        letter-spacing: 0.02em;
    }
    .footer span:hover {
        cursor: pointer;
        background: #FFD601;
    }
    .footer li {
        margin: 30px 0;
    }
    li {
        list-style-type: none;
    }
    .footer-desc {
        margin-top: 48px;
    }
    .footer-desc h4 {
        color: #FFD601;
        font-weight: 700;
        font-size: 16px;
        line-height: 20px;
    }
    .footer-desc p {
        color: #fff;
    }
    .footer h3 {
        font-size: 20px;
        color: #fff;
        font-weight: 700;
        font-size: 20px;
        line-height: 26px;
    }
    .social-media img {
        width: 28px;
        height: 28px;
        margin: 20px 18px 0;
        transition: transform 2;
    }
    .social-media img:hover {
        cursor: pointer;
        transform: scale(1.2);
    }
    .contact-box {
        background-color: #fff;
        padding: 20px;
    }
    .btn-submit button {
        width: 95px;
        height: 38px;
        background-color: #FFD601;
        margin-top: 10px;
        border-radius: 5px;
        font-weight: 600;
        line-height: 24px;
        text-align: center;
        letter-spacing: 0.02em;
        color: #202020;
        transition: transform 0.3;
    }
    .btn-submit button:hover {
        cursor: pointer;
        transform: scale(1.05);
    }
    .contact-box input {
        outline: none;
        padding: 0 5px;
        margin-left: 5px;
        border-bottom: 1px solid #fff;
    }
    .contact-box input:focus {
        border-bottom: 1px solid #ccc;
    }
    .form-select-vue {
        width: 200px;
        margin-bottom: 65px;
    }
    .form-select-vue select {
        border: none !important;
        outline: none !important;
    }
    .form-select-vue select option {
        background-color: none !important;
    }
    .contact-box input {
        width: 80%;
    }
    .trainslate {
        padding-bottom: 30px;
    }
    .trainslate-box {
        width: 200px;
    }
    .trainslate-box img {
        height: 40px;
    }
    .trainslate-box p {
        margin: 0;
        color: #fff;
        padding: 0 10px;
        font-style: normal;
        font-weight: 400;
        font-size: 17px;
        line-height: 40px;
    }
    .down-arrow img {
        height: 20px !important;
    }
    .box-translate-item {
        position: absolute;
        top: -300%;
        z-index: 10;
        background: #030121CC !important;
    }
    /* < PC */
    @media(max-width: 1200px) {
        .footer > .d-flex > .pe-5{
            padding-right: 10px !important;
        } 
        .footer-tags {
            justify-content: end !important;
        }
        .footer-tags ul {
            padding-left: 10px !important;
        }
        .footer-tags ul li {
            text-align: right !important;
        }
        .footer-contact .ps-5{
            padding-left: 40px !important;
        }
    }
    /* < PC */
    @media(max-width: 1200px) {
        .footer-desc .ps-5{
            padding: 0 !important;
        }
        .social-media img {
            margin: 5px 10px !important;
        }
        .footer-update {
            margin-top: 20px;
        }
    }
    /* Mobile */
    @media(max-width:767px) {
        .footer-tags ul {
            padding: 0 !important;
        }
        .footer > img {
            padding-left: 0.8rem;
        }
        .review-content .submit-btn {
            margin-left: 0;
        }
        .review-content .pe-5 {
            padding-right: 0 !important;
        }
    }
    @media(max-width: 513px) {
        .footer-tags ul li{
            text-align: left !important;
        }
    }
</style>