- 👋 Hi, I’m @Omid8213
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- work2022it@gmail.com 
<!---
Omid8213/Omid8213 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
//html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web Robot</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="chat-container">
        <div id="chat-output"></div>
        <input type="text" id="user-input" placeholder="سلام!">
        <button onclick="sendMessage()">ارسال</button>
    </div>
    <script src="script.js"></script>
</body>
</html>
//css

#chat-container {
    width: 300px;
    margin: auto;
    padding: 10px;
    border: 1px solid #ccc;
}

#chat-output {
    height: 200px;
    overflow-y: scroll;
    border-bottom: 1px solid #ccc;
}

#user-input {
    width: 70%;
    padding: 5px;
}

button {
    padding: 5px;
}

//js

function sendMessage() {
    const userInput = document.getElementById("user-input").value;
    const chatOutput = document.getElementById("chat-output");

    // افزودن پیام کاربر به نمایش گردشگر
    chatOutput.innerHTML += `<p>User: ${userInput}</p>`;

    // تحلیل درخواست کاربر و ارسال پاسخ مناسب
    handleUserRequest(userInput);

    // پاکسازی محتوای ورودی کاربر
    document.getElementById("user-input").value = "";
}

function handleUserRequest(userInput) {
    const chatOutput = document.getElementById("chat-output");

    // تحلیل درخواست کاربر و ارسال پاسخ مناسب
    if (userInput.includes("آرایه")) {
        const arrayExample = ["مثال 1", "مثال 2", "مثال 3"];
        chatOutput.innerHTML += `<p>ربات: ${JSON.stringify(arrayExample)}</p>`;
    } else if (userInput.includes("آب و هوا")) {
        chatOutput.innerHTML += `<p>ربات: حالا برنامه‌نویسی برام آب و هوا تعریف کن!</p>`;
    } else if (userInput.includes("سلام") || userInput.includes("خوش")) {
        chatOutput.innerHTML += `<p>ربات: سلام! خوشحالم که اینجا هستید. چطور می‌توانم به شما کمک کنم؟</p>`;
    } else {
        chatOutput.innerHTML += `<p>ربات: متاسفانه من درخواست شما را درک نمی‌کنم.</p>`;
    }
}
