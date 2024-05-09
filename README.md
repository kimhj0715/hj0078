<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>메시지 애니메이션</title>
    <style>
        body {
            background-color: #87CEEB;
            font-family: Arial, sans-serif;
        }
        .message {
            background-color: #FFD700;
            border-radius: 10px;
            padding: 10px;
            margin: 10px 20px;
            display: none; /* 초기에는 숨겨져 있음 */
            width: fit-content;
            max-width: 70%;
        }
        .container {
            position: fixed;
            bottom: 10px;
            right: 10px;
        }
    </style>
</head>
<body>
<div class="container">
    <div class="message" id="msg1">엄마</div>
    <div class="message" id="msg2">아빠</div>
    <div class="message" id="msg3">축 어머이날</div>
    <div class="message" id="msg4">키워 주셔서 감사드립니다</div>
    <div class="message" id="msg5">-김현지-</div>
    <div class="message" id="msg6">빵뗴-</div>
</div>

<script>
    // 메시지들을 차례대로 나타나게 하는 함수
    function showMessageSequentially() {
        let messages = document.querySelectorAll('.message');
        let delay = 0;

        messages.forEach((message, index) => {
            setTimeout(() => {
                message.style.display = 'block';
            }, delay);
            delay += 1000; // 다음 메시지는 1초 후에 나타남
        });
    }

    // 페이지 로드 시 함수 실행
    window.onload = showMessageSequentially;
</script>
</body>
</html>
