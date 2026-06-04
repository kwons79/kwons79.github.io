<template>
  <section class="por-view">
    <div class="por-top-banner">
      <div class="por-top-text-zone">
        <p class="sub">PORTFOLIO</p>
        <h1 class="title">다양한 제작 사례</h1>
        <p class="desc">
          실제 제작 작업물을 분야 별로 확인 해 보세요.<br />
          아이디어가 현실이 되는 과정을 보여드립니다.
        </p>
      </div>
      <div class="por-top-banner-zone"></div>
    </div>
  </section>

  <section>
    <div class="por-container">
      <!-- 상단 고정 네비게이션 메뉴 (왼쪽 정렬 및 라운드 버튼 스타일) -->
      <nav class="menu-bar">
        <div class="menu-wrapper">
          <button
            v-for="menu in menus"
            :key="menu.id"
            @click="scrollToSection(menu.id)"
            class="menu-btn"
          >
            {{ menu.name }}
          </button>
        </div>
      </nav>

      <!-- 메인 리스트 영역 -->
      <div class="content-area">
        <section v-for="menu in menus" :key="menu.id" :id="menu.id" class="category-section">
          <h2 class="category-title">{{ menu.name }} 영역</h2>

          <!-- 4열 10줄 격자 그리드 -->
          <div class="grid-list">
            <div v-for="n in 40" :key="n" class="card-item">
              <div class="image-box">
                <span class="placeholder-text">이미지 {{ n }}</span>
              </div>
              <div class="info-box">
                <p class="item-title">{{ menu.name }} 아이템 {{ n }}</p>
              </div>
            </div>
          </div>
        </section>
      </div>

      <!-- 우측 하단 고정 TOP 버튼 (스크롤 시 노출 및 추적) -->
      <button
        v-show="showTopBtn"
        @click="scrollToTop"
        class="scroll-top-btn"
        aria-label="맨 위로 이동"
      >
        ▲ TOP
      </button>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

// 메뉴 데이터 정의
const menus = ref([
  { id: 'prototype', name: '시제품 제작' },
  { id: 'architecture', name: '건축모형 제작' },
  { id: 'invention', name: '발명품 제작' },
  { id: 'graduation', name: '졸업작품 제작' },
  { id: 'cosmetics', name: '화장품 용기' },
  { id: 'printing', name: 'FDM/SLA 출력' },
])

// TOP 버튼 표시 여부 상태값
const showTopBtn = ref(false)

// 메뉴 클릭 시 해당 id를 가진 섹션으로 스크롤하는 함수
const scrollToSection = (id) => {
  const element = document.getElementById(id)
  if (element) {
    const offset = 80 // 상단 메뉴바 높이 고려 여백
    const bodyRect = document.body.getBoundingClientRect().top
    const elementRect = element.getBoundingClientRect().top
    const elementPosition = elementRect - bodyRect
    const offsetPosition = elementPosition - offset

    window.scrollTo({
      top: offsetPosition,
      behavior: 'smooth',
    })
  }
}

// 맨 위로 부드럽게 스크롤하는 함수
const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth',
  })
}

// 스크롤 위치 감지 함수 (100px 이상 내려오면 TOP 버튼 표시)
const handleScroll = () => {
  showTopBtn.value = window.scrollY > 100
}

// 컴포넌트 마운트 시 스크롤 이벤트 등록 및 해제
onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})
onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
/* [공통 및 레이아웃] */
.por-view {
  width: 100%;
  box-sizing: border-box;
}

.por-top-banner {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1280px;
  height: 350px;
  margin: 0 auto;
  background: #f9f9fa;
  box-sizing: border-box;
}

