<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Система Голосов по Целям</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@500;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            min-height: 100vh;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            font-family: 'Rajdhani', sans-serif;
            padding: 20px;
            position: relative;
            overflow-x: hidden;
            overflow-y: auto;
        }
        
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                radial-gradient(circle at 20% 50%, rgba(120, 119, 198, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(255, 119, 198, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 40% 20%, rgba(100, 200, 255, 0.1) 0%, transparent 50%);
            pointer-events: none;
            z-index: 0;
        }
        
        .container {
            max-width: 1600px;
            width: 100%;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }
        
        .main-card {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 30px;
            padding: 30px 60px;
            position: relative;
            overflow: hidden;
            box-shadow: 
                0 25px 50px rgba(0, 0, 0, 0.5),
                inset 0 1px 0 rgba(255, 255, 255, 0.1),
                0 0 0 1px rgba(255, 255, 255, 0.05);
        }
        
        .main-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, rgba(255,255,255,0.1) 0%, transparent 50%, rgba(255,255,255,0.05) 100%);
            pointer-events: none;
            border-radius: 30px;
        }
        
        .main-card::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255, 255, 255, 0.03) 0%, transparent 70%);
            animation: pulse 6s ease-in-out infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.3; }
            50% { transform: scale(1.1); opacity: 0.6; }
        }
        
        .header {
            text-align: center;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }
        
        .title {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.4rem;
            font-weight: 900;
            background: linear-gradient(90deg, #c0c0c0, #ffffff, #a0a0a0, #ffffff, #c0c0c0);
            background-size: 200% auto;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: shine 4s linear infinite;
            text-transform: uppercase;
            letter-spacing: 4px;
            margin-bottom: 8px;
            text-shadow: 0 0 30px rgba(255, 255, 255, 0.3);
        }
        
        @keyframes shine {
            to { background-position: 200% center; }
        }
        
        .subtitle {
            color: rgba(255, 255, 255, 0.5);
            font-size: 1rem;
            letter-spacing: 3px;
            text-transform: uppercase;
            font-weight: 500;
        }
        
        .
content {
            position: relative;
            z-index: 1;
            color: rgba(255, 255, 255, 0.85);
            line-height: 1.4;
            font-size: 1rem;
        }
        
        .highlight-box {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            padding: 15px 30px;
            margin: 15px 0;
            border-radius: 20px;
            position: relative;
            box-shadow: 
                inset 0 1px 0 rgba(255, 255, 255, 0.05),
                0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .highlight-box::before {
            content: '◆';
            position: absolute;
            top: -12px;
            right: 30px;
            font-size: 1.3rem;
            color: rgba(255, 255, 255, 0.6);
            text-shadow: 0 0 20px rgba(255, 255, 255, 0.5);
        }
        
        .tag {
            display: inline-block;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: #ffffff;
            padding: 6px 16px;
            border-radius: 50px;
            font-weight: 700;
            font-family: 'Orbitron', sans-serif;
            font-size: 0.85rem;
            margin: 0 3px;
            box-shadow: 
                0 4px 15px rgba(0, 0, 0, 0.2),
                inset 0 1px 0 rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }
        
        .tag:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateY(-2px);
            box-shadow: 
                0 6px 20px rgba(0, 0, 0, 0.3),
                inset 0 1px 0 rgba(255, 255, 255, 0.2);
        }
        
        .tag-ready {
            display: inline-block;
            background: rgba(100, 255, 150, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(100, 255, 150, 0.3);
            color: #64ff96;
            padding: 6px 16px;
            border-radius: 50px;
            font-weight: 700;
            font-family: 'Orbitron', sans-serif;
            font-size: 0.85rem;
            margin: 0 3px;
            box-shadow: 
                0 4px 15px rgba(0, 0, 0, 0.2),
                inset 0 1px 0 rgba(100, 255, 150, 0.1);
        }
        
        .example-box {
            background: rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 12px 20px;
            margin: 12px 0;
            font-family: 'Courier New', monospace;
            color: rgba(255, 255, 255, 0.7);
            box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.05);
        }
        
        .divider {
            height: 1px;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            margin: 20px 0;
            border-radius: 1px;
        }
        
        .icon-row {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 15px 0;
            font-size: 1.8rem;
            filter: drop-shadow(0 0 10px rgba(255, 255, 255, 0.2));
        }
        
        .floating {
            animation: float 4s ease-in-out infinite;
            opacity: 0.8;
        }
        
        .floating:nth-child(2) { animation-delay: 0.5s; }
        .floating:nth-child(3) { animation-delay: 1s; }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-8px); }
        }
        
        .suggestion-box {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(15px);
            border: 1px dashed rgba(255, 255, 255, 0.2);
            border-radius: 25px;
            padding: 25px;
            margin-top: 20px;
            text-align: center;
            box-shadow: 
                inset 0 1px 0 rgba(255, 255, 255, 0.05),
