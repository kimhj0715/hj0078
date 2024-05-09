<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>터치로 메시지 표시</title>
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
            display: none;
            width: auto;
            max-width: 80%;
            word-wrap: break-word;
        }
        .container {
            width: 100%;
            padding: 10px;
            box-sizing: border-box;
        }
    </style>
</head>
<body>
<div class="container">
    <div class="message">엄마</div>
    <div class="message">아빠</div>
    <div class="message">축 어머이날</div>
    <div class="message">키워 주셔서 감사드립니다</div>
    <div class="message">-벌써 20살인 김현지-</div>
    <div class="message">-벌써 10살인 빵뗴-</div>
</div>

<script>
    const messages = document.querySelectorAll('.message');
    let currentMessage = 0;

    function showNextMessage() {
        if (currentMessage < messages.length) {
            messages[currentMessage].style.display = 'block';
            currentMessage++;
        }
    }

    document.body.addEventListener('click', showNextMessage);
</script>
</body>
</html>
