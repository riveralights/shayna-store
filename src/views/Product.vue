<template>
  <div class="product">
    <HeaderShayna/>
    <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="breadcrumb-text product-more text-left">
                        <router-link to="/"><i class="fa fa-home"></i> Home </router-link>
                        <span>Detail</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="product-pic-zoom">
                                <img class="product-big-img" :src="default_photo" alt="gambar mickey" />
                            </div>
                            <div class="product-thumbs">
                                <carousel class="product-thumbs-track ps-slider" :dots="false" :nav="false" :items="3">
                                    <div class="pt active" @click="changeImage(thumbs[0])" :class="thumbs[0] == default_photo ? 'active' : '' ">
                                        <img src="img/mickey-shirt-0.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(thumbs[1])" :class="thumbs[1] == default_photo ? 'active' : '' ">
                                        <img src="img/mickey-shirt-1.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(thumbs[2])" :class="thumbs[2] == default_photo ? 'active' : '' ">
                                        <img src="img/mickey-shirt-2.jpg" alt="" />
                                    </div>
                                </carousel>
                            </div>
                        </div>
                        <div class="col-lg-6">
                            <div class="product-details">
                                <div class="pd-title text-left mb-3">
                                    <span>T-Shirt</span>
                                    <h3 class="mt-2">MICKEY MOUSE ©DISNEY T-SHIRT</h3>
                                </div>
                                <div class="pd-desc text-justify">
                                    <p>
                                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error
                                        officia. Rem aperiam laborum voluptatum vel, pariatur modi hic provident eum
                                        iure natus quos non a sequi, id accusantium! Autem.
                                    </p>
                                    <p>
                                        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus quisquam
                                        animi, commodi, nihil voluptate nostrum neque architecto illo officiis
                                        doloremque et corrupti cupiditate voluptatibus error illum. Commodi expedita
                                        animi nulla aspernatur.
                                        Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint
                                        molestiae accusamus voluptates ex tempora illum sit perspiciatis. Nostrum dolor
                                        tenetur amet, illo natus magni veniam quia sit nihil dolores.
                                        Commodi ratione distinctio harum voluptatum velit facilis voluptas animi non
                                        laudantium, id dolorem atque perferendis enim ducimus? A exercitationem
                                        recusandae aliquam quod. Itaque inventore obcaecati, unde quam
                                        impedit praesentium veritatis quis beatae ea atque perferendis voluptates velit
                                        architecto?
                                    </p>
                                    <h4 class="mt-4">$495.00</h4>
                                </div>
                                <div class="quantity">
                                    <a href="shopping-cart.html" class="primary-btn pd-cart">Add To Cart</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Product Shop Section End -->
    <RelatedProduct/>
    <FooterShayna/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import carousel from 'vue-owl-carousel'
import HeaderShayna from '@/components/HeaderShayna.vue'
import RelatedProduct from '@/components/RelatedProduct.vue'
import FooterShayna from '@/components/FooterShayna.vue'

export default {
  name: 'Product',
  components: {
    HeaderShayna,
    carousel,
    FooterShayna,
    RelatedProduct,
  },
  data(){
    return{
      default_photo: "img/mickey-shirt-0.jpg",
      thumbs: [
        'img/mickey-shirt-0.jpg',
        'img/mickey-shirt-1.jpg',
        'img/mickey-shirt-2.jpg',
      ]
    }
  },
  methods: {
    changeImage(urlImage) {
      this.default_photo = urlImage
    }
  }
}
</script>

<style scoped>
.product-thumbs .pt {
  margin-right: 14px;
}
</style>
