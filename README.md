# Birthday-Project
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Something Special For You</title>
    <style>
        :root {
            --pink: #ff4d6d;
            --light-pink: #ffccd5;
            --bg-gradient: linear-gradient(135deg, #fbc2eb 0%, #a6c1ee 100%);
        }
body {
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: var(--bg-gradient);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            color: #333;
        }

        /* Initial Landing Screen */
        #landing {
            text-align: center;
            z-index: 10;
        }
.btn-begin {
            background-color: white;
            color: var(--pink);
            border: none;
            padding: 15px 30px;
            font-size: 1.2rem;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .btn-begin:hover {
            transform: scale(1.1);
        }
/* Hidden Content Section */
        #content {
            display: none;
            max-width: 500px;
            background: rgba(255, 255, 255, 0.9);
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            animation: fadeIn 1s ease-in;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
/* Floating Hearts Animation */
        .heart {
            position: absolute;
            color: var(--pink);
            font-size: 20px;
            user-select: none;
            pointer-events: none;
            animation: float 4s linear forwards;
        }

        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
        }
</style>
</head>
<body>

    <div id="landing">
        <h1 style="color: white; text-shadow: 2px 2px 4px 0g Special Awaits You</h1>
        <button class="btn-begin" 
onclick=" 💝 HAPPY BIRTHDAY JAANUU 🎀()">Click to Begin</button>
    </div>

    <div id="content">
        <div style="font-size: 50px;">❤️</div>
        <h2> 💝 HAPPY BIRTHDAY JAANUU 💝</h2>
        <p id="letterText">
            "Every day with you feels like a beautiful dream. 
            You are the sunshine that brightens my darkest days. 
            I'm so lucky to have you in my life.”
</p>
        <hr style="border: 0; height: 1px; background: #eee; margin: 20px 0;">
        <p><i>- Always yours</i></p>
    </div>

    <script>
        function startSurprise() {
            // Hide landing and show content
            document.getElementById('landing').style.display = 'none';
            document.getElementById('content').style.display = 'block';

            // Start heart rain
            setInterval(createHeart, 300);
        }

        function createHeart() {
            const heart = document.createElement('div');
heart.classList.add('heart');
            heart.innerHTML = '💝 ';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = (Math.random() * 2 + 3) + 's';
            document.body.appendChild(heart);

            setTimeout(() => {
                heart.remove();
            }, 5000);
        }
    </script>
</body>
</html>
