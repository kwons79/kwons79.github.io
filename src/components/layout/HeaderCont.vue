<template>
  <div>
    <header class="Header">
      <div class="header-container">
        <!-- 로고 영역 -->
        <div class="logo">
          <router-link to="/">
            <img src="@/assets/images/taeyoung3d_logo.png" alt="taeyoung 3D 메인로고" />
          </router-link>
        </div>

        <!-- 메뉴 영역 -->
        <nav class="nav-menu">
          <div class="menu-item"><router-link to="/">HOME</router-link></div>
          <div class="menu-item"><router-link to="/">PORTFOLIO</router-link></div>
          <div class="menu-item"><router-link to="/">PROCESS</router-link></div>
          <div class="menu-item"><router-link to="/">견적문의</router-link></div>
        </nav>
      </div>
    </header>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Header',
}
</script>

<style scoped>
/* 기본 배치 및 정렬 */
.Header {
  width: 100%;
  box-sizing: border-box;
  background-color: #f9f9fa;
}
.header-container,
.nav-menu {
  display: flex;
}
.header-container {
  justify-content: space-between;
  align-items: center;
  max-width: 1280px;
  margin: 0 auto;
}
.nav-menu {
  gap: 30px;
  padding-right: 20px;
}
.logo img {
  padding-left: 20px;
  height: 80px;
  display: block;
}

/* 메뉴 아이템 & 텍스트 스타일 */
.menu-item {
  position: relative;
  padding: 8px 0;
  transition: transform 0.3s ease;
}
.menu-item a {
  text-decoration: none;
  color: #294460;
  font-size: 20px;
  font-weight: 500;
  transition: color 0.3s ease;
}

/* 하단 바 (링크 밑줄 애니메이션) */
.menu-item::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 2px;
  background-color: #294460;
  transform: scaleX(0);
  transform-origin: bottom right;
  transition:
    transform 0.3s ease,
    background-color 0.3s ease;
}

/* 마우스 오버 효과 통합 */
.menu-item:hover {
  transform: translateY(-4px);
}
.menu-item:hover a {
  color: #01a081;
}
.menu-item:hover::after {
  background-color: #01a081;
  transform: scaleX(1);
  transform-origin: bottom left;
}

/* 반응형 모바일 레이아웃 */
@media (max-width: 768px) {
  .header-container {
    flex-direction: column;
    gap: 15px;
    padding: 15px 0;
  }
  .logo img,
  .nav-menu {
    padding: 0;
  }
}
</style>
