<template>
  <section class="pro-view">
    <div class="pro-top-banner">
      <div class="pro-top-text-zone">
        <p class="sub">PROCESS</p>
        <h1 class="title">아이디어를 현실로,<br />정확한 제작 프로세스</h1>
        <p class="desc">
          체계적인 5단계 프로세스를 통해.<br />
          최상의 결과물을 제공 합니다.
        </p>
      </div>
      <div class="pro-top-banner-zone"></div>
    </div>
  </section>

  <section>
    <div class="process-container">
      <!-- 1. 메인 설명 카드 (첫 번째) -->
      <div class="card intro-card">
        <h3>PROCESS</h3>
        <h2>제작 과정</h2>
        <p>전문적인 프로세스로<br />아이디어를 완성도 높은<br />결과물로 구현합니다.</p>
      </div>

      <!-- 2. 상담 및 기획 -->
      <div class="card process-card">
        <div class="card-image bg-consulting"></div>
        <div class="card-content">
          <span class="step-num">01</span>
          <h3>상담 및 기획</h3>
          <p>
            고객의 요구사항을 분석하고 용도, 소재, 제작 수량을 고려하여 최적의 제작 방향을
            제안합니다.
          </p>
        </div>
      </div>

      <!-- 3. 설계 및 모델링 -->
      <div class="card process-card">
        <div class="card-image bg-modeling"></div>
        <div class="card-content">
          <span class="step-num">02</span>
          <h3>설계 및 모델링</h3>
          <p>
            아이디어를 바탕으로 3D CAD 프로그램을 활용하여 정밀한 3D 데이터 모델링을 수행합니다.
          </p>
        </div>
      </div>

      <!-- 4. 3D 프린터 출력 -->
      <div class="card process-card">
        <div class="card-image bg-printing"></div>
        <div class="card-content">
          <span class="step-num">03</span>
          <h3>3D 프린터 출력</h3>
          <p>
            제품 특성에 맞는 최적의 3D 프린터(FDM, SLA 등)와 소재를 선택하여 시제품을 출력합니다.
          </p>
        </div>
      </div>

      <!-- 5. 후처리 및 검사 -->
      <div class="card process-card">
        <div class="card-image bg-postprocessing"></div>
        <div class="card-content">
          <span class="step-num">04</span>
          <h3>후처리 및 검사</h3>
          <p>
            서포터 제거, 표면 샌딩, 도색 등 후처리를 진행하고 도면과의 오차 및 퀄리티를 정밀
            검사합니다.
          </p>
        </div>
      </div>

      <!-- 6. 납품 -->
      <div class="card process-card">
        <div class="card-image bg-delivery"></div>
        <div class="card-content">
          <span class="step-num">05</span>
          <h3>납품</h3>
          <p>완성된 제품을 안전하게 포장하여 고객이 원하는 일정과 장소에 최종 납품합니다.</p>
        </div>
      </div>
    </div>
  </section>

  <section>
    <div class="strength-container">
      <!-- 섹션 타이틀 영역 -->
      <div class="strength-header">
        <h2>OUR STRENGTH</h2>
        <p>차별화된 기술력과 서비스로 최고의 결과물을 보장합니다.</p>
      </div>

      <!-- 강점 카드 리스트 (4열 배분) -->
      <div class="strength-grid">
        <!-- 1. 정밀한 기술력 -->
        <div class="strength-card">
          <div class="icon-box">
            <!-- 과녁/정밀 아이콘 -->
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <circle cx="12" cy="12" r="10"></circle>
              <circle cx="12" cy="12" r="6"></circle>
              <circle cx="12" cy="12" r="2"></circle>
            </svg>
          </div>
          <h3>정밀한 기술력</h3>
          <p>오차 없는 완벽한 디테일과 고해상도 출력을 지원합니다.</p>
        </div>

        <!-- 2. 다양한 소재 지원 -->
        <div class="strength-card">
          <div class="icon-box">
            <!-- 레이어/소재 아이콘 -->
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <polygon points="12 2 2 7 12 12 22 7 12 2"></polygon>
              <polyline points="2 17 12 22 22 17"></polyline>
              <polyline points="2 12 12 17 22 12"></polyline>
            </svg>
          </div>
          <h3>다양한 소재 지원</h3>
          <p>플라스틱부터 특수 수지까지 용도에 맞는 최적의 소재를 제공합니다.</p>
        </div>

        <!-- 3. 신속한 대응 -->
        <div class="strength-card">
          <div class="icon-box">
            <!-- 번개/속도 아이콘 -->
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"></polygon>
            </svg>
          </div>
          <h3>신속한 대응</h3>
          <p>실시간 상담과 빠른 공정으로 납기일을 정확하게 준수합니다.</p>
        </div>

        <!-- 4. 고객 중심 서비스 -->
        <div class="strength-card">
          <div class="icon-box">
            <!-- 하트/고객 중심 아이콘 -->
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path
                d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"
              ></path>
            </svg>
          </div>
          <h3>고객 중심 서비스</h3>
          <p>기획부터 최종 납품까지 1:1 맞춤형 컨설팅을 제공합니다.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* [공통 및 레이아웃] */
