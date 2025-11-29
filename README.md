#DARI RENDY
<html lang="id">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sahabat Sejati - Aldo &amp; Masdy</title>
  <script src="/_sdk/element_sdk.js"></script>
  <style>
        body {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Georgia', serif;
            width: 100%;
            height: 100%;
            overflow-x: hidden;
        }
        
        html, body {
            height: 100%;
        }
        
        .main-wrapper {
            width: 100%;
            min-height: 100%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 60px 20px;
        }
        
        .content-container {
            max-width: 900px;
            margin: 0 auto;
        }
        
        .header-section {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .main-title {
            font-size: 56px;
            color: #ffffff;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }
        
        .friends-names {
            font-size: 36px;
            color: #ffd700;
            margin-bottom: 15px;
            font-weight: bold;
        }
        
        .heart-icon {
            font-size: 32px;
            animation: heartbeat 1.5s ease-in-out infinite;
        }
        
        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }
        
        .cards-section {
            display: grid;
            gap: 30px;
            margin-top: 40px;
        }
        
        .quote-card {
            background: #ffffff;
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .quote-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.3);
        }
        
        .quote-icon {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .quote-text {
            font-size: 24px;
            line-height: 1.6;
            color: #4a5568;
            font-style: italic;
            text-align: center;
        }
        
        .footer-section {
            text-align: center;
            margin-top: 60px;
            padding: 30px;
            background: rgba(255,255,255,0.1);
            border-radius: 15px;
        }
        
        .footer-text {
            font-size: 20px;
            color: #ffffff;
            margin-bottom: 15px;
        }
        
        .decorative-stars {
            font-size: 24px;
            color: #ffd700;
        }
        
        @media (max-width: 768px) {
            .main-title {
                font-size: 40px;
            }
            
            .friends-names {
                font-size: 28px;
            }
            
            .quote-text {
                font-size: 20px;
            }
            
            .quote-card {
                padding: 30px 20px;
            }
        }
    </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
  <script src="https://cdn.tailwindcss.com" type="text/javascript"></script>
 </head>
 <body>
  <div class="main-wrapper">
   <div class="content-container">
    <header class="header-section">
     <h1 class="main-title" id="mainTitle">Sahabat Sejati</h1>
     <div class="friends-names" id="friendsNames">
      Aldo &amp; Masdy
     </div>
     <div class="heart-icon">
      ❤️
     </div>
    </header>
    <main class="cards-section">
     <article class="quote-card">
      <div class="quote-icon">
       🌟
      </div>
      <p class="quote-text" id="quoteOne">Sahabat sejati adalah mereka yang tetap bersama di saat suka maupun duka, menjadi cahaya di kegelapan dan pelangi setelah badai</p>
     </article>
     <article class="quote-card">
      <div class="quote-icon">
       🤝
      </div>
      <p class="quote-text" id="quoteTwo">Persahabatan kalian seperti bintang di langit malam, selalu bersinar dan menunjukkan jalan di saat tersesat</p>
     </article>
     <article class="quote-card">
      <div class="quote-icon">
       💫
      </div>
      <p class="quote-text" id="quoteThree">Bersama sahabat sejati, setiap momen menjadi kenangan indah yang tak terlupakan, seperti melodi yang terus bergema di hati</p>
     </article>
    </main>
    <footer class="footer-section">
     <p class="footer-text">Persahabatan adalah harta paling berharga dalam hidup</p>
     <div class="decorative-stars">
      ✨ ⭐ ✨
     </div>
    </footer>
   </div>
  </div>
  <script>
        const defaultConfig = {
            main_title: "Sahabat Sejati",
            friend_one: "Aldo",
            friend_two: "Masdy",
            quote_one: "Sahabat sejati adalah mereka yang tetap bersama di saat suka maupun duka, menjadi cahaya di kegelapan dan pelangi setelah badai",
            quote_two: "Persahabatan kalian seperti bintang di langit malam, selalu bersinar dan menunjukkan jalan di saat tersesat",
            quote_three: "Bersama sahabat sejati, setiap momen menjadi kenangan indah yang tak terlupakan, seperti melodi yang terus bergema di hati",
            primary_color: "#667eea",
            secondary_color: "#764ba2",
            card_color: "#ffffff",
            text_color: "#4a5568",
            accent_color: "#ffd700",
            font_family: "Georgia",
            font_size: 16
        };

        async function onConfigChange(config) {
            const mainTitleEl = document.getElementById('mainTitle');
            const friendsNamesEl = document.getElementById('friendsNames');
            const quoteOneEl = document.getElementById('quoteOne');
            const quoteTwoEl = document.getElementById('quoteTwo');
            const quoteThreeEl = document.getElementById('quoteThree');

            if (mainTitleEl) {
                mainTitleEl.textContent = config.main_title || defaultConfig.main_title;
            }
            
            if (friendsNamesEl) {
                const friend1 = config.friend_one || defaultConfig.friend_one;
                const friend2 = config.friend_two || defaultConfig.friend_two;
                friendsNamesEl.textContent = `${friend1} & ${friend2}`;
            }
            
            if (quoteOneEl) {
                quoteOneEl.textContent = config.quote_one || defaultConfig.quote_one;
            }
            
            if (quoteTwoEl) {
                quoteTwoEl.textContent = config.quote_two || defaultConfig.quote_two;
            }
            
            if (quoteThreeEl) {
                quoteThreeEl.textContent = config.quote_three || defaultConfig.quote_three;
            }

            const primaryColor = config.primary_color || defaultConfig.primary_color;
            const secondaryColor = config.secondary_color || defaultConfig.secondary_color;
            const cardColor = config.card_color || defaultConfig.card_color;
            const textColor = config.text_color || defaultConfig.text_color;
            const accentColor = config.accent_color || defaultConfig.accent_color;
            const customFont = config.font_family || defaultConfig.font_family;
            const baseFontSize = config.font_size || defaultConfig.font_size;

            const wrapper = document.querySelector('.main-wrapper');
            if (wrapper) {
                wrapper.style.background = `linear-gradient(135deg, ${primaryColor} 0%, ${secondaryColor} 100%)`;
            }

            const cards = document.querySelectorAll('.quote-card');
            cards.forEach(card => {
                card.style.background = cardColor;
            });

            const quoteTexts = document.querySelectorAll('.quote-text');
            quoteTexts.forEach(text => {
                text.style.color = textColor;
            });

            const friendsName = document.querySelector('.friends-names');
            if (friendsName) {
                friendsName.style.color = accentColor;
            }

            const stars = document.querySelector('.decorative-stars');
            if (stars) {
                stars.style.color = accentColor;
            }

            document.body.style.fontFamily = `${customFont}, Georgia, serif`;
            
            if (mainTitleEl) {
                mainTitleEl.style.fontSize = `${baseFontSize * 3.5}px`;
            }
            
            if (friendsNamesEl) {
                friendsNamesEl.style.fontSize = `${baseFontSize * 2.25}px`;
            }
            
            quoteTexts.forEach(text => {
                text.style.fontSize = `${baseFontSize * 1.5}px`;
            });
            
            const footerText = document.querySelector('.footer-text');
            if (footerText) {
                footerText.style.fontSize = `${baseFontSize * 1.25}px`;
            }
        }

        function mapToCapabilities(config) {
            return {
                recolorables: [
                    {
                        get: () => config.primary_color || defaultConfig.primary_color,
                        set: (value) => {
                            config.primary_color = value;
                            window.elementSdk.setConfig({ primary_color: value });
                        }
                    },
                    {
                        get: () => config.secondary_color || defaultConfig.secondary_color,
                        set: (value) => {
                            config.secondary_color = value;
                            window.elementSdk.setConfig({ secondary_color: value });
                        }
                    },
                    {
                        get: () => config.card_color || defaultConfig.card_color,
                        set: (value) => {
                            config.card_color = value;
                            window.elementSdk.setConfig({ card_color: value });
                        }
                    },
                    {
                        get: () => config.text_color || defaultConfig.text_color,
                        set: (value) => {
                            config.text_color = value;
                            window.elementSdk.setConfig({ text_color: value });
                        }
                    },
                    {
                        get: () => config.accent_color || defaultConfig.accent_color,
                        set: (value) => {
                            config.accent_color = value;
                            window.elementSdk.setConfig({ accent_color: value });
                        }
                    }
                ],
                borderables: [],
                fontEditable: {
                    get: () => config.font_family || defaultConfig.font_family,
                    set: (value) => {
                        config.font_family = value;
                        window.elementSdk.setConfig({ font_family: value });
                    }
                },
                fontSizeable: {
                    get: () => config.font_size || defaultConfig.font_size,
                    set: (value) => {
                        config.font_size = value;
                        window.elementSdk.setConfig({ font_size: value });
                    }
                }
            };
        }

        function mapToEditPanelValues(config) {
            return new Map([
                ["main_title", config.main_title || defaultConfig.main_title],
                ["friend_one", config.friend_one || defaultConfig.friend_one],
                ["friend_two", config.friend_two || defaultConfig.friend_two],
                ["quote_one", config.quote_one || defaultConfig.quote_one],
                ["quote_two", config.quote_two || defaultConfig.quote_two],
                ["quote_three", config.quote_three || defaultConfig.quote_three]
            ]);
        }

        if (window.elementSdk) {
            window.elementSdk.init({
                defaultConfig,
                onConfigChange,
                mapToCapabilities,
                mapToEditPanelValues
            });
        }
    </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9a642b56211f8198',t:'MTc2NDQ0MDk1My4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html> DARI-RENDY SARAN
