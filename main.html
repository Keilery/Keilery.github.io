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
        
        .content {
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
                inset 0 1px 0 rgba(255, 255, 255, 0.05),0 20px 40px rgba(0, 0, 0, 0.3);
        }
        
        .suggestion-title {
            color: rgba(255, 255, 255, 0.9);
            font-family: 'Orbitron', sans-serif;
            font-size: 1.1rem;
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }
        
        .hash-tag {
            display: inline-block;
            background: rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.25);
            color: #ffffff;
            padding: 10px 25px;
            border-radius: 50px;
            font-weight: 700;
            font-family: 'Courier New', monospace;
            font-size: 1rem;
            animation: glow 3s ease-in-out infinite alternate;
            box-shadow: 
                0 0 20px rgba(255, 255, 255, 0.1),
                inset 0 1px 0 rgba(255, 255, 255, 0.1);
        }
        
        @keyframes glow {
            from { box-shadow: 0 0 10px rgba(255, 255, 255, 0.1), inset 0 1px 0 rgba(255, 255, 255, 0.1); }
            to { box-shadow: 0 0 30px rgba(255, 255, 255, 0.2), 0 0 50px rgba(255, 255, 255, 0.1), inset 0 1px 0 rgba(255, 255, 255, 0.15); }
        }
        
        .process-flow {
            display: flex;
            align-items: center;
            justify-content: center;
            flex-wrap: wrap;
            gap: 12px;
            margin: 15px 0;
            padding: 15px;
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.08);
        }
        
        .flow-item {
            color: rgba(255, 255, 255, 0.9);
            font-weight: 700;
            background: rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(5px);
            padding: 6px 14px;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }
        
        .flow-arrow {
            color: rgba(255, 255, 255, 0.4);
            font-size: 1.1rem;
        }
        
        .vote-info {
            background: rgba(255, 215, 0, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 215, 0, 0.2);
            padding: 12px 20px;
            margin: 15px 0;
            border-radius: 20px;
            color: rgba(255, 255, 255, 0.85);
            box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.05);
        }
        
        .check-icon {
            color: #64ff96;
            font-weight: bold;
            font-size: 1.1rem;
            text-shadow: 0 0 10px rgba(100, 255, 150, 0.5);
        }
        
        strong {
            color: rgba(255, 255, 255, 0.95);
            font-weight: 700;
        }
        
        em {
            color: rgba(255, 255, 255, 0.7);
            font-style: normal;
            font-weight: 600;
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        /* Стили для скроллбара */
        ::-webkit-scrollbar {
            width: 12px;
        }
        
        ::-webkit-scrollbar-track {
            background: rgba(0, 0, 0, 0.3);
            border-radius: 10px;
        }
        
        ::-webkit-scrollbar-thumb {
            background: rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            border: 3px solid transparent;
            background-clip: content-box;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: rgba(255, 255, 255, 0.3);
        }
        
        /* Дополнительный контент для демонстрации прокрутки */
        .extra-content {
            margin-top: 15px;
            padding: 15px;
            background: rgba(255, 255, 255, 0.02);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }
        
        .extra-content h3 {
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 8px;font-family: 'Orbitron', sans-serif;
            font-size: 1rem;
        }
        
        .extra-content p {
            color: rgba(255, 255, 255, 0.6);
            line-height: 1.4;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="main-card">
            <div class="header">
                <h1 class="title">◆ Система Голосов ◆</h1>
                <p class="subtitle">Опросы по целям сообщества</p>
            </div>
            
            <div class="icon-row">
                <span class="floating">◈</span>
                <span class="floating">◉</span>
                <span class="floating">◈</span>
            </div>
            
            <div class="content">
                <div class="highlight-box">
                    <strong>Как это работает:</strong> Здесь проводятся опросы по целям — например, <em>найти Барбоса</em>. 
                    Вы сможете выбрать <span class="tag">"Да"</span> или <span class="tag">"Нет"</span>.
                </div>
                
                <p>
                    Если выбрано <strong>"Да"</strong>, цель получит отметку <span class="tag">#цель</span> 
                    с порядковым номером, например <span class="tag">#цель7</span>.
                </p>
                
                <div class="example-box">
                    Пример: Найти Барбоса → Голосование "Да" → #цель7
                </div>
                
                <p>Обычно цели выполняются по порядку:</p>
                
                <div class="process-flow">
                    <span class="flow-item">#цель1</span>
                    <span class="flow-arrow">→</span>
                    <span class="flow-item">#цель2</span>
                    <span class="flow-arrow">→</span>
                    <span class="flow-item">#цель3</span>
                    <span class="flow-arrow">→</span>
                    <span style="color: rgba(255,255,255,0.3);">...</span>
                </div>
                
                <div class="vote-info">
                    <strong>⚡ Голосование приоритетов:</strong> Каждую неделю проходит голосование, 
                    какую цель выполнить в первую очередь.
                </div>
                
                <p>
                    <span class="check-icon">✓</span> Когда цель выполнена, она получает отметку 
                    <span class="tag-ready">#готова</span> и добавляется <strong>ссылка на достигнутую вещь</strong>.
                </p>
                
                <div class="divider"></div>
                
                <div class="suggestion-box">
                    <div class="suggestion-title">Предложить свою цель</div>
                    <p>Напишите цель в разделе <strong>"Предложения"</strong> и обязательно добавьте в конце:</p>
                    <div style="margin-top: 12px;">
                        <span class="hash-tag">#цели</span>
                    </div>
                    <p style="margin-top: 12px; font-size: 0.8rem; color: rgba(255,255,255,0.4);">
                        (только так, без изменений)
                    </p>
                </div>
                
                <!-- Дополнительный контент для демонстрации прокрутки -->
                <div class="extra-content">
                    <h3>📋 История целей</h3>
                    <p>Здесь будет отображаться история выполненных целей с отметками #готова и ссылками на результаты...</p>
                </div>
                
                <div class="extra-content">
                    <h3>📊 Статистика голосований</h3>
                    <p>Статистика по предыдущим голосованиям и активности сообщества...</p>
                </div>
                
                <div class="extra-content">
                    <h3>💡 Частые вопросы</h3>
                    <p>Ответы на часто задаваемые вопросы о системе голосования...</p>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
