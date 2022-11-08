<template>
  <section id="bannerType" class="banner__wrap" :class="fonts">
    <h2 class="blind">배너 영역</h2>
    <div class="banner__inner">
      <h3 class="title">{{ banners[0].title }}</h3>
      <p class="desc">
        {{ banners[0].desc }}
        <a :href="banners[0].link" title="블로그로 이동">
          {{ banners[0].link }}
        </a>
      </p>
      <span class="small">{{ banners[0].cate }}</span>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    fonts: String,
  },
  data: function () {
    return {
      banners: [
        { title: "술믈리에 이XX", 
        desc: "더 다양한 정보는 구글링 해보시길 바랍니다.",
        link: "https://younghwan112.tistory.com/",
        cate: "배너 유형01" },
      ],
    };
  },
};
</script>
<style>
.banner__inner {
  background-image: url(../../assets/img/banner_bg01.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  text-align: center;
  padding: 120px 0;
  color: #fff;
}
.banner__inner .title {
  font-size: 50px;
  line-height: 1;
  font-weight: 300;
  margin-bottom: 40px;
}
.banner__inner .desc {
  font-size: 24px;
  line-height: 1.5;
  font-weight: 300;
  margin-bottom: 70px;
}
.banner__inner .desc a {
  color: #fff;
  display: block;
}
.banner__inner .desc a:hover {
  text-decoration: underline;
}
.banner__inner .small {
  font-size: 16px;
  text-decoration: underline;
}
@media (max-width: 960px) {
  .banner__inner {
    padding: 100px 0;
  }
}
@media (max-width: 600px) {
  .banner__inner {
    padding: 80px 0;
  }
  .banner__inner .title {
    font-size: 30px;
    margin-bottom: 20px;
  }
  .banner__inner .desc {
    font-size: 16px;
    margin-bottom: 40px;
  }
}
</style>
