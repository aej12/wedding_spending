<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>광고 시청 후 자료 보기</title>
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      padding-top: 80px;
    }
    .btn {
      padding: 15px 30px;
      font-size: 18px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      margin: 10px;
    }
    .ad-button {
      background-color: #007aff;
      color: white;
    }
    .go-button {
      background-color: gray;
      color: white;
    }
    .go-button.active {
      background-color: #28a745;
    }
  </style>
</head>
<body>

  <h2>📢 광고를 먼저 봐주세요!</h2>
  <p>쿠팡 광고를 클릭하면 자료 다운로드 버튼이 활성화됩니다.</p>

  <!-- 쿠팡 광고 버튼 -->
  <button class="btn ad-button" onclick="handleAdClick()">✅ 쿠팡 인기 상품 보기</button>

  <!-- 구글 스프레드시트로 이동 버튼 (처음엔 비활성화) -->
  <button id="goBtn" class="btn go-button" disabled>📄 공유자료 보기</button>

  <script>
    function handleAdClick() {
      // 쿠팡 링크 새 탭으로 열기
      window.open("https://link.coupang.com/a/cGACtg", "_blank");

      // 공유자료 버튼 활성화
      const goBtn = document.getElementById("goBtn");
      goBtn.disabled = false;
      goBtn.classList.add("active");

      // 클릭 시 구글 스프레드시트로 이동
      goBtn.onclick = function () {
        window.location.href = "https://docs.google.com/spreadsheets/d/1Iiqv3YcXnL8R7Zv4hMV8mcV6VTVq0j9xHNVAYNpCI6A/edit?gid=2099666454#gid=2099666454";
      };
    }
  </script>

</body>
</html>
