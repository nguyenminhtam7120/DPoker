<template>
  <div class="faq">
    <div class="container">
      <h4 data-aos="zoom-in" data-aos-duration="1000" class="title-desc text-center">FAQs</h4>
      <div class="fag-box d-flex justify-content-center">
        <div class="faq-list-items col-lg-8 col-md-10 col-11">
          <div v-for="faqItem in listFAQs" v-bind:key="faqItem.id">
            <div
              data-aos="zoom-in" data-aos-duration="1000"
              @click="showAnswers(faqItem.id);"
              class="faq-item p-3 my-4 d-flex align-items-center justify-content-between"
            >
              <div class="d-flex align-items-center">
                <p class="col-2 faq-cirlce">{{ faqItem.id }}</p>
                <h6 class="px-4">{{ faqItem.question }}</h6>
              </div>
              <img v-if="showActive === faqItem.id" src="../assets/up-arrow.png" alt="" />
              <img v-else src="../assets/down-arrow.png" alt="" />
            </div>
            <div class="full-width" v-if="showActive === faqItem.id">
              <h6 :id="faqItem.id">
                {{ faqItem.answer }}
              </h6>
            </div>
          </div>
        </div>
      </div>
      <h4 data-aos="zoom-in" data-aos-duration="1000" class="title-desc text-center title-special pb-2">MEDIA SHOUTOUTS</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "FAQsComponent",
  methods: {
    showAnswers(idFaq) {
      if (idFaq === this.showActive) {
        this.showActive = 0;
      } else {
        this.showActive = idFaq;
      }
    },
  },
  data() {
    return {
      showActive: 0,
      listFAQs: [
        {
          id: 1,
          question: "DPOKER là gì?",
          answer:
            "DPOKER là một nền tảng nền tảng Poker phi tập trung với sự kết hợp của công nghệ Blockchain và DeFi",
        },
        {
          id: 2,
          question: "Các đồng tiền sẽ được sử dụng để thanh toán?",
          answer: "Content for tab 2",
        },
        {
          id: 3,
          question: "Làm sao rút tiền từ hệ thống ra ngoài?",
          answer: "Content for tab 3",
        },
        {
          id: 4,
          question: "Các token nào sẽ được sử dụng?",
          answer: "Content for tab 4",
        },
        {
          id: 5,
          question: "Tương lai sẽ có token riêng cho DPOKER không?",
          answer: "Content for tab 5",
        },
        {
          id: 6,
          question: "Tôi phải sử dụng ví điện tử nào để tham gia DPOKER?",
          answer: "Content for tab 6",
        },
        {
          id: 7,
          question: "Số tiền tối thiểu để rút tiền và gửi tiền là bao nhiêu ?",
          answer: "Content for tab 7",
        },
        {
          id: 8,
          question: "Tôi có thể nhận được 100% số tiền cược của mình ?",
          answer: "Content for tab 8",
        },
        {
          id: 9,
          question: "Tôi có thể chơi DPOKER với BNB hay không ?",
          answer: "Content for tab 9",
        },
        {
          id: 10,
          question:
            "Số tiền tối đa tôi có thể đặt cược khi chơi DPOKER là bao nhiêu ?",
          answer: "Content for tab 10",
        },
      ],
    };
  },
  props: {},
};
</script>

<style>
.full-width > h6 {
  color: #fff;
  padding: 0 90px;
  line-height: 24px;
}
.faq {
  padding: 70px 0 0;
  background-image: url("../assets/final-bg-5.png");
  background-size: 100% 100%;
}
.faq-item {
  color: #fff;
  background-color: #07093e;
}
.faq-item:hover {
  cursor: pointer;
}
.faq-item h6 {
  margin: 0 0;
}
.faq-cirlce {
  font-size: 24px;
  font-weight: 700;
  text-align: center;
  line-height: 50px;
}
.faq-list-items img {
  height: 22px;
}
.faq-list-items p {
  height: 50px !important;
  width: 50px !important;
  border-radius: 50%;
  background: #00a3ff;
  margin: 0 !important;
}
.title-special {
  margin-bottom: 0 !important;
  margin-top: 120px;
}
</style>
