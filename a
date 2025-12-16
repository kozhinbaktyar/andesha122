<!DOCTYPE html>
<html lang="ku" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="theme-color" content="#667eea">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="apple-mobile-web-app-title" content="بینەری داتا">
    <link rel="manifest" href="data:application/json;base64,ewogICJuYW1lIjogIsio24zZhtin2LHbjCDYr9in2KrYpyIsCiAgInNob3J0X25hbWUiOiAi2KjbjNmG2KfYsduMIiwKICAic3RhcnRfdXJsIjogIi8iLAogICJkaXNwbGF5IjogInN0YW5kYWxvbmUiLAogICJiYWNrZ3JvdW5kX2NvbG9yIjogIiNmZmZmZmYiLAogICJ0aGVtZV9jb2xvciI6ICIjNjY3ZWVhIiwKICAiaWNvbnMiOiBbCiAgICB7CiAgICAgICJzcmMiOiAiaHR0cHM6Ly93d3cuZ3N0YXRpYy5jb20vaW1hZ2VzL2JyYW5kaW5nL3Byb2R1Y3QvMXgvc2hlZXRzXzIwMjBxNF8xOTJkcC5wbmciLAogICAgICAic2l6ZXMiOiAiMTkyeDE5MiIsCiAgICAgICJ0eXBlIjogImltYWdlL3BuZyIKICAgIH0sCiAgICB7CiAgICAgICJzcmMiOiAiaHR0cHM6Ly93d3cuZ3N0YXRpYy5jb20vaW1hZ2VzL2JyYW5kaW5nL3Byb2R1Y3QvMXgvc2hlZXRzXzIwMjBxNF81MTJkcC5wbmciLAogICAgICAic2l6ZXMiOiAiNTEyeDUxMiIsCiAgICAgICJ0eXBlIjogImltYWdlL3BuZyIKICAgIH0KICBdCn0=">
    <title>بینەری داتا</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }
        
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            position: fixed;
            width: 100%;
            overflow: hidden;
        }
        
        .container {
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.2);
            padding: 40px;
            max-width: 600px;
            width: 100%;
            max-height: 90vh;
            overflow-y: auto;
        }
        
        h1 {
            color: #333;
            margin-bottom: 30px;
            text-align: center;
        }
        
        .login-form, .data-view {
            display: none;
        }
        
        .login-form.active, .data-view.active {
            display: block;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            color: #555;
            font-weight: bold;
        }
        
        input {
            width: 100%;
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
            transition: border-color 0.3s;
        }
        
        input:focus {
            outline: none;
            border-color: #667eea;
        }
        
        button {
            width: 100%;
            padding: 14px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: transform 0.2s;
        }
        
        button:hover {
            transform: translateY(-2px);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        .data-item {
            padding: 15px;
            background: #f8f9fa;
            border-radius: 8px;
            margin-bottom: 15px;
            border-right: 4px solid #667eea;
        }
        
        .data-item strong {
            color: #667eea;
            display: inline-block;
            min-width: 100px;
        }
        
        .error {
            background: #fee;
            color: #c33;
            padding: 12px;
            border-radius: 8px;
            margin-bottom: 15px;
            border-right: 4px solid #c33;
        }
        
        .loading {
            text-align: center;
            color: #667eea;
            font-size: 18px;
            padding: 20px;
        }
        
        .notification {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: #28a745;
            color: white;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.4);
            display: none;
            z-index: 10000;
            text-align: center;
            font-size: 16px;
            font-weight: bold;
        }
        
        .notification.show {
            display: block;
            animation: slideDown 0.4s ease;
        }
        
        @keyframes slideDown {
            from {
                transform: translateY(-100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }
        
        .install-prompt {
            background: #667eea;
            color: white;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .install-prompt button {
            margin-top: 10px;
            background: white;
            color: #667eea;
        }
        
        .status-indicator {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0,0,0,0.7);
            color: white;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 12px;
            z-index: 9999;
        }
        
        .status-indicator.online {
            background: rgba(40, 167, 69, 0.9);
        }
        
        @media (max-width: 768px) {
            body {
                padding: 10px;
            }
            
            .container {
                padding: 20px;
                margin: 0;
                border-radius: 10px;
            }
            
            .notification {
                padding: 15px;
                font-size: 14px;
            }
        }
    </style>
</head>
<body>
    <div class="notification" id="notification"></div>
    <div class="status-indicator" id="statusIndicator">🔄 چێککردن...</div>
    
    <div class="container">
        <div id="installPrompt" class="install-prompt" style="display:none;">
            <div>📱 دایبگرە وەک ئەپ</div>
            <button onclick="installApp()">دابگرە</button>
        </div>
        
        <!-- Login Form -->
        <div class="login-form active" id="loginForm">
            <h1>چوونەژوورەوە</h1>
            <div id="loginError"></div>
            <div class="form-group">
                <label for="userId">ID:</label>
                <input type="text" id="userId" placeholder="ID-ی خۆت بنووسە">
            </div>
            <button onclick="login()">چوونەژوورەوە</button>
        </div>
        
        <!-- Data View -->
        <div class="data-view" id="dataView">
            <h1>داتاکانت</h1>
            <div id="dataContent"></div>
        </div>
    </div>

    <script>
        const SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbxNAR8sqXtFv14Z_gG4ICCmOwHzP2rDsgOXMR6Q3r0zkkZRC_-XFaUnwTyhpOldBCvE/exec';
        
        let currentUserId = null;
        let lastColumnD = null;
        let checkInterval = null;
        let deferredPrompt = null;
        let isOnline = navigator.onLine;

        // Service Worker بۆ Background Notifications
        if ('serviceWorker' in navigator) {
            navigator.serviceWorker.register('data:text/javascript;base64,c2VsZi5hZGRFdmVudExpc3RlbmVyKCdpbnN0YWxsJywgZnVuY3Rpb24oZXZlbnQpIHsKICBzZWxmLnNraXBXYWl0aW5nKCk7Cn0pOwoKc2VsZi5hZGRFdmVudExpc3RlbmVyKCdhY3RpdmF0ZScsIGZ1bmN0aW9uKGV2ZW50KSB7CiAgcmV0dXJuIHNlbGYuY2xpZW50cy5jbGFpbSgpOwp9KTsKCnNlbGYuYWRkRXZlbnRMaXN0ZW5lcigncHVzaCcsIGZ1bmN0aW9uKGV2ZW50KSB7CiAgY29uc3Qgb3B0aW9ucyA9IHsKICAgIGJvZHk6IGV2ZW50LmRhdGEgPyBldmVudC5kYXRhLnRleHQoKSA6ICfZhtmI24zaqdin2LHYr9mG2YfZiNin2YYnLAogICAgaWNvbjogJ2h0dHBzOi8vd3d3LmdzdGF0aWMuY29tL2ltYWdlcy9icmFuZGluZy9wcm9kdWN0LzF4L3NoZWV0c18yMDIwcTRfNDhkcC5wbmcnLAogICAgdmlicmF0ZTogWzIwMCwgMTAwLCAyMDBdLAogICAgdGFnOiAnc2hlZXQtdXBkYXRlJwogIH07CiAgZXZlbnQud2FpdFVudGlsKAogICAgc2VsZi5yZWdpc3RyYXRpb24uc2hvd05vdGlmaWNhdGlvbign8J+UlCDZhtmI24zahtqp2LHYr9mG24zZiNin2YYnLCBvcHRpb25zKQogICk7Cn0pOw==')
                .then(reg => console.log('Service Worker registered'))
                .catch(err => console.log('Service Worker registration failed'));
        }

        // دەنگی ئاگادارکردنەوە
        function playNotificationSound() {
            try {
                const audioContext = new (window.AudioContext || window.webkitAudioContext)();
                const oscillator = audioContext.createOscillator();
                const gainNode = audioContext.createGain();
                
                oscillator.connect(gainNode);
                gainNode.connect(audioContext.destination);
                
                oscillator.frequency.value = 800;
                oscillator.type = 'sine';
                
                gainNode.gain.setValueAtTime(0.3, audioContext.currentTime);
                gainNode.gain.exponentialRampToValueAtTime(0.01, audioContext.currentTime + 0.5);
                
                oscillator.start(audioContext.currentTime);
                oscillator.stop(audioContext.currentTime + 0.5);
            } catch (e) {
                console.log('Audio not supported');
            }
        }

        // PWA Installation
        window.addEventListener('beforeinstallprompt', (e) => {
            e.preventDefault();
            deferredPrompt = e;
            document.getElementById('installPrompt').style.display = 'block';
        });

        function installApp() {
            if (deferredPrompt) {
                deferredPrompt.prompt();
                deferredPrompt.userChoice.then((choiceResult) => {
                    if (choiceResult.outcome === 'accepted') {
                        document.getElementById('installPrompt').style.display = 'none';
                    }
                    deferredPrompt = null;
                });
            }
        }

        // بەدواداچوونی بەستنەوە
        window.addEventListener('online', () => {
            isOnline = true;
            updateStatusIndicator();
            if (currentUserId) startMonitoring();
        });

        window.addEventListener('offline', () => {
            isOnline = false;
            updateStatusIndicator();
        });

        function updateStatusIndicator() {
            const indicator = document.getElementById('statusIndicator');
            if (isOnline) {
                indicator.textContent = '✓ بەستراوە';
                indicator.className = 'status-indicator online';
            } else {
                indicator.textContent = '✗ بەستنەوە نییە';
                indicator.className = 'status-indicator';
            }
            setTimeout(() => {
                indicator.style.display = 'none';
            }, 3000);
        }

        // بارکردنی یەکەم
        window.onload = function() {
            updateStatusIndicator();
            
            const savedId = localStorage.getItem('userId');
            if (savedId) {
                currentUserId = savedId;
                document.getElementById('userId').value = savedId;
                loadUserData(savedId);
            }
            
            // داواکردنی ڕێگەپێدان بۆ ناوتیفیکەیشن
            if ("Notification" in window && Notification.permission === "default") {
                Notification.requestPermission().then(permission => {
                    if (permission === "granted") {
                        showNotification("✓ ناوتیفیکەیشن چالاک کرا");
                    }
                });
            }
            
            // Keep screen awake
            if ('wakeLock' in navigator) {
                navigator.wakeLock.request('screen').catch(err => console.log(err));
            }
        };

        async function login() {
            const userId = document.getElementById('userId').value.trim();
            
            if (!userId) {
                showError('تکایە ID بنووسە');
                return;
            }
            
            if (!isOnline) {
                showError('بەستنەوە نییە. تکایە ئینتەرنێت چێک بکە');
                return;
            }
            
            showLoading();
            
            try {
                const response = await fetch(`${SCRIPT_URL}?action=getUserData&id=${userId}`);
                const data = await response.json();
                
                if (data.success) {
                    currentUserId = userId;
                    localStorage.setItem('userId', userId);
                    displayData(data.data);
                    startMonitoring();
                } else {
                    showError('ID نەدۆزرایەوە');
                }
            } catch (error) {
                showError('هەڵە لە بەستنەوە. تکایە دووبارە هەوڵبدەرەوە');
                console.error('Error:', error);
            }
        }

        function loadUserData(userId) {
            if (!isOnline) {
                showError('بەستنەوە نییە');
                return;
            }
            
            showLoading();
            
            fetch(`${SCRIPT_URL}?action=getUserData&id=${userId}`)
                .then(response => response.json())
                .then(data => {
                    if (data.success) {
                        displayData(data.data);
                        startMonitoring();
                    } else {
                        localStorage.removeItem('userId');
                        document.getElementById('dataView').classList.remove('active');
                        document.getElementById('loginForm').classList.add('active');
                    }
                })
                .catch(error => {
                    console.error('Error:', error);
                    showError('هەڵە لە بارکردن');
                });
        }

        function displayData(data) {
            document.getElementById('loginForm').classList.remove('active');
            document.getElementById('dataView').classList.add('active');
            
            let html = '';
            const columns = ['A', 'B', 'C', 'D', 'E', 'F'];
            const labels = {
                'A': 'ID',
                'B': 'کۆڵۆم B',
                'C': 'کۆڵۆم C',
                'D': 'کۆڵۆم D',
                'E': 'کۆڵۆم E',
                'F': 'مەسج'
            };
            
            columns.forEach(col => {
                if (data[col] !== undefined && data[col] !== null && data[col] !== '') {
                    html += `
                        <div class="data-item">
                            <strong>${labels[col]}:</strong> ${data[col]}
                        </div>
                    `;
                }
            });
            
            document.getElementById('dataContent').innerHTML = html;
            lastColumnD = data.D;
        }

        function startMonitoring() {
            if (checkInterval) clearInterval(checkInterval);
            checkInterval = setInterval(checkForUpdates, 30000);
        }

        async function checkForUpdates() {
            if (!currentUserId || !isOnline) return;
            
            try {
                const response = await fetch(`${SCRIPT_URL}?action=getUserData&id=${currentUserId}`);
                const data = await response.json();
                
                if (data.success && data.data.D !== lastColumnD && lastColumnD !== null) {
                    const message = `🔔 نوێکردنەوە: کۆڵۆم D گۆڕا بۆ "${data.data.D}"`;
                    
                    playNotificationSound();
                    showNotification(message);
                    
                    if ("Notification" in window && Notification.permission === "granted") {
                        try {
                            const notification = new Notification("🔔 نوێکردنەوە", {
                                body: message,
                                icon: "https://www.gstatic.com/images/branding/product/1x/sheets_2020q4_48dp.png",
                                badge: "https://www.gstatic.com/images/branding/product/1x/sheets_2020q4_48dp.png",
                                vibrate: [200, 100, 200, 100, 200],
                                requireInteraction: true,
                                tag: 'sheet-update',
                                silent: false
                            });
                            
                            notification.onclick = function() {
                                window.focus();
                                this.close();
                            };
                        } catch (e) {
                            console.log('Notification error:', e);
                        }
                    }
                    
                    if ('vibrate' in navigator) {
                        navigator.vibrate([200, 100, 200, 100, 200]);
                    }
                    
                    lastColumnD = data.data.D;
                    displayData(data.data);
                }
                
                if (lastColumnD === null && data.success) {
                    lastColumnD = data.data.D;
                }
            } catch (error) {
                console.error('Error checking updates:', error);
            }
        }

        function showError(message) {
            document.getElementById('loginError').innerHTML = `
                <div class="error">${message}</div>
            `;
            document.getElementById('dataContent').innerHTML = '';
        }

        function showLoading() {
            document.getElementById('dataContent').innerHTML = `
                <div class="loading">چاوەڕوان بە...</div>
            `;
            document.getElementById('loginError').innerHTML = '';
        }

        function showNotification(message) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            notification.classList.add('show');
            
            setTimeout(() => {
                notification.classList.remove('show');
            }, 5000);
        }

        // Keep app alive in background
        document.addEventListener('visibilitychange', function() {
            if (document.hidden && currentUserId) {
                console.log('App in background, monitoring continues');
            } else if (!document.hidden && currentUserId) {
                console.log('App in foreground');
                checkForUpdates();
            }
        });
    </script>
</body>
</html>
