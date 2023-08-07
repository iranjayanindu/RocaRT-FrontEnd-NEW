<template>
    <div class="main home-page">
        <div class="intro-section pt-3 pb-3 mb-2">
            <div class="container">
                <div class="row">
                    <div class="col-lg-8">
                        <div class="intro-slider-container slider-container-ratio mb-2 mb-lg-0">
                            <div class="swiper-carousel swiper-1 intro-slider">
                                <div v-swiper:swiper1="carouselSetting1">
                                    <div class="swiper-wrapper">
                                        <div class="swiper-slide">
                                            <div class="intro-slide">
                                                <figure class="slide-image mb-0">
                                                    <picture>
                                                        <source
                                                            media="(max-width: 480px)"
                                                            srcset="~/static/images/home/sliders/slide-1-480w.jpg"
                                                        />
                                                        <img
                                                            v-lazy="'./images/home/sliders/slide-1.jpg'"
                                                            alt="banner"
                                                        />
                                                    </picture>
                                                </figure>

                                                <div class="intro-content">
                                                    <h3
                                                        class="intro-subtitle text-primary"
                                                    >Daily Deals</h3>

                                                    <h1 class="intro-title">
                                                        AirPods
                                                        <br />Earphones
                                                    </h1>

                                                    <div class="intro-price">
                                                        <sup>Today:</sup>
                                                        <span class="text-primary">
                                                            $247
                                                            <sup>.99</sup>
                                                        </span>
                                                    </div>

                                                    <nuxt-link
                                                        to="/shop/sidebar/4cols"
                                                        class="btn btn-primary btn-round"
                                                    >
                                                        <span>Click Here</span>
                                                        <i class="icon-long-arrow-right"></i>
                                                    </nuxt-link>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="swiper-slide">
                                            <div class="intro-slide">
                                                <figure class="slide-image mb-0">
                                                    <picture>
                                                        <source
                                                            media="(max-width: 480px)"
                                                            srcset="~/static/images/home/sliders/slide-2-480w.jpg"
                                                        />
                                                        <img
                                                            v-lazy="'./images/home/sliders/slide-2.jpg'"
                                                            alt="banner"
                                                        />
                                                    </picture>
                                                </figure>

                                                <div class="intro-content">
                                                    <h3
                                                        class="intro-subtitle text-primary"
                                                    >Deals and Promotions</h3>

                                                    <h1 class="intro-title">
                                                        Echo Dot
                                                        <br />3rd Gen
                                                    </h1>

                                                    <div class="intro-price">
                                                        <sup class="intro-old-price">$49,99</sup>
                                                        <span class="text-primary">
                                                            $29
                                                            <sup>.99</sup>
                                                        </span>
                                                    </div>

                                                    <nuxt-link
                                                        to="/shop/sidebar/4cols"
                                                        class="btn btn-primary btn-round"
                                                    >
                                                        <span>Click Here</span>
                                                        <i class="icon-long-arrow-right"></i>
                                                    </nuxt-link>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="swiper-dots swiper-dots-inner"></div>
                                <div class="swiper-nav nav-inside">
                                    <div class="swiper-prev">
                                        <i class="icon-angle-left"></i>
                                    </div>
                                    <div class="swiper-next">
                                        <i class="icon-angle-right"></i>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-4">
                        <div class="intro-banners">
                            <div class="banner mb-lg-2">
                                <a href="#">
                                    <img
                                        src="~/static/images/home/banners/banner-1.jpg"
                                        width="370"
                                        height="120"
                                        alt="Banner"
                                    />
                                </a>

                                <div class="banner-content">
                                    <h4 class="banner-subtitle d-lg-none d-xl-block">
                                        <a href="#">Top Product</a>
                                    </h4>

                                    <h3 class="banner-title">
                                        <a href="#">
                                            Edifier
                                            <br />Stereo Bluetooth
                                        </a>
                                    </h3>

                                    <a href="#" class="banner-link">
                                        Shop Now
                                        <i class="icon-long-arrow-right"></i>
                                    </a>
                                </div>
                            </div>

                            <div class="banner mb-lg-2">
                                <a href="#">
                                    <img
                                        src="~/static/images/home/banners/banner-2.jpg"
                                        width="370"
                                        height="120"
                                        alt="Banner"
                                    />
                                </a>

                                <div class="banner-content">
                                    <h4 class="banner-subtitle d-lg-none d-xl-block">
                                        <a href="#">Clearance</a>
                                    </h4>

                                    <h3 class="banner-title">
                                        <a href="#">
                                            GoPro - Fusion 360
                                            <span>Save $70</span>
                                        </a>
                                    </h3>

                                    <a href="#" class="banner-link">
                                        Shop Now
                                        <i class="icon-long-arrow-right"></i>
                                    </a>
                                </div>
                            </div>

                            <div class="banner mb-0">
                                <a href="#">
                                    <img
                                        src="~/static/images/home/banners/banner-3.jpg"
                                        width="370"
                                        height="120"
                                        alt="Banner"
                                    />
                                </a>

                                <div class="banner-content">
                                    <h4 class="banner-subtitle d-lg-none d-xl-block">
                                        <a href="#">Featured</a>
                                    </h4>

                                    <h3 class="banner-title">
                                        <a href="#">
                                            Apple Watch 4
                                            <span>Our Hottest Deals</span>
                                        </a>
                                    </h3>

                                    <a href="#" class="banner-link">
                                        Shop Now
                                        <i class="icon-long-arrow-right"></i>
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <special-collection :products="products" v-if="loaded"></special-collection>

        <div class="mb-7"></div>

        <div class="container">
            <div
                class="cta cta-border cta-border-image mb-5 mb-lg-7"
                v-lazy:background-image="'./images/home/bg-1.jpg'"
            >
                <div class="cta-border-wrapper bg-white">
                    <div class="row justify-content-center">
                        <div class="col-md-11 col-xl-11">
                            <div class="cta-content">
                                <div class="cta-heading">
                                    <h3 class="cta-title text-right">
                                        <span class="text-primary">New Deals</span>
                                        <br />Start Daily at 12pm e.t.
                                    </h3>
                                </div>

                                <div class="cta-text">
                                    <p>
                                        Get
                                        <span
                                            class="text-dark font-weight-normal"
                                        >FREE SHIPPING* & 5% rewards</span> on
                                        <br />every order with Molla Theme rewards program
                                    </p>
                                </div>

                                <a href="javascript:;" class="btn btn-primary btn-round">
                                    <span>Add to Cart for $50.00/yr</span>
                                    <i class="icon-long-arrow-right"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <deal-collection v-if="loaded" :products="dealProducts"></deal-collection>

        <div class="container">
            <div class="swiper-carousel brands-slider swiper-2 mb-3">
                <div v-swiper:swiper2="carouselSetting2">
                    <div class="swiper-wrapper">
                        <div
                            class="swiper-slide"
                            v-for="(brand, index) in homeData.brands"
                            :key="index"
                        >
                            <a href="#" class="brand">
                                <img
                                    :src="brand.image"
                                    class="bg-white"
                                    alt="Brand"
                                    :width="brand.width"
                                    :height="brand.height"
                                />
                            </a>
                        </div>
                    </div>
                </div>
                <div class="swiper-nav">
                    <div class="swiper-prev">
                        <i class="icon-angle-left"></i>
                    </div>
                    <div class="swiper-next">
                        <i class="icon-angle-right"></i>
                    </div>
                </div>
            </div>
        </div>
        <div class="container">
            <hr class="mt-3 mb-6" />
        </div>
        <trendy-collection :products="topProducts" v-if="loaded"></trendy-collection>
        <div class="container">
            <hr class="mt-5 mb-6" />
        </div>
        <top-collection :products="topProducts" v-if="loaded"></top-collection>

        <div class="icon-boxes-container mb-2 bg-transparent">
            <div class="container">
                <div class="row">
                    <div class="col-sm-6 col-lg-3">
                        <div class="icon-box icon-box-side">
                            <span class="icon-box-icon text-dark">
                                <i class="icon-rocket"></i>
                            </span>
                            <div class="icon-box-content">
                                <h3 class="icon-box-title">Free Shipping</h3>

                                <p>Orders $50 or more</p>
                            </div>
                        </div>
                    </div>

                    <div class="col-sm-6 col-lg-3">
                        <div class="icon-box icon-box-side">
                            <span class="icon-box-icon text-dark">
                                <i class="icon-rotate-left"></i>
                            </span>

                            <div class="icon-box-content">
                                <h3 class="icon-box-title">Free Returns</h3>

                                <p>Within 30 days</p>
                            </div>
                        </div>
                    </div>

                    <div class="col-sm-6 col-lg-3">
                        <div class="icon-box icon-box-side">
                            <span class="icon-box-icon text-dark">
                                <i class="icon-info-circle"></i>
                            </span>

                            <div class="icon-box-content">
                                <h3 class="icon-box-title">Get 20% Off 1 Item</h3>

                                <p>when you sign up</p>
                            </div>
                        </div>
                    </div>

                    <div class="col-sm-6 col-lg-3">
                        <div class="icon-box icon-box-side">
                            <span class="icon-box-icon text-dark">
                                <i class="icon-life-ring"></i>
                            </span>

                            <div class="icon-box-content">
                                <h3 class="icon-box-title">We Support</h3>

                                <p>24/7 amazing services</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="container">
            <div
                class="cta cta-separator cta-border-image cta-half mb-0"
                v-lazy:background-image="'./images/home/bg-2.jpg'"
            >
                <div class="cta-border-wrapper bg-white">
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="cta-wrapper cta-text text-center">
                                <h3 class="cta-title">Shop Social</h3>

                                <p
                                    class="cta-desc"
                                >Donec nec justo eget felis facilisis fermentum. Aliquam porttitor mauris sit amet orci.</p>

                                <div
                                    class="social-icons social-icons-colored justify-content-center"
                                >
                                    <a
                                        href="#"
                                        class="social-icon social-facebook"
                                        title="Facebook"
                                        target="_blank"
                                    >
                                        <i class="icon-facebook-f"></i>
                                    </a>
                                    <a
                                        href="#"
                                        class="social-icon social-twitter"
                                        title="Twitter"
                                        target="_blank"
                                    >
                                        <i class="icon-twitter"></i>
                                    </a>
                                    <a
                                        href="#"
                                        class="social-icon social-instagram"
                                        title="Instagram"
                                        target="_blank"
                                    >
                                        <i class="icon-instagram"></i>
                                    </a>
                                    <a
                                        href="#"
                                        class="social-icon social-youtube"
                                        title="Youtube"
                                        target="_blank"
                                    >
                                        <i class="icon-youtube"></i>
                                    </a>
                                    <a
                                        href="#"
                                        class="social-icon social-pinterest"
                                        title="Pinterest"
                                        target="_blank"
                                    >
                                        <i class="icon-pinterest"></i>
                                    </a>
                                </div>
                            </div>
                        </div>

                        <div class="col-lg-6">
                            <div class="cta-wrapper text-center">
                                <h3 class="cta-title">Get the Latest Deals</h3>

                                <p class="cta-desc">
                                    and
                                    <br />receive
                                    <span class="text-primary">$20 coupon</span> for first shopping
                                </p>

                                <form action="#">
                                    <div class="input-group">
                                        <input
                                            type="email"
                                            class="form-control"
                                            placeholder="Enter your Email Address"
                                            aria-label="Email Adress"
                                            required
                                        />
                                        <div class="input-group-append">
                                            <button
                                                class="btn btn-primary btn-rounded"
                                                type="submit"
                                            >
                                                <i class="icon-long-arrow-right"></i>
                                            </button>
                                        </div>
                                    </div>
                                </form>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { mapGetters } from 'vuex';

