<template>
  <section id="textType" class="text__wrap" :class="attr">
    <span class="blind">텍스트 유형01</span>
    <h2 class="mb70">{{ text[0].main }}</h2>
    <div class="text__inner" :class="layout">
      <div class="text t1">
        <h3 class="text__title">{{ text[1].title1 }}</h3>
        <p class="text__desc">
          {{ text[7].desc1 }}
        </p>
        <a class="text_btn" href="/"> {{ text[13].add }} </a>
      </div>
      <div class="text t2">
        <h3 class="text__title">{{ text[2].title2 }}</h3>
        <p class="text__desc">
          {{ text[8].desc2 }}
        </p>
        <a class="text_btn" href="/"> {{ text[13].add }} </a>
      </div>
      <div class="text t3">
        <h3 class="text__title">{{ text[3].title3 }}</h3>
        <p class="text__desc">
          {{ text[9].desc3 }}
        </p>
        <a class="text_btn" href="/"> {{ text[13].add }} </a>
      </div>
      <div class="text t4">
        <h3 class="text__title">{{ text[4].title4 }}</h3>
        <p class="text__desc">
          {{ text[10].desc4 }}
        </p>
        <a class="text_btn" href="/"> {{ text[13].add }} </a>
      </div>
      <div class="text t5">
        <h3 class="text__title">{{ text[5].title5 }}</h3>
        <p class="text__desc">
          {{ text[11].desc5 }}
        </p>
        <a class="text_btn" href="/"> {{ text[13].add }} </a>
      </div>
      <div class="text t6">
        <h3 class="text__title">{{ text[6].title6 }}</h3>
        <p class="text__desc">
          {{ text[12].desc6 }}
        </p>
        <a class="text_btn" href="/"> {{ text[13].add }} </a>
      </div>
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
      text: [
        { main: "술과 잘맞는 음식궁합" },
        { title1: "위스키" },
        { title2: "와인" },
        { title3: "소주" },
        { title4: "맥주" },
        { title5: "막걸리" },
        { title6: "고량주" },
        {
          desc1:
            "어떤 음식과도 궁합이 맞는 위스키입니다. 온더락 잔에 다크 초콜릿과 함께해도 좋고, 과일과 함께해도 좋은 음식입니다.",
        },
        {
          desc2:
            "와인엔 치즈라는 말이 있을정도로 궁합이 잘맞지만 사실 다른음식들과도 잘 맞습니다. 레드와인은 스테이크와 함께 화이트와인은",
        },
        {
          desc3:
            "소주하면 생각나는 음식은 한국인이라면 삼겹살일겁니다. 삼쏘는 최고의 조합이며, 사실 어느 음식점을 가더라도 판매하고 있을정도로",
        },
        {
          desc4:
            "간단하게 즐길수있는 주류로, 치킨에 맥주 치맥, 간단하게 견과류, 마른안주 어떤음식과도 조합이 좋습니다.",
        },
        {
          desc5:
            "비오는날 생각나는 주류로, 막걸리는 무조건 파전류와 함께해야하 한다는 인식이 있습니다. 파전이 없는 막걸리는 상상할 수 없습니다.",
        },
        {
          desc6:
            "흔히 중식당에서 회식을 하면 볼수있는 주류로, 중국 술이기 때문에 중국음식들과 조합이 좋습니다, 유산슬, 깐풍기, 탕수육등등 생각나네요.",
        },
        {
          add: "더보기",
        },
      ],
    };
  },
};
</script>
<style>
.text__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.text {
  width: 32%;
  margin-bottom: 2%;
  padding: 20px;
  box-sizing: border-box;
  border-radius: 10px;
}
.text:hover {
  background: #f5f5f5;
  transition: background 0.4s;
}
.text__title {
  font-size: 24px;
  line-height: 1;
  margin-bottom: 10px;
  white-space: nowrap;
  text-overflow: ellipsis;
  position: relative;
  padding-top: 75px;
}
.text__title::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: url(../../assets/img/text_icon.svg);
}
.text.t1 .text__title::before {
  background-position: 0 0;
}
.text.t2 .text__title::before {
  background-position: -60px 0;
}
.text.t3 .text__title::before {
  background-position: -120px 0;
}
.text.t4 .text__title::before {
  background-position: -180px 0;
}
.text.t5 .text__title::before {
  background-position: -240px 0;
}
.text.t6 .text__title::before {
  background-position: -300px 0;
}
.text__desc {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.4;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  color: #666;
  margin-bottom: 20px;
}
.text_btn {
  font-size: 16px;
  line-height: 1;
  text-decoration: underline;
  text-underline-position: under;
  color: #666;
}

@media (max-width: 960px) {
  .text {
    width: 49%;
    background: #f5f5f5;
  }
}
@media (max-width: 600px) {
  .text__title {
    font-size: 20px;
  }
  .text__desc {
    font-size: 16px;
  }
}

@media (max-width: 480px) {
  .text {
    width: 100%;
  }
}
</style>
