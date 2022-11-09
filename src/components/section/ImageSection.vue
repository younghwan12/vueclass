<template>
  <section id="imageType" class="image__wrap" :class="attr">
    <h2>{{ title[0].title }}</h2>
    <p>{{ title[0].desc }}</p>
    <div class="image__inner" :class="layout">
      <article
        class="image"
        :class="image.img"
        v-for="image in images"
        v-bind:key="image.text"
      >
        <h3 class="image__title">{{ image.title }}</h3>
        <p class="image__desc">
          {{ image.desc }}
        </p>
        <a class="image__btn" href="/" title="자세히 보기">
          {{ image.add }}
        </a>
      </article>
      <!-- <article class="image img2">
        <h3 class="image__title">{{ image[1].title2 }}</h3>
        <p class="image__desc">
          {{ image[3].desc2 }}
        </p>
        <a class="image__btn yellow" href="/" title="자세히 보기">
          {{ image[4].add }}
        </a>
      </article> -->
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
        { title: "WHISKEY", desc: "평소에 흔히 볼수있는 위스키 리스트입니다." },
      ],
      images: [
        {
          img: "img1",
          title: "JACKDANIELS",
          desc: "잭다니엘 블랙라벨입니다. 도수는 40도 최소 4년 숙성한 위스키로서, 콜라를 섞어 잭콕으로 먹던가, 온더락잔에 얼음과 같이 드시면 됩니다. 사실 맛은 없다.",
          add: "자세히 보기",
        },
        {
          img: "img2",
          title: "JAMESON",
          desc: "아일랜드 위스키 재임슨입니다. 레이디가가와 리아나가 사랑한 술로 알려져 더욱 유명해졌으며, 하이볼과 샷으로 먹지만 스트레이트로 마실 때 맛있는 술입니다.",
          add: "자세히 보기",
        },
      ],
    };
  },
};
</script>
<style>
/* imageType */
.image__inner {
  display: flex;
  justify-content: space-between;
}
.image {
  width: 49%;
  height: 370px;
  color: #fff;
  padding: 200px 30px 30px 30px;
  box-sizing: border-box;
}
.image.img1 {
  background: url(../../assets/img/jpg_bg_01_01.jpg) no-repeat center;
}
.image.img2 {
  background: url(../../assets/img/jpg_bg_01_02.jpg) no-repeat center;
}
.image__title {
  font-size: 32px;
  margin-bottom: 10px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.image__desc {
  font-size: 16px;
  margin-bottom: 10px;
  line-height: 1.5;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}
.image__btn {
  font-size: 16px;
  color: #fff;
  background-color: #404e3b;
  padding: 10px 20px;
  display: inline-block;
}
.image__btn.yellow {
  background-color: #3b434e;
}

@media (max-width: 960px) {
}
@media (max-width: 600px) {
  .image__inner {
    flex-direction: column;
  }
  .image {
    width: 100%;
    padding: 200px 20px 20px 20px;
  }
  .image:first-child {
    margin-bottom: 20px;
  }
  .image__title {
    font-size: 24px;
  }
  .image__desc {
    font-size: 16px;
  }
}
</style>