import CountDown from '~/components/elements/CountDown';
import SpecialCollection from '~/components/partial/home/SpecialCollection';
import DealCollection from '~/components/partial/home/DealCollection';
import TrendyCollection from '~/components/partial/home/TrendyCollection';
import TopCollection from '~/components/partial/home/TopCollection';
import NewsletterModal from '~/components/elements/modals/NewsletterModal';

import Repository, { baseUrl } from '~/repositories/repository.js';
import { attrFilter } from '~/utilities/common';
import {
    carouselSettingSingle,
    carouselSettingDefault
} from '~/utilities/carousel';
import { homeData } from '~/utilities/data';

export default {
    components: {
        CountDown,
        TopCollection,
        DealCollection,
        TrendyCollection,
        SpecialCollection
    },
    data: function() {
        return {
            loaded: false,
            products: [],
            dealProducts: [],
            topProducts: [],
            carouselSetting1: {
                ...carouselSettingSingle,
                pagination: {
                    el: '.swiper-1 .swiper-dots',
                    clickable: true
                },
                navigation: {
                    nextEl: '.intro-slider-container .swiper-next',
                    prevEl: '.intro-slider-container .swiper-prev'
                }
            },
            carouselSetting2: {
                ...carouselSettingDefault,
                slidesPerView: 6,
                spaceetween: 0,
                navigation: {
                    nextEl: '.brands-slider .swiper-next',
                    prevEl: '.brands-slider .swiper-prev'
                },
                breakpoints: {
                    992: {
                        slidesPerView: 5
                    },
                    768: {
                        slidesPerView: 4
                    },
                    576: {
                        slidesPerView: 3
                    },
                    480: {
                        slidesPerView: 2
                    }
                }
            },
            homeData: homeData
        };
    },
    computed: {
        ...mapGetters('demo', ['newsletterShow'])
    },
    created: function() {
        this.getProducts();
    },
    mounted: function() {
        if (this.newsletterShow) {
            setTimeout(() => {
                if (this.$route.path == '/' && this.newsletterShow) {
                    this.$modal.show(
                        NewsletterModal,
                        {},
                        { width: '970', height: 'auto', adaptive: true }
                    );
                }
            }, 8000);
        }
    },
    methods: {
        getProducts: async function() {
            this.loaded = false;
            await Repository.get(`${baseUrl}/demo3`)
                .then(response => {
                    this.products = response.data.products;
                    this.dealProducts = attrFilter(
                        this.products,
                        'until'
                    ).slice(0, 2);
                    this.topProducts = attrFilter(this.products, 'top');
                    this.loaded = true;
                })
                .catch(error => ({ error: JSON.stringify(error) }));
        }
    }
};
</script>