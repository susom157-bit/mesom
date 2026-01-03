<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>play game with me?</h1>
        <div class="buttons">
            <button id="yesBtn">Yes 😍</button>
            <button id="noBtn">No 😢</button>
        </div>
        <p id="message"></p>
    </div>
    <script src="script.js"></script>
</body>
</html>

body {
    font-family: 'Arial', sans-serif;
    background: #ffe6f2;
    text-align: center;
    padding-top: 100px;
}

.container h1 {
    font-size: 2.5rem;
    color: #d6336c;
    margin-bottom: 40px;
}

button {
    font-size: 1.2rem;
    padding: 10px 30px;
    margin: 0 15px;
    border: none;
    cursor: pointer;
    border-radius: 8px;
    transition: transform .2s;
}

#yesBtn {
    background-color: #ff4d94;
    color: white;
}

#noBtn {
    background-color: #aaa;
    color: white;
}

button:hover {
    transform: scale(1.1);
}

#message {
    margin-top: 40px;
    font-size: 1.5rem;
    color: #d6336c;
}

const yesBtn = document.getElementById('yesBtn');
const noBtn = document.getElementById('noBtn');
const message = document.getElementById('message');

// ถ้ากด YES
yesBtn.addEventListener('click', () => {
    message.innerText = "Yay! I knew you'd say yes 🥰";
    yesBtn.disabled = true;
    noBtn.disabled = true;
});
/// เคลื่อนปุ่ม NO เมื่อพยายามคลิก
noBtn.addEventListener('mouseover', () => {
    const x = Math.random() * (window.innerWidth - 120);
    const y = Math.random() * (window.innerHeight - 60);
    noBtn.style.position = 'absolute';
    noBtn.style.left = x + 'px';
    noBtn.style.top = y + 'px';
});
