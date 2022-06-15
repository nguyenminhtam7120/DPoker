<template>
    <div class="header">
        <div class="header-pc">
            <div class="d-flex">
                <div class="col-lg-2 main-logo">
                    <img src="./../assets/mainlogo.png" alt="">
                </div>
                <div class="col-lg-10 d-flex justify-content-center align-items-center pe-5">
                    <a v-for="headerItem in menuArr" :key="headerItem" class="" :href="headerItem.href" >{{headerItem.titile}}</a>
                </div>
            </div>
        </div>
        <div class="header-mobile container-fluid py-2">
            <div class="d-flex align-items-center justify-content-between">
                <img src="../assets/mainlogo.png" alt="">
                <div @click="handleMenuBtn()" class="mobile-menu">
                    <img id="btnMenu" ref="btnMenu" src="../assets/menu.png" alt=""/>
                </div>
            </div>
            <div id="mMenuItem" ref="mMenuItem" class="mobile-menu-items" style="display: none">
                <div class="d-flex flex-column text-end">
                    <a v-for="headerItem in menuArr" :key="headerItem" class="" :href="headerItem.href">{{headerItem.titile}}</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data(){
        return {
            menuArr :[
                {
                    titile: "Trang chủ",
                    href: "#",
                    activeClass: "active"

                },
                {
                    titile: "Các yếu tố nổi bật",
                    href: "#outstandElement",
                    activeClass: ""

                },
                {   
                    titile: "Tại sao nên tham gia Dpoker Defi?",
                    href: "#reason",
                    activeClass: ""

                },
                {
                    titile: "Roadmap",
                    href: "#roadMap",
                    activeClass: ""

                },
                // {
                //     titile: "FAQs",
                //     href: "#",
                //     activeClass: ""

                // }
            ]
        }
    },
    components: {
        //FAQsComponent,
    },
    methods: {
        handleMenuBtn() {
            if(this.$refs.mMenuItem.style.display == "none") {
                return this.$refs.mMenuItem.style.display = "block"; 
            } else {
                return this.$refs.mMenuItem.style.display = "none";
            }
        }
    },
    props: {
        msg: String
    }
}
</script>

<style>
    .header {
        background: #030121CC !important;
        position: fixed;
        z-index: 10;
        width: 100%;
    }
    .header-mobile {
        display: none;
    }
    .header img {
        padding-top: 18px;
        padding-bottom: 8px;
        padding-left: 60px;
    }

    a {
        text-decoration: none !important;
        color: #fff !important;
        font-weight: 400;
        font-size: 16px;
        line-height: 26px;
        padding: 48px 25.5px 23px;
    }

    a:hover {
        cursor: pointer;
        color: #FFD601 !important;
    }

    .active {
        color: #FFD601 !important;
    }
    .header-mobile img {
        padding: 0;
        height: 60px;
    }
    .mobile-menu {
        padding: 5px;
    }
    .mobile-menu img {
        height: 50px;
    }
    .mobile-menu-items {
        margin-top: 20px;
        margin-bottom: 20px;
    }
    .mobile-menu-items a {
        padding: 3px 1rem;
        margin: 5px 0;
    }
    /* < PC */
    @media(max-width: 1200px) {
        .header-pc {
            display: none !important;
        }
        .header-mobile {
            display: block !important;
        }
    }
</style>