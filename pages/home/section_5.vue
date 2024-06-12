<template>
  <div class="section_5" id="testimonial">
    <div class="container">
      <div class="row justify-content-center mb-5">
        <div class="new_product"><i>TESTIMONIAL</i></div>
      </div>
      <div class="content_carousel">
        <carousel
          :autoplay="true"
          :nav="false"
          :dots="true"
          :loop="true"
          :items="1"
          :responsive="responsiveOptions"
          :slideSpeed="2000"
        >
          <div v-for="item in dataContent" :key="item.id">
            <div class="card">
              <div class="card-body">
                <b-list-group-item class="item_list_head">
                  <b-avatar
                    variant="warning"
                    :text="item.image"
                    class="mr-3"
                  ></b-avatar>
                  <span class="mr-auto name_test">{{ item.title }}</span>
                </b-list-group-item>
                <b-list-group-item class="item_list_head">
                  <div class="stars mb-2">
                    <i v-for="star in stars" :key="star" class="fa fa-star"></i>
                  </div>
                  <div class="text-card">{{ item.desc }}</div>
                </b-list-group-item>
              </div>
            </div>
          </div>
        </carousel>
      </div>
    </div>
  </div>
</template>

<script>
import VOwlCarousel from 'v-owl-carousel'

export default {
  components: { VOwlCarousel },
  data() {
    return {
      dataContent: [
        {
          id: 0,
          image: 'I',
          title: 'iwanconatejosstraxx',
          desc: 'Belum di coba, mudah2 pas sama bure up nya',
        },
        {
          id: 1,
          image: 'AB',
          title: 'ayyubeebumble',
          desc: 'Ok mantap',
        },
        {
          id: 2,
          image: 'JN',
          title: 'imamyujin',
          desc: 'Jangan ragu beli disini',
        },
        {
          id: 3,
          image: 'YG',
          title: 'yguw512z1_',
          desc: 'Mantap bang',
        },
      ],
      stars: 5,
      responsiveOptions: {
        0: {
          items: 1,
        },
        600: {
          items: 2,
        },
        1000: {
          items: 3,
        },
      },
    }
  },
}
</script>

<style scoped>
.section_5 {
  font-family: 'Poppins';
  min-height: 500px;
  margin: 50px 0;
  display: flex;
  align-items: center;
}
.card {
  min-height: 250px;
  margin: 10px;
  box-shadow: 0 1px 2px -2px rgba(0, 0, 0, 0.16),
    0 3px 6px 0 rgba(0, 0, 0, 0.12), 0 5px 12px 4px rgba(0, 0, 0, 0.09);
}
.card-body {
  padding: 0px;
}
.stars {
  color: gold;
}
.b-avatar {
  background: #0056b3;
  color: #fff;
}
.item_list_head {
  border: none;
}
.new_product {
  font-size: 40px;
  font-weight: 700;
  text-align: center;
}
.card {
  background: transparent;
  border: none;
}
.number_title {
  font-size: 120px;
  font-weight: 700;
  opacity: 0.2;
  z-index: -1;
  position: absolute;
  top: 0;
  left: 0;
}
.card-title .title {
  font-size: 1.5rem;
  font-weight: 700;
  color: #000;
  z-index: 1;
}
.card-title {
  margin-bottom: 1.5rem;
  min-height: 100px;
  display: flex;
  align-items: center;
  justify-content: end;
}
</style>
