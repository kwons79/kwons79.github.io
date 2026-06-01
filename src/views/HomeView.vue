<template>
  <main class="home-view">
    <div class="home-top-banner">
      <div class="home-top-text-zone">
        <p class="sub">IDEA를 REAL로</p>
        <h1 class="title">정확한 기술로<br />완성하는 차이</h1>
        <p class="desc">
          3D 프린팅, 설계, 모형 제작까지<br />
          고객의 아이디어를 가장 현실적인 결과물로 만듭니다.
        </p>
        <router-link to="/portfolio"><span class="common-btn">포트폴리오 보기 ></span></router-link>
        <router-link to="/estimate"><span class="common-btn">견적 문의하기 ></span></router-link>
      </div>
      <div class="home-top-banner-zone"></div>
    </div>

    <!-- 주요 서비스 -->
    <section class="our-services-container">
      <header class="our-services-header">
        <p class="our-service-num">01 &gt;</p>
        <p class="our-service-subtitle">OUR SERVICES</p>
        <h2 class="our-service-title">주요 서비스</h2>
        <p class="our-service-desc">아이디어를 현실로 만드는<br />4가지 핵심 서비스</p>
      </header>

      <div class="our-services-grid">
        <!-- 01. 시제품 제작 -->
        <article class="our-service-card">
          <figure class="our-service-img-wrap">
            <img src="@/assets/images/main_goods_img01.png" alt="시제품 제작" />
          </figure>
          <div class="our-service-content">
            <h3>시제품 제작</h3>
            <p>제품 디자인 검토를 위한<br />외관 시제품을 제작합니다.</p>
          </div>
        </article>

        <article class="our-service-card">
          <figure class="our-service-img-wrap">
            <img src="@/assets/images/main_goods_img02.png" alt="건축모형 제작" />
          </figure>
          <div class="our-service-content">
            <h3>건축모형 제작</h3>
            <p>건축 설계 도면을 기반으로 제작한<br />정밀 건축 모형입니다.</p>
          </div>
        </article>

        <article class="our-service-card">
          <figure class="our-service-img-wrap">
            <img src="@/assets/images/main_goods_img03.png" alt="발명품 제작" />
          </figure>
          <div class="our-service-content">
            <h3>발명품 제작</h3>
            <p>전국 과학발명 경진대회 전문<br />발명품 전용 제작 서비스입니다.</p>
          </div>
        </article>

        <article class="our-service-card">
          <figure class="our-service-img-wrap">
            <img src="@/assets/images/main_goods_img04.png" alt="졸업작품 제작" />
          </figure>
          <div class="our-service-content">
            <h3>졸업작품 제작</h3>
            <p>졸업 작품을 위한<br />정확한 모형을 제작합니다.</p>
          </div>
        </article>
      </div>
    </section>

    <!-- 대표 작업물 -->
    <section class="our-services-container">
      <header class="our-services-header portfolio-header">
        <p class="our-service-num">02 &gt;</p>
        <p class="our-service-subtitle">PORTFOLIO</p>
        <h2 class="our-service-title">대표 작업물</h2>
        <p class="our-service-desc">다양한 프로젝트를 통해<br />검증된 결과물을 확인해보세요.</p>
        <router-link to="/portfolio">
          <span class="common-btn common-margin-top-20">포트폴리오 보기 ></span>
        </router-link>
      </header>

      <!-- 이 영역 크기 안에서만 슬라이드가 작동합니다 -->
      <div class="main-slider-container">
        <div class="main-slider-track">
          <div v-for="item in items" :key="item.id" class="main-slider-card">
            <img :src="item.imgSrc" :alt="item.title" />
            <div class="our-service-content">
              <h3>{{ item.title }}</h3>
              <p v-html="item.desc"></p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 제작 과정 -->
    <section class="pro-services-container">
      <header class="our-services-header">
        <p class="our-service-num">03 &gt;</p>
        <p class="our-service-subtitle">PROCESS</p>
        <h2 class="our-service-title">제작 과정</h2>
        <p class="our-service-desc">체계적인 프로세스로<br />최상의 결과물을 제공합니다.</p>
      </header>

      <div class="pro-services-grid">
        <article v-for="item in proList" :key="'p-' + item.id" class="our-service-card">
          <figure class="pro-service-img-wrap">
            <img :src="item.imgSrc" :alt="item.title" />
          </figure>
          <div class="our-service-content">
            <h3>{{ item.title }}</h3>
            <p v-html="item.desc"></p>
          </div>
        </article>
      </div>
    </section>
    <!-- 제작 과정 -->

    <!-- 견적 문의 -->
    <section class="home-contact-banner-zone">
      <div class="our-services-header">
        <p class="our-service-num">04 &gt;</p>
        <p class="our-service-subtitle">CONTACT</p>
        <h2 class="our-service-title">지금 아이디어를<br />현실로 만들어 보세요</h2>
        <p class="our-service-desc">체계적인 프로세스로<br />최상의 결과물을 제공합니다.</p>
        <router-link to="/estimate">
          <span class="common-btn common-margin-top-20">견적 문의하기 ></span>
        </router-link>
      </div>
    </section>
    <!-- 견적 문의 -->
  </main>
