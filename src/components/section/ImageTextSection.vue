<template>
  <section id="imgTextType" class="imgText__wrap" :class="attr">
    <h2 class="blind">유용한 사이트 살펴보기</h2>
    <div class="imgText__inner" :class="layout">
      <div class="imgText__txt">
        <span>{{ title[0].type }}</span>
        <h3>{{ title[0].title }}</h3>
        <p>
          {{ title[0].desc }}
        </p>
        <ul>
          <li v-for="title in imgText" v-bind:key="title.text">
            <a href="/">{{ title.text }}</a>
          </li>
        </ul>
      </div>
      <div
        class="imgText__img"
        :class="text.style"
        v-for="text in imgText2"
        v-bind:key="text.text"
      >
        <a href="/">{{ text.desc }}</a>
      </div>
      <!-- <div class="imgText__img img2">
        <a href="/" class="blue"> {{ imgText[1].text }} </a>
      </div> -->
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
  data: function () {
    return {
      title: [
        {
          type: "이미지 텍스트 유형01",
          title: "다양한 술 종류 알아보기",
          desc: "다양한 술의 종류들에 대해서 알아볼 수 있으며 그에 따른 전문 사이트입니다.",
        },
      ],
      imgText: [
        { text: "위스키 사이트" },
        { text: "와인 사이트" },
        { text: "소주 사이트" },
        { text: "맥주 사이트" },
        { text: "막걸리 사이트" },
        { text: "고량주 사이트" },
      ],
      imgText2: [
        { style: "img1", desc: "위스키 사이트" },
        { style: "img2", desc: "와인 사이트" },
      ],
    };
  },
};
</script>
<style>
/* imgTextType */
.imgText__inner {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
.imgText__inner > div {
  width: 32%;
  height: 500px;
}
.imgText__txt span {
  font-size: 16px;
  color: #666;
  text-decoration: underline;
  text-underline-position: under;
  margin-bottom: 20px;
  display: block;
}
.imgText__txt h3 {
  font-size: 50px;
  font-weight: 300;
  margin-bottom: 20px;
}
.imgText__txt p {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.5;
  color: #666;
  margin-bottom: 10px;
}
.imgText__txt ul {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.6;
}
.imgText__txt ul li {
  position: relative;
  padding-left: 20px;
}
.imgText__txt ul li a {
  color: #666;
}
.imgText__txt ul li::before {
  content: "";
  width: 5px;
  height: 5px;
  border-radius: 50%;
  position: absolute;
  left: 5px;
  top: 9px;
  background: #666;
}
.imgText__img {
  border-radius: 10px;
  position: relative;
}
.imgText__img a {
  position: absolute;
  left: 30px;
  bottom: 30px;
  background-color: rgba(66, 14, 14, 0.849);
  color: #fff;
  font-size: 18px;
  padding: 10px 30px;
  border-radius: 30px;
  display: inline-block;
}
.imgText__img a.blue {
  background-color: rgba(87, 43, 18, 0.815);
}
.imgText__img.img1 {
  background: url(../../assets/img/imgText_bg01.jpg) no-repeat center / cover;
}
.imgText__img.img2 {
  background: url(../../assets/img/imgText_bg02.jpg) no-repeat center / cover;
}

@media (max-width: 960px) {
  .imgText__inner {
    flex-wrap: wrap;
  }
  .imgText__txt h3 {
    font-size: 40px;
  }
  .imgText__txt p {
    margin-bottom: 60px;
  }
  .imgText__inner > div.imgText__txt {
    width: 100%;
    height: auto;
    text-align: center;
  }
  .imgText__inner > div.imgText__txt ul {
    display: none;
  }
  .imgText__inner > div.imgText__img {
    width: 49%;
  }
}
@media (max-width: 600px) {
  .imgText__txt span {
    font-size: 14px;
    margin-bottom: 10px;
  }
  .imgText__txt h3 {
    font-size: 30px;
  }
  .imgText__txt p {
    margin-bottom: 50px;
    font-size: 16px;
  }
  .imgText__inner > div.imgText__img {
    width: 100%;
    height: 300px;
  }
  .imgText__inner > div.imgText__img.img1 {
    margin-bottom: 20px;
  }
  .imgText__img a {
    left: 20px;
    bottom: 20px;
  }
}
</style>
