<template>
  <section id="cardType" class="card__wrap" :class="attr">
    <h2>{{ card[0].main }}</h2>
    <p>{{ card[1].comm }}</p>
    <div class="card_inner" :class="layout">
      <article class="card">
        <figure class="card__header">
          <img src="../../assets/img/card_bg01_01.jpg" alt="축구 기초 강의" />
        </figure>
        <div class="card__body">
          <h3 class="tit">{{ card[2].title1 }}</h3>
          <p class="desc">
            {{ card[5].desc1 }}
          </p>
          <a class="btn" href="/">
            {{ card[8].add }}
            <span aria-hidden="true">
              <svg
                width="66"
                height="8"
                viewBox="0 0 66 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M65.3535 4.34956C65.5465 4.15211 65.543 3.83555 65.3455 3.6425L62.128 0.496467C61.9305 0.303411 61.614 0.306968 61.4209 0.504411C61.2279 0.701855 61.2314 1.01842 61.4289 1.21147L64.2889 4.00794L61.4924 6.86797C61.2994 7.06541 61.3029 7.38198 61.5004 7.57503C61.6978 7.76809 62.0144 7.76453 62.2074 7.56709L65.3535 4.34956ZM1.00562 5.21902L65.0016 4.49997L64.9903 3.50003L0.994382 4.21909L1.00562 5.21902Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img src="../../assets/img/card_bg01_02.jpg" alt="드리블 기초 강의" />
        </figure>
        <div class="card__body">
          <h3 class="tit">{{ card[3].title2 }}</h3>
          <p class="desc">
            {{ card[6].desc2 }}
          </p>
          <a class="btn" href="/">
            {{ card[8].add }}
            <span aria-hidden="true">
              <svg
                width="66"
                height="8"
                viewBox="0 0 66 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M65.3535 4.34956C65.5465 4.15211 65.543 3.83555 65.3455 3.6425L62.128 0.496467C61.9305 0.303411 61.614 0.306968 61.4209 0.504411C61.2279 0.701855 61.2314 1.01842 61.4289 1.21147L64.2889 4.00794L61.4924 6.86797C61.2994 7.06541 61.3029 7.38198 61.5004 7.57503C61.6978 7.76809 62.0144 7.76453 62.2074 7.56709L65.3535 4.34956ZM1.00562 5.21902L65.0016 4.49997L64.9903 3.50003L0.994382 4.21909L1.00562 5.21902Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img src="../../assets/img/card_bg01_03.jpg" alt="슈팅 기초 강의" />
        </figure>
        <div class="card__body">
          <h3 class="tit">{{ card[4].title3 }}</h3>
          <p class="desc">
            {{ card[7].desc3 }}
          </p>
          <a class="btn" href="/">
            {{ card[8].add }}
            <span aria-hidden="true">
              <svg
                width="66"
                height="8"
                viewBox="0 0 66 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M65.3535 4.34956C65.5465 4.15211 65.543 3.83555 65.3455 3.6425L62.128 0.496467C61.9305 0.303411 61.614 0.306968 61.4209 0.504411C61.2279 0.701855 61.2314 1.01842 61.4289 1.21147L64.2889 4.00794L61.4924 6.86797C61.2994 7.06541 61.3029 7.38198 61.5004 7.57503C61.6978 7.76809 62.0144 7.76453 62.2074 7.56709L65.3535 4.34956ZM1.00562 5.21902L65.0016 4.49997L64.9903 3.50003L0.994382 4.21909L1.00562 5.21902Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
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
      card: [
        { main: "세계맥주 추천" },
        { comm: "편의점에서 보는 세계맥주 어떤걸 사야할지 모르시겠다구요?" },
        { title1: "홉하우스13" },
        { title2: "기네스" },
        { title3: "하이네켄" },
        {
          desc1:
            "맥주를 별로 선호하지 않는 제가 좋아하는 몇 안 되는 맥주입니다. 쌉쌀하고 강한 향이 따라오는 진한 라거로써 안주가 필요 없이 술 자체로 즐길수 있는 매력을 가지고있습니다.",
        },
        {
          desc2:
            "호불호가 갈리는 기네스 흑맥주입니다. 탄산이 거의 없으며 쌉싸름 하고 진한 흑맥주의 맛을 잘 느낄수 있는 매력을 가지고 있습니다. 크리미한 거품을 빠트릴 순 없겠죠?",
        },
        {
          desc3:
            "네덜란드의 맥주 브랜드. 유럽뿐만 아니라 세계적으로 인지도와 판매량에서 최상위 브랜드입니다. 소맥맛과 비슷하며 소맥을 좋아하는 사람에게 추천합니다. 벌꿀향이 나는 것은 포인트!",
        },
        { add: "더 자세히 보기" },
      ],
    };
  },
};
</script>
<style>
/* cardType */
.card_inner {
  display: flex;
  justify-content: space-between; /*양쪽 정렬*/
}
.card {
  width: 32%;
  background: #f5f5f5;
}
.card__body {
  padding: 24px;
}
.card__body .tit {
  font-size: 24px;
  margin-bottom: 10px;
  /* 한줄효과 */
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  padding-right: 20px;
}
.card__body .desc {
  font-size: 18px;
  line-height: 1.4;
  color: #666;
  margin-bottom: 20px;
  font-weight: 300;
  /* 4줄이상이면 ...으로 표시 */
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
}
@media (max-width: 960px) {
  .card_inner {
    flex-wrap: wrap;
  }
  .card {
    width: 49%;
  }
  .card:last-child {
    display: none;
  }
}
@media (max-width: 600px) {
  .card {
    width: 100%;
  }
  .card:first-child {
    margin-bottom: 20px;
  }
  .card__body {
    padding: 20px;
  }
  .card__body .desc {
    font-size: 16px;
  }
}
</style>