/* [텍스트 영역] */
.por-top-text-zone {
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
.por-top-banner-zone {
  width: 60%;
  height: 100%;
  background: url('@/assets/images/portfolio_topmain.png') no-repeat center right / contain;
}

/* 전체 레이아웃 제어 */
.por-container {
  position: relative; /* TOP 버튼의 기준점 */
  width: 100%;
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 20px;
  box-sizing: border-box;
  font-family: 'Noto Sans KR', sans-serif;

  /* 고정식 상단 네비게이션 */
  .menu-bar {
    position: sticky;
    top: 0;
    left: 0;
    width: 100%;
    height: 70px;
    background-color: #ffffff;
    border-bottom: 1px solid #e0e0e0;
    z-index: 100;
    display: flex;
    align-items: center;
  }

  /* 메뉴를 왼쪽으로 정렬하기 위한 래퍼 */
  .menu-wrapper {
    display: flex;
    gap: 12px; /* 버튼 사이 간격 */
    justify-content: flex-start;
    width: 100%;
  }

  /* 라운드 버튼 모양 스타일 및 호버 애니메이션 추가 */
  .menu-btn {
    background-color: #f1f3f5;
    border: 1px solid #e9ecef;
    border-radius: 30px; /* 둥근 라운드 처리 */
    font-size: 15px;
    font-weight: 500;
    color: #495057;
    cursor: pointer;
    padding: 10px 22px;
    transition: all 0.25s ease-in-out; /* 부드러운 애니메이션 전환 */
  }

  /* 마우스 오버 시 위로 살짝 올라가고 그림자 생기는 효과 */
  .menu-btn:hover {
    background-color: #007bff;
    color: #ffffff;
    border-color: #007bff;
    transform: translateY(-4px); /* 위로 4px 이동 */
    box-shadow: 0 4px 12px rgba(0, 123, 255, 0.2); /* 입체감 주는 그림자 */
  }

  /* 콘텐츠 섹션 스타일 */
  .content-area {
    margin-top: 20px;

    .category-section {
      padding-top: 20px;
      margin-bottom: 60px;

      .category-title {
        font-size: 24px;
        margin-bottom: 20px;
        color: #222222;
        border-left: 4px solid #007bff;
        padding-left: 10px;
      }

      /* 4열 격자 배치를 위한 CSS Grid 적용 */
      .grid-list {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 20px;
      }

      /* 개별 카드 아이템 스타일 */
      .card-item {
        background-color: #f9f9f9;
        border: 1px solid #eee;
        border-radius: 8px;
        overflow: hidden;
        display: flex;
        flex-direction: column;
      }

      .image-box {
        width: 100%;
        aspect-ratio: 4 / 3;
        background-color: #e2e8f0;
        display: flex;
        justify-content: center;
        align-items: center;
      }

      .placeholder-text {
        color: #718096;
        font-size: 14px;
      }

      .info-box {
        padding: 15px;
        text-align: center;
      }

      .item-title {
        margin: 0;
        font-size: 14px;
        color: #4a5568;
      }
    }
  }
}

/* 우측 하단 고정 플로팅 TOP 버튼 스타일 */
.scroll-top-btn {
  position: fixed;
  bottom: 40px;
  /* 1280px 콘텐트 영역 오른쪽에 붙이기 위한 계산 (오른쪽 패딩 20px 고려) */
  right: calc(50% - 640px + 30px);
  width: 60px;
  height: 60px;
  border-radius: 50%; /* 완전한 원형 버튼 */
  background-color: #333333;
  color: #ffffff;
  border: none;
  font-size: 12px;
  font-weight: bold;
  cursor: pointer;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.15);
  z-index: 999;
  transition: all 0.2s ease-in-out;
}

.scroll-top-btn:hover {
  background-color: #007bff;
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(0, 123, 255, 0.3);
}

/* 화면이 1280px보다 작아질 때 TOP 버튼 위치 조절 (반응형 안전장치) */
@media (max-width: 1280px) {
  .scroll-top-btn {
    right: 20px;
  }
}

/* [반응형 레이아웃] */
@media (max-width: 760px) {
  .por-top-banner {
    flex-direction: column-reverse;
    height: auto;
    padding: 40px 20px;
  }

  .por-top-text-zone {
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

  .por-top-banner-zone {
    width: 100%;
    height: 250px;
    background-position: center;
  }

  .por-container {
    .menu-bar {
      height: 60px;
      padding: 0 16px;
    }

    /* 세로 나열 방지, 가로 스크롤 활성화, 스크롤바 숨기기 */
    .menu-wrapper {
      gap: 8px; /* 버튼 간격 축소 */
      overflow-x: auto; /* 가로 스크롤 활성화 */
      white-space: nowrap; /* 줄바꿈 금지 */
      -webkit-overflow-scrolling: touch; /* iOS 부드러운 스크롤 */
    }

    /* 브라우저 기본 스크롤바 숨기기 (디자인 유지) */
    .menu-wrapper::-webkit-scrollbar {
      display: none;
    }

    /* 모바일 화면에 맞는 버튼 크기 및 효과 조정 */
    .menu-btn {
      padding: 8px 16px; /* 패딩 축소 */
      font-size: 14px; /* 글자 크기 축소 */
      flex-shrink: 0; /* 버튼 형태 일그러짐 방지 */
    }

    /* 터치 기기 특성을 고려하여 호버 애니메이션 제거 또는 약화 */
    .menu-btn:hover {
      transform: none; /* 위로 올라가는 효과 제거 */
      box-shadow: none; /* 그림자 효과 제거 */
      background-color: #007bff;
      color: #ffffff;
      border-color: #007bff;
    }

    .content-area {
      margin-top: 15px;

      .category-section {
        padding-top: 15px;
        margin-bottom: 40px;

        .category-title {
          font-size: 18px;
          margin-bottom: 15px;
          border-left-width: 3px;
          padding-left: 8px;
        }

        /* 4열에서 2열 격자 배치로 변경 */
        .grid-list {
          grid-template-columns: repeat(2, 1fr);
          gap: 12px;
        }

        /* 모바일 환경에 맞춘 개별 카드 조절 */
        .card-item {
          border-radius: 6px;
        }

        .placeholder-text {
          font-size: 12px;
        }

        .info-box {
          padding: 10px;
        }

        .item-title {
          font-size: 13px;
          line-height: 1.4;
        }
      }
    }
  }
}
</style>
