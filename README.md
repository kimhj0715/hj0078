<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>메시지 애니메이션</title>
    <style>
        body {
            background-color: #87CEEB;
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: flex-end;
            height: 100vh;
            overflow: hidden;
        }
        .message {
            background-color: #FFD700;
            border-radius: 10px;
            padding: 8px 12px;
            margin: 5px;
            display: none; /* 초기에는 숨겨져 있음 */
            width: auto;
            max-width: 80%; /* 너무 길지 않게 조정 */
            word-wrap: break-word; /* 긴 텍스트 자동 줄바꿈 */
        }
        .container {
            width: 100%;
            padding: 10px;
            box-sizing: border-box; /* 패딩 포함 너비 계산 */
        }
    </style>
</head>
<body>
<div class="container">
    <div class="message" id="msg1">엄마</div>
    <div class="message" id="msg2">아빠</div>
    <div class="message" id="msg3">어머이날 기억 주세요</div>
    <div class="message" id="msg4">감사드립니다</div>
    <div class="message" id="msg5">-김현진-</div>
    <div class="message" id="msg6">빵뗴-</div>
</div>

<script>
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

    window.onload = showMessageSequentially;
</script>
</body>
</html>

    window.onload = showMessageSequentially;
</script>
</body>
</html>
