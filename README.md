# Game<!DOCTYPE html>
<html>
<head>
    <title>Stone Paper Scissors</title>
    <style>
        body { text-align: center; font-family: Arial; background: #222; color: white; padding-top: 50px; }
        button { padding: 15px 30px; font-size: 18px; cursor: pointer; margin: 10px; border-radius: 8px; border: none; background: #ff4757; color: white; }
        button:hover { background: #ff6b81; }
        #result { font-size: 24px; margin-top: 30px; color: #eccc68; }
    </style>
</head>
<body>
    <h1>Stone Paper Scissors</h1>
    <button onclick="play('stone')">🪨 Stone</button>
    <button onclick="play('paper')">📄 Paper</button>
    <button onclick="play('scissors')">✂️ Scissors</button>
    <div id="result">Khel shuru karein!</div>

    <script>
        function play(user) {
            const choices = ['stone', 'paper', 'scissors'];
            const bot = choices[Math.floor(Math.random() * 3)];
            let res = "";
            if (user === bot) res = "Match Draw! 🤝";
            else if ((user==='stone' && bot==='scissors') || (user==='paper' && bot==='stone') || (user==='scissors' && bot==='paper')) 
                res = "Aap Jeet Gaye! 🎉 (Bot: " + bot + ")";
            else res = "Aap Haar Gaye! 💀 (Bot: " + bot + ")";
            document.getElementById("result").innerText = res;
        }
    </script>
</body>
</html>
