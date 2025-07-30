<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>우리 결혼합니다</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Noto+Serif+KR:wght@300;600&display=swap');

    body {
      margin: 0;
      font-family: 'Noto Serif KR', serif;
      background: #fffaf5;
      color: #333;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      padding-bottom: 150px;
    }

    header {
      margin-top: 40px;
      animation: slideDown 1.5s ease-out;
    }

    h1 {
      font-size: 2.5rem;
      margin-bottom: 0.5rem;
    }

    h2 {
      font-weight: 300;
      font-size: 1.2rem;
      margin-bottom: 2rem;
    }

    /* 슬라이드 컨테이너 */
    .slideshow {
      position: relative;
      width: 90%;
      max-width: 600px;
      height: 400px;
      overflow: hidden;
      border-radius: 16px;
      box-shadow: 0 8px 24px rgba(0,0,0,0.1);
      margin-bottom: 2rem;
      background: #eee;
    }

    /* 슬라이드 이미지 */
    .slide {
      position: absolute;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      opacity: 0;
      transition: opacity 1s ease-in-out;
      object-fit: cover;
      object-position: center center;
      border-radius: 16px;
      user-select: none;
    }

    /* 활성 슬라이드 */
    .slide.active {
      opacity: 1;
      z-index: 1;
    }

    /* 컨트롤 버튼 */
    .controls {
      margin-top: 10px;
      display: flex;
      justify-content: center;
      gap: 1rem;
    }

    .controls button {
      padding: 0.5rem 1.5rem;
      font-size: 1rem;
      border: none;
      border-radius: 0.5rem;
      background-color: #fbb03b;
      color: white;
      cursor: pointer;
      user-select: none;
    }

    .controls button:hover {
      background-color: #e79d1a;
    }

    /* 메시지, 날짜, 정보 스타일 */
    .message {
      max-width: 700px;
      padding: 2rem;
      font-size: 1.1rem;
      line-height: 1.8;
      background: #ffffffdd;
      border-radius: 1rem;
      margin-top: 2rem;
      animation: fadeIn 2s ease-in;
    }

    .date {
      font-size: 1.5rem;
      margin-top: 2rem;
      font-weight: 600;
      animation: pulse 2s infinite ease-in-out;
    }

    .info {
      margin-top: 1.5rem;
      font-size: 1rem;
      line-height: 1.6;
      color: #555;
      animation: fadeIn 2s ease-in;
    }

    .guestbook {
      margin-top: 3rem;
      padding: 1rem;
      width: 90%;
      max-width: 600px;
      background: #fff;
      border-radius: 1rem;
      box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
      text-align: left;
    }

    .guestbook h3 {
      text-align: center;
    }

    textarea, input[type="text"] {
      width: 100%;
      padding: 0.75rem;
      font-family: inherit;
      font-size: 1rem;
      border: 1px solid #ccc;
      border-radius: 0.5rem;
      margin-bottom: 1rem;
      resize: vertical;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes slideDown {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.05); }
      100% { transform: scale(1); }
    }

    /* 반응형 */
    @media (max-width: 768px) {
      .slideshow {
        height: 300px;
      }
    }

    @media (max-width: 480px) {
      .slideshow {
        height: 220px;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>우리는 결혼합니다</h1>
    <h2>소중한 당신을 초대합니다</h2>
  </header>

  <!-- 슬라이드 영역 -->
  <div class="slideshow" aria-label="사진 슬라이드쇼">
    <img src="image1.jpg" alt="문 열고 나오는" class="slide active" />
    <img src="image2.jpg" alt="창문에 앉아서" class="slide" />
    <img src="image3.jpg" alt="스윙아웃" class="slide" />
    <img src="image4.jpg" alt="거울앞에 앉아서" class="slide" />
    <img src="image5.jpg" alt="베일 흑백" class="slide" />
    <img src="image6.jpg" alt="지이 자켓" class="slide" />
    <img src="image7.jpg" alt="지이 초점" class="slide" />
    <img src="image8.jpg" alt="정주 초점" class="slide" />
  </div>

  <div class="controls">
    <button id="prevBtn" aria-label="이전 사진 보기">← 이전</button>
    <button id="nextBtn" aria-label="다음 사진 보기">다음 →</button>
  </div>

  <div class="message">
    서로의 삶이 하나로 이어지는 뜻깊은 날,<br />
    사랑과 믿음으로 함께 걸어가기로 약속했습니다.<br /><br />
    두 사람이 만나 가족이 되는 이 기쁜 날,<br />
    따뜻한 마음으로 축복해 주시면 더없는 기쁨이겠습니다.
  </div>

  <div class="date">
    2025년 10월 26일 일요일 오후 2시 30분<br />
    충주 파라다이스 웨딩홀 드레스가든
  </div>

  <div class="info">
    신랑 계좌번호 : 신한은행 110-442-634305<br />
    신랑 전화번호 : 010-5360-1111<br /><br />
    신부 계좌번호 :<br />
    신부 전화번호 : 010-2691-0852
  </div>

  <div class="guestbook">
    <h3>방명록</h3>
    <input type="text" id="guestName" placeholder="이름을 입력해주세요" />
    <textarea id="guestMessage" placeholder="따뜻한 한마디를 남겨주세요..."></textarea>
    <button onclick="saveMessage()">남기기</button>
    <p id="saveStatus"></p>
  </div>

  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const slides = document.querySelectorAll('.slide');
      const prevBtn = document.getElementById('prevBtn');
      const nextBtn = document.getElementById('nextBtn');
      let current = 0;
      let timer;

      function showSlide(index) {
        slides.forEach((slide, i) => {
          slide.classList.toggle('active', i === index);
        });
        current = index;
      }

      function nextSlide() {
        let nextIndex = (current + 1) % slides.length;
        showSlide(nextIndex);
      }

      function prevSlide() {
        let prevIndex = (current - 1 + slides.length) % slides.length;
        showSlide(prevIndex);
      }

      prevBtn.addEventListener('click', () => {
        prevSlide();
        resetTimer();
      });

      nextBtn.addEventListener('click', () => {
        nextSlide();
        resetTimer();
      });

      function resetTimer() {
        clearInterval(timer);
        timer = setInterval(nextSlide, 5000);
      }

      // 초기 슬라이드 & 자동 재생 시작
      showSlide(current);
      timer = setInterval(nextSlide, 5000);
    });

    function saveMessage() {
      const name = document.getElementById("guestName").value.trim();
      const message = document.getElementById("guestMessage").value.trim();
      if (!name) {
        alert("이름을 입력해주세요.");
        return;
      }
      if (!message) {
        alert("메시지를 입력해주세요.");
        return;
      }
      const blob = new Blob([`이름: ${name}\n메시지: ${message}\n`], { type: 'text/plain' });
      const url = URL.createObjectURL(blob);
      const a = document.createElement("a");
      a.href = url;
      a.download = `guest_message_${Date.now()}.txt`;
      a.click();
      URL.revokeObjectURL(url);
      document.getElementById("guestMessage").value = "";
      document.getElementById("guestName").value = "";
      document.getElementById("saveStatus").innerText = "저장되었습니다. 감사합니다!";
    }
  </script>
</body>
</html>
