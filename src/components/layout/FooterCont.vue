<template>
  <footer id="Footer" class="footer">
    <section class="footer-container">
      <div class="footer-container-logo">
        <router-link to="/">
          <img src="@/assets/images/footer_logo_img.png" alt="taeyoung 3D 메인 하단 로고" />
        </router-link>
        <p>3D 프린팅, 설계, 출력 제작 전문<br />아이디어를 최고의 결과물로 보답하겠습니다.</p>
      </div>
      <div class="footer-contact-information">
        <h2>Contact Information</h2>
        <p>전화: 010-9680-2429</p>
        <p>이메일: ty190225@gmail.com</p>
        <p>상담 : 연중 무휴 [9:00 ~ 18:00]</p>
      </div>
    </section>
    <div class="footer-copyright">
      <p>Copyright © 2024 Taeyoung 3D. All rights reserved.</p>
    </div>
  </footer>
</template>

<script lang="ts">
export default {
  name: 'Footer',
}
</script>

<style lang="scss">
.footer {
  width: 100%;
  background-color: #f9f9fa; /* 배경색은 필요에 따라 변경하세요 */
  padding: 40px 0 20px 0;

  .footer-container {
    max-width: 1280px;
    margin: 0 auto; /* 중앙 정렬 */
    padding: 0 20px; /* 양옆 여백 */
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    box-sizing: border-box;

    .footer-container-logo {
      width: 50%;
      box-sizing: border-box;

      img {
        max-width: 320px; /* 로고 크기 제한 */
        height: auto;
      }
      p {
        margin-top: 15px;
        padding-left: 16px;
        line-height: 1.6;
      }
    }

    .footer-contact-information {
      text-align: right;
      width: 50%;
      box-sizing: border-box;
      padding: 0 20px 0 20px; /* 두 영역 사이의 간격 */

      h2 {
        font-size: 1.2rem;
        margin-bottom: 15px;
      }
      p {
        margin-bottom: 8px;
      }
    }
  }

  .footer-copyright {
    max-width: 1280px;
    margin: 30px auto 0 auto;
    padding: 20px 20px 0 20px;
    border-top: 1px solid #e9ecef; /* 구분선 */
    text-align: center;
  }
}

/* 📱 모바일 반응형 대응 (화면이 좁아지면 세로로 정렬) */
@media (max-width: 768px) {
  .footer {
    .footer-container {
      flex-direction: column;
      gap: 30px;

      .footer-container-logo,
      .footer-contact-information {
        width: 100%;
        text-align: center;
        margin: 0 auto;
      }
    }
  }
}
</style>