</template>

<script setup>
import { ref } from 'vue'

// 5개의 객체를 가진 데이터 배열 정의
const items = ref([
  {
    id: 1,
    title: '작품 이름 01',
    desc: '간단한 설명<br />정확한 모형을 제작합니다.',
    imgSrc: new URL('@/assets/images/main_portfolio_img01.png', import.meta.url).href,
  },
  {
    id: 2,
    title: '작품 이름 02',
    desc: '간단한 설명<br />두 번째 작품입니다.',
    imgSrc: new URL('@/assets/images/main_portfolio_img02.png', import.meta.url).href,
  },
  {
    id: 3,
    title: '작품 이름 03',
    desc: '간단한 설명<br />세 번째 작품입니다.',
    imgSrc: new URL('@/assets/images/main_portfolio_img03.png', import.meta.url).href,
  },
  {
    id: 4,
    title: '작품 이름 04',
    desc: '간단한 설명<br />네 번째 작품입니다.',
    imgSrc: new URL('@/assets/images/main_portfolio_img04.png', import.meta.url).href,
  },
  {
    id: 5,
    title: '작품 이름 05',
    desc: '간단한 설명<br />다섯 번째 작품입니다.',
    imgSrc: new URL('@/assets/images/main_portfolio_img05.png', import.meta.url).href,
  },
  {
    id: 1,
    title: '작품 이름 01',
    desc: '간단한 설명<br />정확한 모형을 제작합니다.',
    imgSrc: new URL('@/assets/images/main_portfolio_img01.png', import.meta.url).href,
  },
  {
    id: 2,
    title: '작품 이름 02',
    desc: '간단한 설명<br />두 번째 작품입니다.',
    imgSrc: new URL('@/assets/images/main_portfolio_img02.png', import.meta.url).href,
  },
  {
    id: 3,
    title: '작품 이름 03',
    desc: '간단한 설명<br />세 번째 작품입니다.',
    imgSrc: new URL('@/assets/images/main_portfolio_img03.png', import.meta.url).href,
  },
  {
    id: 4,
    title: '작품 이름 04',
    desc: '간단한 설명<br />네 번째 작품입니다.',
    imgSrc: new URL('@/assets/images/main_portfolio_img04.png', import.meta.url).href,
  },
  {
    id: 5,
    title: '작품 이름 05',
    desc: '간단한 설명<br />다섯 번째 작품입니다.',
    imgSrc: new URL('@/assets/images/main_portfolio_img05.png', import.meta.url).href,
  },
])

