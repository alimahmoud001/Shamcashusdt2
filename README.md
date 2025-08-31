<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تبادل USDT - شام كاش</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
            direction: rtl;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #4CAF50 0%, #45a049 100%);
            color: white;
            padding: 30px 20px;
            text-align: center;
        }

        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            font-weight: 700;
        }

        .header p {
            font-size: 1.1rem;
            opacity: 0.9;
        }

        .main-content {
            padding: 30px 20px;
        }

        .operation-selector {
            display: flex;
            gap: 15px;
            margin-bottom: 30px;
        }

        .operation-btn {
            flex: 1;
            padding: 15px 20px;
            border: 2px solid #e0e0e0;
            background: white;
            border-radius: 12px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1.1rem;
            font-weight: 600;
            text-align: center;
        }

        .operation-btn.active {
            background: #4CAF50;
            color: white;
            border-color: #4CAF50;
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(76, 175, 80, 0.3);
        }

        .operation-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }

        .form-section {
            display: none;
            animation: fadeIn 0.5s ease;
        }

        .form-section.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #333;
            font-size: 1rem;
        }

        .form-group input,
        .form-group select {
            width: 100%;
            padding: 15px;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            font-size: 1rem;
            transition: all 0.3s ease;
            background: #f9f9f9;
        }

        .form-group input:focus,
        .form-group select:focus {
            outline: none;
            border-color: #4CAF50;
            background: white;
            box-shadow: 0 0 0 3px rgba(76, 175, 80, 0.1);
        }

        .calculate-btn {
            width: 100%;
            padding: 18px;
            background: linear-gradient(135deg, #4CAF50 0%, #45a049 100%);
            color: white;
            border: none;
            border-radius: 12px;
            font-size: 1.2rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-bottom: 20px;
        }

        .calculate-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(76, 175, 80, 0.3);
        }

        .result-section {
            background: #f8f9fa;
            border-radius: 15px;
            padding: 25px;
            margin-top: 20px;
            border: 2px solid #e9ecef;
            display: none;
        }

        .result-section.show {
            display: block;
            animation: slideIn 0.5s ease;
        }

        @keyframes slideIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .result-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 0;
            border-bottom: 1px solid #e0e0e0;
        }

        .result-item:last-child {
            border-bottom: none;
        }

        .result-label {
            font-weight: 600;
            color: #555;
        }

        .result-value {
            font-weight: 700;
            color: #4CAF50;
            font-size: 1.1rem;
        }

        .address-section {
            background: #fff3cd;
            border: 2px solid #ffeaa7;
            border-radius: 12px;
            padding: 20px;
            margin: 20px 0;
        }

        .address-title {
            font-weight: 700;
            color: #856404;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        .address-value {
            background: #fff;
            padding: 15px;
            border-radius: 8px;
            font-family: 'Courier New', monospace;
            font-size: 0.9rem;
            word-break: break-all;
            border: 1px solid #ffeaa7;
            margin-bottom: 10px;
        }

        .copy-btn {
            background: #ffc107;
            color: #856404;
            border: none;
            padding: 8px 15px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .copy-btn:hover {
            background: #ffb300;
        }

        .instructions {
            background: #d1ecf1;
            border: 2px solid #bee5eb;
            border-radius: 12px;
            padding: 20px;
            margin: 20px 0;
        }

        .instructions h3 {
            color: #0c5460;
            margin-bottom: 15px;
            font-size: 1.2rem;
        }

        .instructions ul {
            list-style: none;
            padding: 0;
        }

        .instructions li {
            padding: 8px 0;
            color: #0c5460;
            position: relative;
            padding-right: 25px;
        }

        .instructions li:before {
            content: "✓";
            position: absolute;
            right: 0;
            color: #28a745;
            font-weight: bold;
        }

        .footer-note {
            background: #f8d7da;
            border: 2px solid #f5c6cb;
            border-radius: 12px;
            padding: 20px;
            margin: 20px 0;
            text-align: center;
            color: #721c24;
            font-weight: 600;
        }

        .telegram-link {
            color: #0088cc;
            text-decoration: none;
            font-weight: 700;
        }

        .telegram-link:hover {
            text-decoration: underline;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            body {
                padding: 10px;
            }

            .header h1 {
                font-size: 2rem;
            }

            .header p {
                font-size: 1rem;
            }

            .main-content {
                padding: 20px 15px;
            }

            .operation-selector {
                flex-direction: column;
                gap: 10px;
            }

            .operation-btn {
                padding: 12px 15px;
                font-size: 1rem;
            }

            .form-group input,
            .form-group select {
                padding: 12px;
                font-size: 0.9rem;
            }

            .calculate-btn {
                padding: 15px;
                font-size: 1.1rem;
            }

            .result-item {
                flex-direction: column;
                align-items: flex-start;
                gap: 5px;
            }

            .address-value {
                font-size: 0.8rem;
            }
        }

        @media (max-width: 480px) {
            .header {
                padding: 20px 15px;
            }

            .header h1 {
                font-size: 1.8rem;
            }

            .main-content {
                padding: 15px 10px;
            }

            .result-section,
            .address-section,
            .instructions {
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>💰 تبادل USDT</h1>
            <p>شراء وبيع USDT عبر شام كاش</p>
        </div>

        <div class="main-content">
            <div class="operation-selector">
                <div class="operation-btn active" onclick="selectOperation('buy')">
                    🛒 شراء USDT
                </div>
                <div class="operation-btn" onclick="selectOperation('sell')">
                    💸 بيع USDT
                </div>
            </div>

            <!-- Buy USDT Section -->
            <div id="buy-section" class="form-section active">
                <div class="form-group">
                    <label for="buy-amount">مبلغ USDT المراد شراؤه:</label>
                    <input type="number" id="buy-amount" placeholder="أدخل المبلغ بالـ USDT" step="0.01" min="0">
                </div>

                <div class="form-group">
                    <label for="buy-address">عنوان محفظتك (BEP20 فقط):</label>
                    <input type="text" id="buy-address" placeholder="أدخل عنوان محفظة BEP20">
                </div>

                <div class="form-group">
                    <label for="buy-currency">عملة الدفع:</label>
                    <select id="buy-currency">
                        <option value="syp">ليرة سورية (SYP)</option>
                        <option value="usd">دولار أمريكي (USD)</option>
                    </select>
                </div>

                <button class="calculate-btn" onclick="calculateBuy()">
                    احسب المبلغ المطلوب
                </button>
            </div>

            <!-- Sell USDT Section -->
            <div id="sell-section" class="form-section">
                <div class="form-group">
                    <label for="sell-amount">مبلغ USDT المراد بيعه:</label>
                    <input type="number" id="sell-amount" placeholder="أدخل المبلغ بالـ USDT" step="0.01" min="0">
                </div>

                <div class="form-group">
                    <label for="sell-shamcash">عنوان شام كاش الخاص بك:</label>
                    <input type="text" id="sell-shamcash" placeholder="أدخل عنوان شام كاش">
                </div>

                <div class="form-group">
                    <label for="sell-currency">عملة الاستلام:</label>
                    <select id="sell-currency">
                        <option value="syp">ليرة سورية (SYP)</option>
                        <option value="usd">دولار أمريكي (USD)</option>
                    </select>
                </div>

                <button class="calculate-btn" onclick="calculateSell()">
                    احسب المبلغ المستلم
                </button>
            </div>

            <!-- Results Section -->
            <div id="results" class="result-section">
                <div id="calculation-results"></div>
                <div id="address-info"></div>
                <div id="instructions-info"></div>
                <div class="footer-note">
                    عند تحويل المبلغ سوف يتم اعتماد سعر صرف الدولار كما هو سعر الصرف في البنك المركزي.
                </div>
            </div>
        </div>
    </div>

    <script>
        // Constants
        const USD_RATE = 11000; // سعر صرف الدولار بالليرة السورية
        const COMMISSION_FIXED = 1; // عمولة ثابتة بالدولار
        const COMMISSION_PERCENT = 0.005; // عمولة نسبية 0.5%
        const MY_SHAMCASH = "be456e0ea9392db4d68a7093ee317bc8";
        const MY_USDT_ADDRESS = "0x2F1A184B6abBb49De547D539eDC3b5eAdc3E01F9";
        const TELEGRAM_SUPPORT = "@ali0619000";
        const TELEGRAM_GROUP = "@shamcashusdt1";

        function selectOperation(operation) {
            // Update buttons
            document.querySelectorAll('.operation-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            event.target.classList.add('active');

            // Show/hide sections
            document.querySelectorAll('.form-section').forEach(section => {
                section.classList.remove('active');
            });
            
            if (operation === 'buy') {
                document.getElementById('buy-section').classList.add('active');
            } else {
                document.getElementById('sell-section').classList.add('active');
            }

            // Hide results
            document.getElementById('results').classList.remove('show');
        }

        function calculateBuy() {
            const amount = parseFloat(document.getElementById('buy-amount').value);
            const address = document.getElementById('buy-address').value.trim();
            const currency = document.getElementById('buy-currency').value;

            // التحقق من صحة البيانات
            if (!amount || amount <= 0) {
                showAlert('يرجى إدخال مبلغ صحيح', 'error');
                return;
            }

            if (!address) {
                showAlert('يرجى إدخال عنوان المحفظة', 'error');
                return;
            }

            // التحقق من صحة عنوان BEP20 (يبدأ بـ 0x ويحتوي على 42 حرف)
            if (!isValidBEP20Address(address)) {
                showAlert('عنوان المحفظة غير صحيح. يجب أن يكون عنوان BEP20 صحيح', 'error');
                return;
            }

            // حساب العمولة
            const commissionUSD = COMMISSION_FIXED + (amount * COMMISSION_PERCENT);
            const totalUSD = amount + commissionUSD;

            let paymentAmount, paymentCurrency;
            if (currency === 'syp') {
                paymentAmount = totalUSD * USD_RATE;
                paymentCurrency = 'ليرة سورية';
            } else {
                paymentAmount = totalUSD;
                paymentCurrency = 'دولار أمريكي';
            }

            displayBuyResults(amount, commissionUSD, totalUSD, paymentAmount, paymentCurrency, address);
        }

        function calculateSell() {
            const amount = parseFloat(document.getElementById('sell-amount').value);
            const shamcashAddress = document.getElementById('sell-shamcash').value.trim();
            const currency = document.getElementById('sell-currency').value;

            // التحقق من صحة البيانات
            if (!amount || amount <= 0) {
                showAlert('يرجى إدخال مبلغ صحيح', 'error');
                return;
            }

            if (!shamcashAddress) {
                showAlert('يرجى إدخال عنوان شام كاش', 'error');
                return;
            }

            // التحقق من صحة عنوان شام كاش (32 حرف hex)
            if (!isValidShamCashAddress(shamcashAddress)) {
                showAlert('عنوان شام كاش غير صحيح', 'error');
                return;
            }

            // حساب العمولة
            const commissionUSD = COMMISSION_FIXED + (amount * COMMISSION_PERCENT);
            const netUSD = amount - commissionUSD;

            if (netUSD <= 0) {
                showAlert('المبلغ صغير جداً. العمولة أكبر من المبلغ المراد بيعه', 'error');
                return;
            }

            let receiveAmount, receiveCurrency;
            if (currency === 'syp') {
                receiveAmount = netUSD * USD_RATE;
                receiveCurrency = 'ليرة سورية';
            } else {
                receiveAmount = netUSD;
                receiveCurrency = 'دولار أمريكي';
            }

            displaySellResults(amount, commissionUSD, netUSD, receiveAmount, receiveCurrency, shamcashAddress);
        }

        function displayBuyResults(amount, commission, total, payment, currency, address) {
            const resultsHTML = `
                <div class="result-item">
                    <span class="result-label">مبلغ USDT:</span>
                    <span class="result-value">${amount.toFixed(2)} USDT</span>
                </div>
                <div class="result-item">
                    <span class="result-label">العمولة:</span>
                    <span class="result-value">${commission.toFixed(2)} USD</span>
                </div>
                <div class="result-item">
                    <span class="result-label">المجموع بالدولار:</span>
                    <span class="result-value">${total.toFixed(2)} USD</span>
                </div>
                <div class="result-item">
                    <span class="result-label">المبلغ المطلوب دفعه:</span>
                    <span class="result-value">${payment.toLocaleString()} ${currency}</span>
                </div>
            `;

            const addressHTML = `
                <div class="address-section">
                    <div class="address-title">عنوان شام كاش للدفع:</div>
                    <div class="address-value">${MY_SHAMCASH}</div>
                    <button class="copy-btn" onclick="copyToClipboard('${MY_SHAMCASH}')">نسخ العنوان</button>
                </div>
            `;

            const instructionsHTML = `
                <div class="instructions">
                    <h3>تعليمات الشراء:</h3>
                    <ul>
                        <li>قم بتحويل المبلغ ${payment.toLocaleString()} ${currency} إلى عنوان شام كاش أعلاه</li>
                        <li>التقط لقطة شاشة للتحويل</li>
                        <li>أرسل لقطة الشاشة إلى الدعم: <a href="https://t.me/${TELEGRAM_SUPPORT.substring(1)}" class="telegram-link">${TELEGRAM_SUPPORT}</a></li>
                        <li>سيتم إرسال ${amount.toFixed(2)} USDT إلى عنوانك: ${address}</li>
                        <li>الشبكة: BEP20 فقط</li>
                    </ul>
                </div>
            `;

            document.getElementById('calculation-results').innerHTML = resultsHTML;
            document.getElementById('address-info').innerHTML = addressHTML;
            document.getElementById('instructions-info').innerHTML = instructionsHTML;
            document.getElementById('results').classList.add('show');

            // إرسال التقرير إلى التلجرام (سيتم تنفيذه لاحقاً)
            sendReportToTelegram('buy', {
                amount: amount,
                commission: commission,
                total: total,
                payment: payment,
                currency: currency,
                address: address
            });
        }

        function displaySellResults(amount, commission, net, receive, currency, shamcashAddress) {
            const resultsHTML = `
                <div class="result-item">
                    <span class="result-label">مبلغ USDT للبيع:</span>
                    <span class="result-value">${amount.toFixed(2)} USDT</span>
                </div>
                <div class="result-item">
                    <span class="result-label">العمولة:</span>
                    <span class="result-value">${commission.toFixed(2)} USD</span>
                </div>
                <div class="result-item">
                    <span class="result-label">الصافي بالدولار:</span>
                    <span class="result-value">${net.toFixed(2)} USD</span>
                </div>
                <div class="result-item">
                    <span class="result-label">المبلغ المستلم:</span>
                    <span class="result-value">${receive.toLocaleString()} ${currency}</span>
                </div>
            `;

            const addressHTML = `
                <div class="address-section">
                    <div class="address-title">عنوان USDT للإرسال (BEP20):</div>
                    <div class="address-value">${MY_USDT_ADDRESS}</div>
                    <button class="copy-btn" onclick="copyToClipboard('${MY_USDT_ADDRESS}')">نسخ العنوان</button>
                </div>
            `;

            const instructionsHTML = `
                <div class="instructions">
                    <h3>تعليمات البيع:</h3>
                    <ul>
                        <li>أرسل ${amount.toFixed(2)} USDT إلى العنوان أعلاه</li>
                        <li>الشبكة: BEP20 فقط</li>
                        <li>التقط لقطة شاشة للتحويل</li>
                        <li>أرسل لقطة الشاشة إلى الدعم: <a href="https://t.me/${TELEGRAM_SUPPORT.substring(1)}" class="telegram-link">${TELEGRAM_SUPPORT}</a></a></li>
                        <li>سيتم إرسال ${receive.toLocaleString()} ${currency} إلى شام كاش: ${shamcashAddress}</li>
                        <li>انتظر عدة دقائق لاستلام المبلغ</li>
                    </ul>
                </div>
            `;

            document.getElementById('calculation-results').innerHTML = resultsHTML;
            document.getElementById('address-info').innerHTML = addressHTML;
            document.getElementById('instructions-info').innerHTML = instructionsHTML;
            document.getElementById('results').classList.add('show');

            // إرسال التقرير إلى التلجرام (سيتم تنفيذه لاحقاً)
            sendReportToTelegram('sell', {
                amount: amount,
                commission: commission,
                net: net,
                receive: receive,
                currency: currency,
                shamcashAddress: shamcashAddress
            });
        }

        function copyToClipboard(text) {
            navigator.clipboard.writeText(text).then(function() {
                alert('تم نسخ العنوان بنجاح!');
            }, function(err) {
                console.error('فشل في نسخ العنوان: ', err);
                // Fallback for older browsers
                const textArea = document.createElement("textarea");
                textArea.value = text;
                document.body.appendChild(textArea);
                textArea.focus();
                textArea.select();
                try {
                    document.execCommand('copy');
                    alert('تم نسخ العنوان بنجاح!');
                } catch (err) {
                    alert('فشل في نسخ العنوان');
                }
                document.body.removeChild(textArea);
            });
        }

        function sendReportToTelegram(operation, data) {
            // هذه الوظيفة تحتاج إلى تكامل مع Telegram Bot API
            // يمكن تنفيذها لاحقاً باستخدام خادم خلفي أو خدمة ويب
            console.log('إرسال تقرير إلى التلجرام:', operation, data);
            
            // إنشاء رسالة التقرير
            let reportMessage = '';
            const currentTime = new Date().toLocaleString('ar-EG', {
                timeZone: 'Asia/Damascus',
                year: 'numeric',
                month: '2-digit',
                day: '2-digit',
                hour: '2-digit',
                minute: '2-digit'
            });

            if (operation === 'buy') {
                reportMessage = `🛒 طلب شراء USDT جديد
⏰ الوقت: ${currentTime}
💰 المبلغ: ${data.amount.toFixed(2)} USDT
💵 العمولة: ${data.commission.toFixed(2)} USD
📊 المجموع: ${data.total.toFixed(2)} USD
💳 المبلغ المطلوب: ${data.payment.toLocaleString()} ${data.currency}
🏦 عنوان المحفظة: ${data.address}
📱 شبكة: BEP20`;
            } else {
                reportMessage = `💸 طلب بيع USDT جديد
⏰ الوقت: ${currentTime}
💰 المبلغ: ${data.amount.toFixed(2)} USDT
💵 العمولة: ${data.commission.toFixed(2)} USD
📊 الصافي: ${data.net.toFixed(2)} USD
💳 المبلغ المستلم: ${data.receive.toLocaleString()} ${data.currency}
🏦 عنوان شام كاش: ${data.shamcashAddress}`;
            }

            // يمكن إضافة كود هنا لإرسال البيانات إلى خادم يقوم بإرسالها إلى التلجرام
            // أو استخدام خدمة ويب مثل Zapier أو IFTTT
            
            // عرض الرسالة في وحدة التحكم للمطور
            console.log('رسالة التقرير:', reportMessage);
        }

        // وظائف التحقق من صحة العناوين
        function isValidBEP20Address(address) {
            // التحقق من أن العنوان يبدأ بـ 0x ويحتوي على 42 حرف
            const bep20Regex = /^0x[a-fA-F0-9]{40}$/;
            return bep20Regex.test(address);
        }

        function isValidShamCashAddress(address) {
            // التحقق من أن عنوان شام كاش يحتوي على 32 حرف hex
            const shamcashRegex = /^[a-fA-F0-9]{32}$/;
            return shamcashRegex.test(address);
        }

        // نظام التنبيهات المحسن
        function showAlert(message, type = 'info') {
            // إزالة التنبيهات السابقة
            const existingAlert = document.querySelector('.custom-alert');
            if (existingAlert) {
                existingAlert.remove();
            }

            // إنشاء التنبيه الجديد
            const alertDiv = document.createElement('div');
            alertDiv.className = `custom-alert alert-${type}`;
            
            const alertColors = {
                'error': '#f8d7da',
                'success': '#d4edda',
                'warning': '#fff3cd',
                'info': '#d1ecf1'
            };

            const alertTextColors = {
                'error': '#721c24',
                'success': '#155724',
                'warning': '#856404',
                'info': '#0c5460'
            };

            alertDiv.style.cssText = `
                position: fixed;
                top: 20px;
                left: 50%;
                transform: translateX(-50%);
                background: ${alertColors[type]};
                color: ${alertTextColors[type]};
                padding: 15px 25px;
                border-radius: 8px;
                border: 2px solid ${alertColors[type]};
                box-shadow: 0 4px 12px rgba(0,0,0,0.15);
                z-index: 1000;
                font-weight: 600;
                max-width: 90%;
                text-align: center;
                animation: slideDown 0.3s ease;
            `;

            alertDiv.textContent = message;
            document.body.appendChild(alertDiv);

            // إزالة التنبيه بعد 5 ثوان
            setTimeout(() => {
                if (alertDiv.parentNode) {
                    alertDiv.style.animation = 'slideUp 0.3s ease';
                    setTimeout(() => alertDiv.remove(), 300);
                }
            }, 5000);

            // إضافة الأنيميشن
            if (!document.querySelector('#alert-animations')) {
                const style = document.createElement('style');
                style.id = 'alert-animations';
                style.textContent = `
                    @keyframes slideDown {
                        from { transform: translateX(-50%) translateY(-100%); opacity: 0; }
                        to { transform: translateX(-50%) translateY(0); opacity: 1; }
                    }
                    @keyframes slideUp {
                        from { transform: translateX(-50%) translateY(0); opacity: 1; }
                        to { transform: translateX(-50%) translateY(-100%); opacity: 0; }
                    }
                `;
                document.head.appendChild(style);
            }
        }

        // تحسين تجربة المستخدم على الجوال
        document.addEventListener('DOMContentLoaded', function() {
            // منع التكبير عند النقر على حقول الإدخال في iOS
            if (/iPad|iPhone|iPod/.test(navigator.userAgent)) {
                const inputs = document.querySelectorAll('input, select');
                inputs.forEach(input => {
                    input.addEventListener('focus', function() {
                        input.style.fontSize = '16px';
                    });
                });
            }
        });
    </script>
</body>
</html>
