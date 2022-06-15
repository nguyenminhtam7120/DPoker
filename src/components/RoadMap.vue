<template>
  <div id="roadMap">
    <div class="container">
      <div class="d-flex flex-wrap">
        <div
          class="col-lg-4 col-12 d-flex align-items-center justify-content-center road-map"
        >
          <h4 class="title-desc">ROADMAP</h4>
        </div>
        <div class="col-lg-8 col-12 road-map-items">
          <div
            class="road-map-node d-flex align-items-center justify-content-start py-3"
          >
            <div class="col-lg-2">
              <div class="cirlce">
                <p>01</p>
              </div>
            </div>
            <div class="col-lg-10 road-map-item-content pt-3 ps-3">
              <h6>Quý 3, 2022</h6>
              <div class="d-flex">
                <div>
                  <img src="../assets/right-arrow.png" alt="" />
                </div>
                <div>
                  <p>Cho ra mắt <b>MVP (Mininum Viable Product)</b> nội bộ</p>
                </div>
              </div>
              <div class="d-flex">
                <div>
                  <img src="../assets/right-arrow.png" alt="" />
                </div>
                <div>
                  <p>
                    Ra mắt phiên bản thử nghiệm quy <b>mô 1000 người chơi</b>
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div
            class="road-map-node d-flex align-items-center justify-content-start py-3 road-map-node-center"
          >
            <div class="col-lg-2">
              <div class="cirlce">
                <p>02</p>
              </div>
            </div>
            <div class="col-lg-10 road-map-item-content pt-3 ps-3">
              <h6>Quý 4, 2022</h6>
              <div class="d-flex">
                <div>
                  <img src="../assets/right-arrow.png" alt="" />
                </div>
                <div>
                  <p>Kêu gọi quỹ đầu tư</p>
                </div>
              </div>
              <div class="d-flex">
                <div>
                  <img src="../assets/right-arrow.png" alt="" />
                </div>
                <div>
                  <p>
                    Ra mắt phiên bản <b>MVP Public</b> và hạn chế số lượng người
                    tham gia trải nghiệm
                  </p>
                </div>
              </div>
              <div class="d-flex">
                <div>
                  <img src="../assets/right-arrow.png" alt="" />
                </div>
                <div>
                  <p>
                    Hoàn tất quy trình chỉnh sửa lỗi từ phiên bản
                    <b>MVP Public</b>
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div
            class="road-map-node d-flex align-items-center justify-content-start py-3"
          >
            <div class="col-lg-2">
              <div class="cirlce">
                <p>03</p>
              </div>
            </div>
            <div class="col-lg-10 road-map-item-content pt-3 ps-3">
              <h6>Quý 1, 2023</h6>
              <div class="d-flex">
                <div>
                  <img src="../assets/right-arrow.png" alt="" />
                </div>
                <div>
                  <p>Ra mắt phiên bản website chính thức của <b>DPoker</b></p>
                </div>
              </div>
              <div class="d-flex">
                <div>
                  <img src="../assets/right-arrow.png" alt="" />
                </div>
                <div>
                  <p>
                    Ra mắt <b>ứng dụng di động</b> cho 2 hệ điều hành
                    Iphone/Android
                  </p>
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
  name: "RoadMapComponent",
  props: {
    msg: String,
  },
  computed: {},
};
</script>

<style>
#roadMap {
  padding: 70px 0;
  background-image: url("../assets/final-bg-3.png");
  background-repeat: no-repeat;
  background-size: 100% 100%;
}
.road-map h4 {
  margin: 0;
}
.road-map-items p {
  margin: 0;
}
.road-map-items .col-lg-2 .cirlce {
  background-color: #032558;
  width: 100px;
  height: 100px;
  border-radius: 50%;
  text-align: center;
  line-height: 100px;
  color: #fff;
  font-size: 28px;
  font-weight: 600;
}
.road-map-item-content h6 {
  font-family: "Chakra Petch";
  font-style: normal;
  font-weight: 700;
  font-size: 22px;
  line-height: 110%;
  color: #ffd601;
}
.road-map-item-content p {
  font-family: "Chakra Petch";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 28px;
  color: #ffffff;
  opacity: 0.8;
  padding-right: 120px;
}
.road-map-item-content img {
  width: 13px;
  margin-right: 9px;
}
.road-map-node-center {
  margin: 130px 0 130px 100px;
}
.road-map-node-center .cirlce {
  background-color: #0451a1 !important;
}
/* < PC */
@media (max-width: 1200px) {
  .road-map-item-content {
    margin-left: 20px;
  }
  .road-map-item-content p {
    padding: 0;
  }
  .road-map-node-center {
    margin: 20px 0;
  }
  .road-map-items {
    margin-top: 30px;
  }
}
/* Tablet */
@media (min-width: 768px) and (max-width: 1200px) {
  .road-map-items {
    padding: 0 3rem;
  }
}
/* Mobile */
@media (max-width: 767px) {
  .road-map h4 {
    text-align: center !important;
  }
  .road-map-items {
    padding: 10px;
  }
  .road-map-node-center {
    margin: 0;
  }
  .title-desc {
    text-align: center;
  }
  .road-map-node {
    flex-wrap: wrap !important;
  }
  .road-map h4.pe-5 {
    padding-right: 0 !important;
  }
}
</style>