const proList = ref([
  {
    id: 1,
    title: '상담 및 기획',
    desc: '체계적인 프로세스로<br />정확히 파악합니다.',
    imgSrc: new URL('@/assets/images/main_process_img01.png', import.meta.url).href,
  },
  {
    id: 2,
    title: '설계 및 모델링',
    desc: '3D 모델링 및 검토를 통해<br />최적의 솔루션을 제안합니다.',
    imgSrc: new URL('@/assets/images/main_process_img02.png', import.meta.url).href,
  },
  {
    id: 3,
    title: '제작',
    desc: '다양한 방식의 3D 프린팅으로<br />정밀하게 제작합니다.',
    imgSrc: new URL('@/assets/images/main_process_img03.png', import.meta.url).href,
  },
  {
    id: 4,
    title: '후처리 및 검사',
    desc: '후처리 및 품질 검수를 통해<br />오나성도를 높입니다.',
    imgSrc: new URL('@/assets/images/main_process_img04.png', import.meta.url).href,
  },
  {
    id: 5,
    title: '배송',
    desc: '안전한 포장과 함께<br />고객님께 전달합니다.',
    imgSrc: new URL('@/assets/images/main_process_img05.png', import.meta.url).href,
  },
])
</script>

<style scoped>
/* [공통 및 레이아웃] */
.home-view {
  width: 100%;
  box-sizing: border-box;
}

.home-top-banner {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1280px;
  height: 450px;
  margin: 0 auto;
  /* padding: 0 40px; */
  background: #f9f9fa;
  box-sizing: border-box;
}

/* [텍스트 영역] */
.home-top-text-zone {
  width: 45%;
  color: #294460;
  padding: 0 40px;
  p {
    margin: 0;
    line-height: 1.6;
  }
  span {
    display: inline-block;
    margin: 20px 20px 0 0;
  }
  .sub {
    font-size: 24px;
    font-weight: 600;
    margin-bottom: 12px !important;
    color: #4a6b82;
  }
  .title {
    font-size: 52px;
    font-weight: 800;
    line-height: 1.3;
    margin: 0 0 20px;
  }
  .desc {
    font-size: 22px;
    color: #5a6e85;
  }
}

/* [이미지 영역] */
.home-top-banner-zone {
  width: 60%;
  height: 100%;
  background: url('@/assets/images/main_banner.png') no-repeat center right / contain;
}

.our-services-container {
  max-width: 1280px;
  margin: 0 auto;
  padding-top: 60px;

  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 24px;
  align-items: start;
}

.our-services-header {
  text-align: left;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding-top: 10px; /* 카드들과 시각적 높이를 맞추기 위한 여백 */

  .our-service-num {
    font-size: 14px;
    color: #888;
    margin: 0 0 2px 0;
  }
  .our-service-subtitle {
    font-size: 12px;
    font-weight: bold;
    letter-spacing: 1px;
    margin: 0 0 16px 0;
  }
  .our-service-title {
    font-size: 28px; /* 좁아진 너비에 맞춰 폰트 크기 살짝 축소 */
    font-weight: 700;
    margin: 0 0 16px 0;
    line-height: 1.3;
  }
  .our-service-desc {
    font-size: 13px;
    color: #666;
    line-height: 1.6;
    margin: 0;
  }
}

/* 2~5번째 칸을 묶어주는 grid (컨테이너의 그리드 흐름을 그대로 이어받음) */
.our-services-grid {
  display: content; /* 자식 요소들(our-service-card)이 부모 그리드(5칸)에 직접 배치되도록 설정 */
  grid-column: span 4; /* 5칸 중 나머지 4칸을 차지 */

  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
}

/* 개별 카드 스타일 (기존 유지) */
.our-service-card {
  background: #fff;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
  transition: transform 0.3s ease;
}
.our-service-card:hover {
  transform: translateY(-8px);
}
.our-service-img-wrap {
  margin: 0;
  width: 100%;
  height: 220px; /* 5칸 배치에 맞춰 높이 최적화 */
  overflow: hidden;

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}