.pro-view {
  width: 100%;
  box-sizing: border-box;
}

.pro-top-banner {
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
.pro-top-text-zone {
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
.pro-top-banner-zone {
  width: 60%;
  height: 100%;
  background: url('@/assets/images/process_topmain.png') no-repeat center right / contain;
}

.process-container {
  display: flex;
  gap: 16px;
  width: 1280px;
  height: 500px;
  margin: 0 auto;
  padding: 20px;
  box-sizing: border-box;
  background-color: #f8f9fa;
  font-family: 'Noto Sans KR', sans-serif;

  /* 공통 카드 스타일 (6개 카드 동일 너비 배분) */
  .card {
    flex: 1;
    display: flex;
    flex-direction: column;
    background: #ffffff;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
    transition:
      transform 0.3s ease,
      box-shadow 0.3s ease;
  }

  .card:hover {
    transform: translateY(-8px);
    box-shadow: 0 12px 24px rgba(0, 0, 0, 0.1);
  }

  /* 첫 번째 소개 카드 스타일 */
  .intro-card {
    background: linear-gradient(135deg, #1e3a8a, #3b82f6);
    color: #ffffff;
    padding: 40px 24px;
    justify-content: center;
  }

  .intro-card h2 {
    font-size: 28px;
    font-weight: 700;
    line-height: 1.4;
    margin: 0 0 20px 0;
  }

  .intro-card p {
    font-size: 15px;
    line-height: 1.6;
    opacity: 0.9;
    margin: 0;
  }

  /* 과정 카드 스타일 (이미지 + 텍스트) */
  .process-card .card-image {
    height: 45%;
    background-size: cover;
    background-position: center;
    background-color: #e5e7eb; /* 이미지 로딩 전 기본 배경색 */
  }

  /* 각 카드별 임시 이미지 경로 설정 (실제 이미지 경로로 변경 필요) */
  .bg-consulting {
    background-image: url('@/assets/images/no_image.png');
  }
  .bg-modeling {
    background-image: url('@/assets/images/no_image.png');
  }
  .bg-printing {
    background-image: url('@/assets/images/no_image.png');
  }
  .bg-postprocessing {
    background-image: url('@/assets/images/no_image.png');
  }
  .bg-delivery {
    background-image: url('@/assets/images/no_image.png');
  }

  .process-card .card-content {
    height: 55%;
    padding: 24px 20px;
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
  }

  .step-num {
    font-size: 14px;
    font-weight: 700;
    color: #3b82f6;
    margin-bottom: 8px;
  }

  .process-card h3 {
    font-size: 18px;
    font-weight: 700;
    color: #1f2937;
    margin: 0 0 12px 0;
  }

  .process-card p {
    font-size: 14px;
    color: #4b5563;
    line-height: 1.5;
    margin: 0;
    /* 텍스트가 넘칠 경우를 대비한 말줄임 처리 */
    display: -webkit-box;
    -webkit-line-clamp: 5;
    -webkit-box-orient: vertical;
    overflow: hidden;
  }
}

/* 3번째 안내 start */
/* 강점 섹션 전체 컨테이너 (기존 가로폭 1280px 유지) */
.strength-container {
  width: 1280px;
  margin: 0 auto;
  padding: 60px 20px;
  box-sizing: border-box;
  background-color: #ffffff;
  font-family: 'Noto Sans KR', sans-serif;
}

/* 섹션 타이틀 및 부제목 */
.strength-header {
  text-align: center;
  margin-bottom: 40px;
}

.strength-header h2 {
  font-size: 28px;
  font-weight: 700;
  color: #1e3a8a; /* 기존 intro-card 메인 색상 계열 */
  letter-spacing: -0.5px;
  margin: 0 0 10px 0;
}

.strength-header p {
  font-size: 16px;
  color: #6b7280;
  margin: 0;
}

/* 4열 배열을 위한 그리드 레이아웃 */
.strength-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
}

/* 강점 개별 카드 스타일 (기존 카드 스타일과 통일) */
.strength-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  padding: 35px 24px;
  background: #f8f9fa; /* 기존 배경색과 대비되도록 반전 */
  border-radius: 12px;
  box-sizing: border-box;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
}

/* 기존 카드와 동일한 호버 효과 */
.strength-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.08);
  background: #ffffff; /* 호버 시 화이트로 배경 전환 */
  border: 1px solid #e5e7eb;
}

