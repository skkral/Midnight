[midnight.txt](https://github.com/user-attachments/files/30878287/midnight.txt)
# Midnight<!DOCTYPE html>
<html lang="sk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Midnight</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            background-color: #050505;
            color: #d1d1d1;
            font-family: 'Courier New', Courier, monospace;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            overflow-x: hidden;
            position: relative;
        }

        /* Filmový šum (Grain efekt) cez celú stránku - dodáva to špinavý, starý vibe */
        body::after {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: url('https://images.unsplash.com/photo-1518709268805-4e9042af9f23?auto=format&fit=crop&w=200&q=10') repeat;
            opacity: 0.04;
            pointer-events: none;
            z-index: 999;
        }

        /* Atmosférické zlaté svetlo v pozadí pripomínajúce nočné reflektory z videa */
        .glow {
            position: absolute;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, rgba(255,180,50,0.15) 0%, rgba(5,5,5,0) 70%);
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 1;
            pointer-events: none;
            animation: pulseGlow 4s infinite alternate;
        }

        @keyframes pulseGlow {
            0% { transform: translate(-50%, -50%) scale(0.9); opacity: 0.4; }
            100% { transform: translate(-50%, -50%) scale(1.2); opacity: 0.8; }
        }

        .container {
            position: relative;
            z-index: 2;
            text-align: center;
            padding: 20px;
        }

        h1 {
            font-size: 4rem;
            letter-spacing: 8px;
            text-transform: uppercase;
            color: #fff;
            text-shadow: 0 0 15px rgba(255, 200, 100, 0.4);
            margin-bottom: 10px;
        }

        p {
            font-size: 1.1rem;
            letter-spacing: 3px;
            color: #777;
            text-transform: uppercase;
            margin-bottom: 40px;
        }

        .links {
            display: flex;
            flex-direction: column;
            gap: 15px;
            width: 280px;
            margin: 0 auto;
        }

        a {
            display: block;
            background: rgba(20, 20, 20, 0.8);
            border: 1px solid #333;
            color: #ccc;
            padding: 15px;
            text-decoration: none;
            letter-spacing: 2px;
            font-size: 0.9rem;
            text-transform: uppercase;
            transition: all 0.3s ease;
        }

        a:hover {
            background: #fff;
            color: #000;
            border-color: #fff;
            box-shadow: 0 0 20px rgba(255, 200, 100, 0.5);
        }

        .footer-text {
            position: absolute;
            bottom: 20px;
            font-size: 0.7rem;
            letter-spacing: 2px;
            color: #444;
            z-index: 2;
        }
    </style>
</head>
<body>

    <div class="glow"></div>

    <div class="container">
        <h1>Midnight</h1>
        <p>Nočný archív</p>
        
        <div class="links">
            <a href="#" target="_blank">Instagram</a>
            <a href="#" target="_blank">TikTok</a>
            <a href="#" target="_blank">Kontakt</a>
        </div>
    </div>

    <div class="footer-text">
        &copy; 2026 MIDNIGHT. Všetky práva vyhradené.
    </div>

</body>
</html>
