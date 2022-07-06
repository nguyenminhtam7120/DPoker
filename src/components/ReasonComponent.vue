<template>
  <div id="reason">
    <div class="container">
      <div class="reason-choose">
        <h4 data-aos="zoom-in" data-aos-duration="1000" class="title-desc text-center">TẠI SAO NÊN THAM GIA DPOKER</h4>
        <div class="d-flex justify-content-lg-center flex-wrap">
          <div
            v-for="itemReason in listReasons"
            v-bind:key="itemReason.id"
            class="col-lg-4 col-md-6 col-12 px-4 pt-5"
          >
            <div class="reasion-card text-center" data-aos="zoom-in" data-aos-duration="1500">
              <img
                :src="require('../assets/' + itemReason.imgURL)"
                :key="itemReason.id"
                alt=""
              />
              <div class="reasion-card-desc px-5">
                <h5 class="px-4">{{ itemReason.title }}</h5>
                <div class="an">
                  <p class="px-3">{{ itemReason.desc }}</p>
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
  name: "ReasonComponent",
  data() {
    return {
      listReasons: [
        {
          id: 1,
          imgURL: "frame-1.png",
          title: "Tính phi tập trung",
          desc: "Với cấu trúc phi tập trung người chơi sẽ hoàn toàn yên tâm được về sự minh bạch với chi phí tốt nhất.",
        },
        {
          id: 2,
          imgURL: "frame-2.png",
          title: "Đảm bảo lợi ích cho người chơi",
          desc: "Là công trung gian, Dpoker sẽ đảm bảo lợi nhuận trực tiếp của người chơi, khoản lợi nhuận này sẽ đến từ chi phí giao dịch giữa người chơi và nhà cái. ",
        },
        {
          id: 3,
          imgURL: "frame-5.png",
          title: "Cộng đồng người chơi đông với quy mô toàn thế giới",
          desc: "Với hệ sinh thái rộng lớn và số lượng người chơi mang tính toàn cầu. Chính vì vậy, bạn có thể chơi với bất cứ ai.",
        },
        {
          id: 4,
          imgURL: "frame-3.png",
          title: "Đa dạng phương thức nạp và rút",
          desc: "Nhanh chóng tiện lợi hỗ trợ 24/7 với đa dạng cổng giao dịch. Tiết kiệm chi phí, thời gian nhờ vào tốc độ xử lý giao dịch và công nghệ Blockchain",
        },
        {
          id: 5,
          imgURL: "frame-4.png",
          title: "Hệ sinh thái đa dạng",
          desc: "Hero Book, Dragon Pool và tương lai sẽ có thêm rất nhiều Game Fi NFT được tích hợp vào hệ sinh thái.",
        },
      ],
    };
  },
  props: {
    msg: String,
  },
};
</script>

<style>
#reason {
  background: url("../assets/final-bg-4.png");
  background-size: 100% 100%;
  background-repeat: no-repeat;
  padding: 90px 0;
}
.reasion-card {
  background: rgba(250, 250, 250, 0.05);
  backdrop-filter: blur(80px);
  min-height: 340px;
  transition: transform 0.3s;
}
.reasion-card:hover {
  cursor: pointer;
  transform: scale(1.05);
}
.reasion-card img {
  padding: 36px 0;
}
.reasion-card-desc .an {
  -webkit-line-clamp: 4;
}
.reasion-card-desc h5 {
  font-family: "Chakra Petch";
  font-style: normal;
  font-weight: 700;
  font-size: 22px;
  line-height: 130%;
  text-align: center;
  color: #ffd601;
}
.reasion-card-desc p {
  font-family: "Chakra Petch";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 18px;
  text-align: center;
  color: #ffffff;
  opacity: 0.8;
}
/* Tablet */
@media (max-width: 1200px) {
  .reasion-card .px-5 {
    padding: 0 !important;
  }
}
</style>