.our-service-content {
  padding: 20px;
  text-align: center;

  h3 {
    font-size: 16px;
    margin-bottom: 10px;
    font-weight: 600;
  }
  p {
    font-size: 13px;
    color: #555;
    line-height: 1.6;
  }
}

.pro-services-container {
  max-width: 1280px;
  margin: 0 auto;
  padding-top: 60px;

  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 16px;
  align-items: start;
}
.pro-services-grid {
  display: content;
  gap: 16px;
  display: grid;
  grid-column: span 5;
  grid-template-columns: repeat(5, 1fr);
}
.pro-service-img-wrap {
  margin: 0;
  padding-top: 12px;
  width: 100%;
  height: 154px; /* 5칸 배치에 맞춰 높이 최적화 */
  overflow: hidden;
  background-color: #f9f9fa;
  text-align: center;
  justify-content: center;

  img {
    width: 140px;
    height: 140px;
    object-fit: cover;
  }
}

/* [데스크톱 기준: 4개 1세트] */
.portfolio-header {
  /*width: 40%; */
}
.main-slider-container {
  /*width: 60%; */
  overflow: hidden;
  margin: 0 auto;
}

.main-slider-track {
  display: flex;
  gap: 12px;
  width: 766px;
  animation: desktop-scroll 20s linear infinite;
}

/* ★ 추가: 마우스를 올렸을 때 애니메이션 일시 정지 */
.main-slider-track:hover {
  animation-play-state: paused;
  cursor: pointer; /* 마우스를 올렸을 때 손가락 모양으로 변경 (선택사항) */
}

.main-slider-card {
  width: 225.5px;
  flex-shrink: 0;
  box-sizing: border-box;
  border: 1px solid #ddd;
  border-radius: 8px;
  overflow: hidden;
}

.main-slider-card img {
  width: 100%;
  height: auto;
  display: block;
  padding: 2px;
}

@keyframes desktop-scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-1157.5px);
  }
}

/* [반응형 기준: max-width 760px 이하 - 2개 1세트] */
@media (max-width: 760px) {
  .main-slider-container {
    width: 100%;
  }

  .main-slider-track {
    width: max-content;
    animation: mobile-scroll 12s linear infinite;
  }

  /* 모바일/태블릿 터치 시에도 일시 정지되도록 유지 */
  .main-slider-track:hover {
    animation-play-state: paused;
  }

  .main-slider-card {
    width: calc((100vw - 6px) / 2);
  }

  @keyframes mobile-scroll {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(calc(((100vw - 6px) / 2) * -5 - 30px));
    }
  }
}

/* [이미지 영역] */
.home-contact-banner-zone {
  max-width: 1280px;
  margin: 60px auto;
  background: url('@/assets/images/main_footer_img01.png') no-repeat center right / contain;
}
.home-contact-banner-zone div {
  width: 100%;
  height: 280px;
}

/* [반응형 레이아웃] */
@media (max-width: 760px) {
  .home-top-text-zone {
    .title {
      font-size: 38px;
    }
  }

  .home-top-banner {
    flex-direction: column-reverse;
    height: auto;
    padding: 40px 20px;
  }

  .home-top-text-zone {
    width: 100%;
    text-align: center;
    margin-top: 30px;

    .title {
      font-size: 32px;
    }
    .sub {
      font-size: 16px;
    }
    .desc {
      font-size: 14px;
    }
  }

  .home-top-banner-zone {
    width: 100%;
    height: 250px;
    background-position: center;
  }

  .our-services-container {
    grid-template-columns: 1fr;
  }
  .our-services-grid {
    grid-column: span 1;
    grid-template-columns: repeat(2, 1fr);
  }

  .pro-services-container {
    grid-template-columns: 1fr;
  }
  .pro-services-grid {
    grid-column: span 1;
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>