/* 아이콘 박스 설정 (파란색 원형 원동력 강조) */
.strength-card .icon-box {
  width: 64px;
  height: 64px;
  background-color: #eff6ff;
  color: #3b82f6; /* 기존 step-num 색상 계열 */
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 20px;
  transition:
    background-color 0.3s ease,
    color 0.3s ease;
}

/* 호버 시 아이콘 색상 반전 효과 */
.strength-card:hover .icon-box {
  background-color: #3b82f6;
  color: #ffffff;
}

.strength-card .icon-box svg {
  width: 28px;
  height: 28px;
}

/* 카드 내 제목 (기존 process-card h3 스타일 적용) */
.strength-card h3 {
  font-size: 18px;
  font-weight: 700;
  color: #1f2937;
  margin: 0 0 12px 0;
}

/* 카드 내 본문 설명 (기존 process-card p 스타일 적용) */
.strength-card p {
  font-size: 14px;
  color: #4b5563;
  line-height: 1.6;
  margin: 0;
}

/* [반응형 레이아웃] */
@media (max-width: 760px) {
  .pro-top-banner {
    flex-direction: column-reverse;
    height: auto;
    padding: 40px 20px;
  }

  .pro-top-text-zone {
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

  .pro-top-banner-zone {
    width: 100%;
    height: 250px;
    background-position: center;
  }

  /* 1. 기존 프로세스 영역 반응형 수정 */
  .process-container {
    width: 100%;
    height: auto;
    flex-direction: column;
    gap: 20px;
    padding: 16px;

    .card {
      width: 100%;
      height: auto;
    }

    /* --- intro-card 자연스러운 줄바꿈 및 넘침 방지 추가 --- */
    .intro-card {
      padding: 32px 20px; /* 모바일 화면에 맞춰 내부 여백 살짝 축소 */
      box-sizing: border-box;
      /* 긴 영문이나 숫자가 와도 강제로 깨뜨려 영역을 넘지 않게 방지 */
      word-break: keep-all;
      overflow-wrap: break-word;
    }

    .intro-card h2 {
      font-size: 22px; /* 모바일 가독성을 위해 타이틀 크기 축소 */
      line-height: 1.3;
      margin-bottom: 12px;
    }

    .intro-card p {
      font-size: 14px; /* 본문 폰트 크기 미세 조정 */
      line-height: 1.5;
    }
  }

  /* 2. 추가된 OUR STRENGTH 영역 반응형 수정 */
  .strength-container {
    width: 100%;
    padding: 60px 16px;
  }

  .strength-header h2 {
    font-size: 24px;
  }

  .strength-header p {
    font-size: 14px;
  }

  .strength-grid {
    grid-template-columns: repeat(1, 1fr);
    gap: 16px;
  }

  /* 정렬 방식을 block으로 변경하여 내부 요소들이 자연스럽게 한 줄씩 차지하도록 수정 */
  .strength-card {
    display: block;
    text-align: center; /* 모바일 환경에서 정중앙 정렬로 가독성 확보 */
    padding: 30px 20px;
  }

  /* 아이콘 박스를 중앙 정렬하고 아래 여백 부여 */
  .strength-card .icon-box {
    width: 56px;
    height: 56px;
    margin: 0 auto 16px auto; /* 가로 중앙 정렬 및 h3와의 간격 */
  }

  .strength-card .icon-box svg {
    width: 24px;
    height: 24px;
  }

  /* h3는 원래 블록 요소이므로 p 태그를 자동으로 다음 줄로 밀어냅니다 */
  .strength-card h3 {
    font-size: 17px;
    margin: 0 0 8px 0; /* 제목과 설명(p) 사이의 확실한 줄내림 간격 */
  }

  .strength-card p {
    font-size: 14px;
    line-height: 1.5;
  }
}
</style>
