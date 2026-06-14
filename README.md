<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, viewport-fit=cover">
    <meta name="description" content="Calculator Suite - Free professional online calculators including Basic Calculator and Age Calculator. Simple, fast, and privacy-focused tools for everyday calculations.">
    <meta name="keywords" content="calculator, online calculator, age calculator, basic calculator, free calculator, arithmetic calculator, date calculator, age computation">
    <meta name="author" content="Calculator Suite">
    <meta name="robots" content="index, follow">
    <meta name="language" content="English">
    <meta name="revisit-after" content="7 days">
    
    <!-- Open Graph / Social Media Meta Tags -->
    <meta property="og:title" content="Calculator Suite | Free Online Calculators">
    <meta property="og:description" content="Professional free calculators including Basic Calculator and Age Calculator. Fast, accurate, and privacy-focused.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://calculatorsuite.example.com">
    <meta property="og:image" content="https://calculatorsuite.example.com/og-image.jpg">
    
    <!-- Twitter Card Meta Tags -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Calculator Suite | Free Online Calculators">
    <meta name="twitter:description" content="Professional free calculators including Basic Calculator and Age Calculator.">
    
    <title>Calculator Suite | Free Basic Calculator & Age Calculator</title>
    
    <style>
        /* ========== RESET & VARIABLES ========== */
        :root {
            --primary-gradient-start: #667eea;
            --primary-gradient-end: #764ba2;
            --primary-dark: #5a67d8;
            --success-color: #51cf66;
            --danger-color: #ff6b6b;
            --warning-color: #ffd43b;
            --gray-light: #f8f9fa;
            --gray-medium: #e9ecef;
            --gray-dark: #6c757d;
            --text-primary: #212529;
            --text-secondary: #495057;
            --border-radius-sm: 12px;
            --border-radius-md: 20px;
            --border-radius-lg: 40px;
            --shadow-sm: 0 2px 8px rgba(0, 0, 0, 0.1);
            --shadow-md: 0 10px 30px rgba(0, 0, 0, 0.2);
            --shadow-lg: 0 20px 60px rgba(0, 0, 0, 0.3);
            --transition-fast: 0.2s ease;
            --transition-normal: 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        /* ========== BASE STYLES ========== */
        body {
            min-height: 100vh;
            background: linear-gradient(135deg, var(--primary-gradient-start) 0%, var(--primary-gradient-end) 100%);
            font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, 'Roboto', 'Poppins', sans-serif;
            padding: 20px;
            line-height: 1.5;
        }

        /* ========== CONTAINER ========== */
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        /* ========== NAVIGATION BAR ========== */
        .navbar {
            background: rgba(255, 255, 255, 0.98);
            border-radius: var(--border-radius-lg);
            padding: 12px 24px;
            margin-bottom: 30px;
            box-shadow: var(--shadow-md);
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
            backdrop-filter: blur(10px);
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, var(--primary-gradient-start), var(--primary-gradient-end));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: -0.5px;
        }

        .nav-links {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .nav-btn {
            background: transparent;
            border: none;
            padding: 10px 20px;
            font-size: 0.95rem;
            font-weight: 600;
            cursor: pointer;
            border-radius: 25px;
            transition: all var(--transition-fast);
            color: var(--text-secondary);
        }

        .nav-btn:hover {
            background: var(--gray-medium);
            transform: translateY(-2px);
        }

        .nav-btn:focus-visible {
            outline: 3px solid var(--primary-gradient-start);
            outline-offset: 2px;
        }

        .nav-btn.active {
            background: linear-gradient(135deg, var(--primary-gradient-start), var(--primary-gradient-end));
            color: white;
            box-shadow: var(--shadow-sm);
        }

        /* ========== PAGE CONTAINERS ========== */
        .page-content {
            animation: fadeIn var(--transition-normal);
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hidden {
            display: none;
        }

        /* ========== CALCULATOR & CARD STYLES ========== */
        .calculator-card, .age-calculator, .info-card {
            background: rgba(255, 255, 255, 0.98);
            border-radius: var(--border-radius-lg);
            padding: 30px;
            box-shadow: var(--shadow-lg);
        }

        .info-card {
            max-width: 900px;
            margin: 0 auto;
        }

        /* ========== DISPLAY SCREEN ========== */
        .display-section {
            margin-bottom: 25px;
        }

        .previous-operand {
            background: var(--gray-light);
            padding: 12px 20px;
            border-radius: var(--border-radius-md);
            margin-bottom: 10px;
            text-align: right;
            font-size: 1.1rem;
            color: var(--gray-dark);
            min-height: 55px;
            word-wrap: break-word;
            word-break: break-all;
            font-family: 'Courier New', monospace;
        }

        .current-display {
            background: var(--gray-light);
            border-radius: var(--border-radius-md);
            padding: 5px 20px;
        }

        .current-display input {
            width: 100%;
            height: 85px;
            font-size: 2.5rem;
            text-align: right;
            background: transparent;
            border: none;
            color: var(--text-primary);
            font-weight: 600;
            font-family: 'Courier New', monospace;
            outline: none;
            padding: 0;
        }

        /* ========== BUTTONS GRID ========== */
        .buttons-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 12px;
        }

        .calc-btn {
            border: none;
            outline: none;
            background: white;
            padding: 20px 0;
            border-radius: var(--border-radius-md);
            font-size: 1.4rem;
            font-weight: 600;
            cursor: pointer;
            transition: all var(--transition-fast);
            color: var(--text-primary);
            box-shadow: var(--shadow-sm);
        }

        .calc-btn:active {
            transform: scale(0.95);
        }

        .calc-btn:focus-visible {
            outline: 3px solid var(--primary-gradient-start);
            outline-offset: 2px;
        }

        .number-btn {
            background: #ffffff;
        }

        .operator-btn {
            background: var(--warning-color);
            font-size: 1.6rem;
        }

        .clear-btn {
            background: var(--danger-color);
            color: white;
        }

        .equals-btn {
            background: var(--success-color);
            color: white;
            font-size: 1.6rem;
        }

        .delete-btn {
            background: var(--gray-dark);
            color: white;
            font-size: 1.2rem;
        }

        .zero-btn {
            grid-column: span 2;
        }

        /* ========== AGE CALCULATOR STYLES ========== */
        .age-title {
            text-align: center;
            margin-bottom: 10px;
            color: var(--text-primary);
        }

        .age-subtitle {
            text-align: center;
            color: var(--gray-dark);
            margin-bottom: 25px;
        }

        .input-group {
            margin-bottom: 25px;
        }

        .input-group label {
            display: block;
            margin-bottom: 10px;
            font-weight: 600;
            color: var(--text-primary);
            font-size: 0.95rem;
        }

        .input-group input {
            width: 100%;
            padding: 14px 16px;
            font-size: 1rem;
            border: 2px solid var(--gray-medium);
            border-radius: var(--border-radius-sm);
            outline: none;
            transition: all var(--transition-fast);
            font-family: inherit;
        }

        .input-group input:focus {
            border-color: var(--primary-gradient-start);
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
        }

        .input-group small {
            color: var(--gray-dark);
            display: block;
            margin-top: 5px;
            font-size: 0.8rem;
        }

        .calculate-btn {
            background: linear-gradient(135deg, var(--primary-gradient-start), var(--primary-gradient-end));
            color: white;
            padding: 14px 30px;
            font-size: 1rem;
            font-weight: 600;
            width: 100%;
            margin: 10px 0;
            border: none;
            border-radius: var(--border-radius-sm);
            cursor: pointer;
            transition: all var(--transition-fast);
        }

        .calculate-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .calculate-btn:active {
            transform: translateY(0);
        }

        /* ========== RESULTS STYLES ========== */
        .age-result {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.08), rgba(118, 75, 162, 0.08));
            padding: 25px;
            border-radius: var(--border-radius-md);
            margin-top: 20px;
            animation: slideUp var(--transition-normal);
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .age-result h3 {
            color: var(--text-primary);
            margin-bottom: 20px;
            font-size: 1.2rem;
            text-align: center;
        }

        .result-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 0;
            border-bottom: 1px solid rgba(0, 0, 0, 0.08);
        }

        .result-item:last-child {
            border-bottom: none;
        }

        .result-label {
            font-weight: 600;
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .result-value {
            color: var(--primary-gradient-start);
            font-weight: 700;
            font-size: 1rem;
        }

        .error-message {
            background: #fee;
            color: #c33;
            padding: 15px;
            border-radius: var(--border-radius-sm);
            text-align: center;
            margin-top: 20px;
            border-left: 4px solid #c33;
        }

        /* ========== INFO PAGE STYLES ========== */
        .info-card h1 {
            color: var(--text-primary);
            margin-bottom: 20px;
            font-size: 1.8rem;
        }

        .info-card h2 {
            color: var(--text-secondary);
            margin: 25px 0 12px;
            font-size: 1.3rem;
        }

        .info-card h3 {
            color: var(--text-secondary);
            margin: 20px 0 10px;
            font-size: 1.1rem;
        }

        .info-card p {
            color: var(--gray-dark);
            line-height: 1.7;
            margin-bottom: 15px;
        }

        .info-card ul, .info-card ol {
            margin: 15px 0 15px 25px;
            color: var(--gray-dark);
            line-height: 1.7;
        }

        .info-card li {
            margin: 8px 0;
        }

        .contact-box {
            background: var(--gray-light);
            padding: 25px;
            border-radius: var(--border-radius-md);
            margin: 20px 0;
        }

        .email-display {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 15px;
            background: white;
            padding: 15px;
            border-radius: var(--border-radius-sm);
            margin-top: 10px;
        }

        .email-address {
            font-size: 1rem;
            font-weight: 600;
            color: var(--primary-gradient-start);
            word-break: break-all;
        }

        .copy-btn {
            background: linear-gradient(135deg, var(--primary-gradient-start), var(--primary-gradient-end));
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: var(--border-radius-sm);
            cursor: pointer;
            font-size: 0.85rem;
            font-weight: 500;
            transition: all var(--transition-fast);
        }

        .copy-btn:hover {
            transform: scale(1.02);
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .feature-item {
            background: var(--gray-light);
            padding: 20px;
            border-radius: var(--border-radius-md);
            text-align: center;
        }

        .feature-icon {
            font-size: 2rem;
            margin-bottom: 10px;
        }

        .faq-item {
            background: var(--gray-light);
            border-radius: var(--border-radius-md);
            margin-bottom: 15px;
            overflow: hidden;
        }

        .faq-question {
            padding: 18px 20px;
            font-weight: 600;
            color: var(--text-primary);
            cursor: pointer;
            background: var(--gray-light);
            transition: background var(--transition-fast);
        }

        .faq-question:hover {
            background: var(--gray-medium);
        }

        .faq-answer {
            padding: 0 20px;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease, padding 0.3s ease;
        }

        .faq-item.active .faq-answer {
            padding: 0 20px 18px 20px;
            max-height: 300px;
        }

        /* ========== FOOTER ========== */
        .footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: rgba(255, 255, 255, 0.9);
            font-size: 0.85rem;
            border-top: 1px solid rgba(255, 255, 255, 0.2);
        }

        .footer p {
            margin: 5px 0;
        }

        .footer a {
            color: white;
            text-decoration: none;
            font-weight: 500;
        }

        .footer a:hover {
            text-decoration: underline;
        }

        /* ========== RESPONSIVE DESIGN ========== */
        @media (max-width: 768px) {
            body {
                padding: 15px;
            }

            .navbar {
                flex-direction: column;
                text-align: center;
                padding: 15px;
            }

            .calculator-card, .age-calculator, .info-card {
                padding: 20px;
            }

            .current-display input {
                height: 70px;
                font-size: 2rem;
            }

            .calc-btn {
                padding: 15px 0;
                font-size: 1.2rem;
            }

            .operator-btn, .equals-btn {
                font-size: 1.4rem;
            }

            .result-item {
                flex-direction: column;
                align-items: flex-start;
                gap: 5px;
            }
        }

        @media (max-width: 480px) {
            .calc-btn {
                padding: 12px 0;
                font-size: 1.1rem;
            }

            .info-card h1 {
                font-size: 1.5rem;
            }

            .info-card h2 {
                font-size: 1.2rem;
            }

            .email-display {
                flex-direction: column;
            }

            .copy-btn {
                width: 100%;
            }
        }

        @media (max-width: 360px) {
            .calc-btn {
                padding: 10px 0;
                font-size: 1rem;
            }

            .current-display input {
                height: 60px;
                font-size: 1.6rem;
            }
        }

        /* Landscape mode optimization */
        @media (max-height: 500px) and (orientation: landscape) {
            body {
                padding: 10px;
            }

            .calculator-card, .age-calculator {
                padding: 15px;
            }

            .calc-btn {
                padding: 8px 0;
            }

            .current-display input {
                height: 50px;
                font-size: 1.5rem;
            }
        }

        /* Print styles */
        @media print {
            .navbar, .footer, .calculate-btn {
                display: none;
            }

            .page-content {
                display: block !important;
            }
        }

        /* Accessibility - Reduced motion */
        @media (prefers-reduced-motion: reduce) {
            * {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
            }
        }

        /* Animation for calculator result */
        .result-pulse {
            animation: pulse 0.3s ease;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.02); }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Navigation -->
        <nav class="navbar" aria-label="Main navigation">
            <div class="logo" aria-label="Calculator Suite logo">✨ Calculator Suite</div>
            <div class="nav-links">
                <button class="nav-btn active" onclick="showPage('home')" aria-label="Go to Home">🏠 Home</button>
                <button class="nav-btn" onclick="showPage('calculator')" aria-label="Open Basic Calculator">🧮 Calculator</button>
                <button class="nav-btn" onclick="showPage('age')" aria-label="Open Age Calculator">🎂 Age Calculator</button>
                <button class="nav-btn" onclick="showPage('privacy')" aria-label="View Privacy Policy">🔒 Privacy</button>
                <button class="nav-btn" onclick="showPage('about')" aria-label="Learn About Us">ℹ️ About</button>
                <button class="nav-btn" onclick="showPage('contact')" aria-label="Contact Us">📧 Contact</button>
            </div>
        </nav>

        <!-- HOME PAGE with Introduction and FAQ -->
        <div id="home-page" class="page-content">
            <div class="info-card">
                <h1>✨ Welcome to Calculator Suite</h1>
                <p>Your go-to destination for fast, accurate, and completely free online calculators. No registration, no data collection, just reliable calculations right in your browser.</p>

                <h2>🚀 What We Offer</h2>
                <div class="feature-grid">
                    <div class="feature-item">
                        <div class="feature-icon">🧮</div>
                        <h3>Basic Calculator</h3>
                        <p>Perform addition, subtraction, multiplication, and division with our easy-to-use calculator.</p>
                    </div>
                    <div class="feature-item">
                        <div class="feature-icon">🎂</div>
                        <h3>Age Calculator</h3>
                        <p>Calculate exact age in years, months, days, and even get zodiac sign and age group information.</p>
                    </div>
                    <div class="feature-item">
                        <div class="feature-icon">🔒</div>
                        <h3>100% Private</h3>
                        <p>All calculations happen locally in your browser. We never store or share your data.</p>
                    </div>
                </div>

                <h2>💡 Why Choose Calculator Suite?</h2>
                <ul>
                    <li>✓ <strong>Completely Free</strong> - No hidden charges or premium tiers</li>
                    <li>✓ <strong>No Registration Required</strong> - Use instantly without creating an account</li>
                    <li>✓ <strong>Privacy Focused</strong> - Zero data collection, all calculations are local</li>
                    <li>✓ <strong>Mobile Responsive</strong> - Works perfectly on phones, tablets, and desktops</li>
                    <li>✓ <strong>Keyboard Support</strong> - Use your keyboard for faster calculations</li>
                    <li>✓ <strong>Instant Results</strong> - Real-time calculations with no waiting</li>
                </ul>

                <h2>❓ Frequently Asked Questions</h2>
                <div class="faq-item" id="faq1">
                    <div class="faq-question" onclick="toggleFAQ('faq1')">📌 Is Calculator Suite really free?</div>
                    <div class="faq-answer">Yes! Calculator Suite is 100% free to use. There are no hidden fees, subscription plans, or premium features. All calculators are available to everyone at no cost.</div>
                </div>
                <div class="faq-item" id="faq2">
                    <div class="faq-question" onclick="toggleFAQ('faq2')">🔒 Do you collect my personal data?</div>
                    <div class="faq-answer">No, we do not collect any personal data. All calculations are performed locally in your browser. We never store, share, or have access to your inputs or results.</div>
                </div>
                <div class="faq-item" id="faq3">
                    <div class="faq-question" onclick="toggleFAQ('faq3')">📱 Does it work on mobile devices?</div>
                    <div class="faq-answer">Absolutely! Our website is fully responsive and works seamlessly on smartphones, tablets, laptops, and desktop computers. The interface adapts to your screen size for the best experience.</div>
                </div>
                <div class="faq-item" id="faq4">
                    <div class="faq-question" onclick="toggleFAQ('faq4')">⌨️ Can I use my keyboard with the calculator?</div>
                    <div class="faq-answer">Yes! The basic calculator supports keyboard input. Use number keys (0-9), operators (+, -, *, /), Enter or = for results, Backspace to delete, and Escape to clear.</div>
                </div>
                <div class="faq-item" id="faq5">
                    <div class="faq-question" onclick="toggleFAQ('faq5')">🎂 How accurate is the Age Calculator?</div>
                    <div class="faq-answer">The Age Calculator is highly accurate. It accounts for leap years, different month lengths, and provides results in years, months, days, weeks, total days, hours, minutes, and seconds.</div>
                </div>

                <h2>🛠️ Coming Soon</h2>
                <p>We're constantly improving and adding new features. Stay tuned for more useful tools while maintaining our commitment to privacy and simplicity.</p>
            </div>
        </div>

        <!-- MAIN CALCULATOR PAGE -->
        <div id="calculator-page" class="page-content hidden">
            <div class="calculator-card">
                <div class="display-section">
                    <div class="previous-operand" id="previousOperand" aria-label="Previous calculation"></div>
                    <div class="current-display">
                        <input type="text" id="display" value="0" readonly aria-label="Current calculation display">
                    </div>
                </div>
                
                <div class="buttons-grid" role="group" aria-label="Calculator buttons">
                    <button class="calc-btn clear-btn" onclick="clearAll()" aria-label="Clear all">AC</button>
                    <button class="calc-btn delete-btn" onclick="deleteLast()" aria-label="Delete last character">⌫</button>
                    <button class="calc-btn operator-btn" onclick="appendOperator('/')" aria-label="Divide">÷</button>
                    <button class="calc-btn operator-btn" onclick="appendOperator('*')" aria-label="Multiply">×</button>
                    
                    <button class="calc-btn number-btn" onclick="appendNumber('7')" aria-label="Seven">7</button>
                    <button class="calc-btn number-btn" onclick="appendNumber('8')" aria-label="Eight">8</button>
                    <button class="calc-btn number-btn" onclick="appendNumber('9')" aria-label="Nine">9</button>
                    <button class="calc-btn operator-btn" onclick="appendOperator('-')" aria-label="Subtract">−</button>
                    
                    <button class="calc-btn number-btn" onclick="appendNumber('4')" aria-label="Four">4</button>
                    <button class="calc-btn number-btn" onclick="appendNumber('5')" aria-label="Five">5</button>
                    <button class="calc-btn number-btn" onclick="appendNumber('6')" aria-label="Six">6</button>
                    <button class="calc-btn operator-btn" onclick="appendOperator('+')" aria-label="Add">+</button>
                    
                    <button class="calc-btn number-btn" onclick="appendNumber('1')" aria-label="One">1</button>
                    <button class="calc-btn number-btn" onclick="appendNumber('2')" aria-label="Two">2</button>
                    <button class="calc-btn number-btn" onclick="appendNumber('3')" aria-label="Three">3</button>
                    <button class="calc-btn equals-btn" onclick="calculateResult()" aria-label="Calculate result">=</button>
                    
                    <button class="calc-btn number-btn zero-btn" onclick="appendNumber('0')" aria-label="Zero">0</button>
                    <button class="calc-btn number-btn" onclick="appendNumber('.')" aria-label="Decimal point">.</button>
                </div>
            </div>
        </div>

        <!-- AGE CALCULATOR PAGE -->
        <div id="age-page" class="page-content hidden">
            <div class="age-calculator">
                <h1 class="age-title">🎂 Age Calculator</h1>
                <p class="age-subtitle">Calculate your exact age in years, months, and days</p>
                
                <div class="input-group">
                    <label for="dob">📅 Date of Birth *</label>
                    <input type="date" id="dob" name="dob" aria-label="Date of birth" required>
                </div>
                
                <div class="input-group">
                    <label for="asOnDate">📆 Calculate as on (Optional)</label>
                    <input type="date" id="asOnDate" name="asOnDate" aria-label="Calculate as on date">
                    <small>Leave blank to calculate up to today</small>
                </div>
                
                <button class="calculate-btn" onclick="calculateAge()" aria-label="Calculate age">✨ Calculate Age ✨</button>
                
                <div id="ageResult" class="age-result" style="display: none;"></div>
            </div>
        </div>

        <!-- PRIVACY POLICY PAGE -->
        <div id="privacy-page" class="page-content hidden">
            <div class="info-card">
                <h1>🔒 Privacy Policy</h1>
                <p><strong>Last Updated:</strong> June 2026</p>
                <p>Welcome to Calculator Suite. Your privacy is our top priority. This Privacy Policy explains how we handle your information when you use our website.</p>
                
                <h2>📊 Information We Collect</h2>
                <p><strong>We do NOT collect any personal information.</strong> This website does not collect your name, email address, phone number, or any other personally identifiable information. All calculations are performed locally in your browser and never leave your device.</p>
                
                <h2>🍪 Cookies</h2>
                <p>This website may use essential cookies to improve user experience. Cookies are small files stored on your device. You can disable cookies in your browser settings at any time. We do not use tracking cookies or third-party advertising cookies.</p>
                
                <h2>📢 Third-Party Services</h2>
                <p>Currently, we do not use any third-party services. In the future, we may display non-intrusive advertisements to keep our services free. Any such services would comply with privacy regulations.</p>
                
                <h2>🔐 Data Security</h2>
                <p>Since we don't collect any data, there is no data to secure on our servers. All calculations happen locally on your device, ensuring maximum privacy and security.</p>
                
                <h2>👶 Children's Privacy</h2>
                <p>Our website is safe for users of all ages. We do not knowingly collect any information from children under 13. Parents can rest assured that no personal data is being collected.</p>
                
                <h2>📝 Changes to This Policy</h2>
                <p>We may update this Privacy Policy occasionally. Any changes will be posted on this page with an updated "Last Updated" date. We encourage you to review this policy periodically.</p>
                
                <h2>📧 Contact Us</h2>
                <p>If you have any questions about this Privacy Policy, please contact us through our Contact page.</p>
                
                <p>✅ <strong>Last Updated:</strong> This policy is current as of June 2026.</p>
            </div>
        </div>

        <!-- ABOUT PAGE -->
        <div id="about-page" class="page-content hidden">
            <div class="info-card">
                <h1>ℹ️ About Calculator Suite</h1>
                <p>Welcome to <strong>Calculator Suite</strong> - your trusted destination for free, easy-to-use online calculators. We believe that essential calculation tools should be accessible to everyone, without barriers or hidden costs.</p>
                
                <h2>🚀 Our Mission</h2>
                <p>Our mission is to provide simple, accurate, and accessible calculation tools for everyone, completely free of charge. We're committed to maintaining a privacy-first approach where your data never leaves your device.</p>
                
                <h2>✨ What We Offer</h2>
                <ul>
                    <li><strong>Basic Arithmetic Calculator</strong> - Perform addition, subtraction, multiplication, and division with keyboard support</li>
                    <li><strong>Age Calculator</strong> - Calculate exact age with detailed breakdown including zodiac signs and age groups</li>
                    <li><strong>More tools coming soon</strong> - We're constantly improving and adding new features</li>
                </ul>
                
                <h2>💡 Why Choose Calculator Suite?</h2>
                <ul>
                    <li><strong>100% Free</strong> - No hidden charges, no premium tiers, no paid features</li>
                    <li><strong>No Registration Required</strong> - Use instantly without creating an account</li>
                    <li><strong>Privacy Focused</strong> - Zero data collection, all calculations are local to your browser</li>
                    <li><strong>Mobile Responsive</strong> - Works perfectly on all devices and screen sizes</li>
                    <li><strong>Keyboard Support</strong> - Faster calculations with keyboard shortcuts</li>
                </ul>
                
                <h2>🛠️ Technology</h2>
                <p>Our calculators are built with modern web technologies including HTML5, CSS3, and pure JavaScript. No external libraries or frameworks are used, ensuring fast load times and complete transparency. All calculations are performed locally in your browser, providing instant results without any server delays.</p>
                
                <h2>📈 Future Plans</h2>
                <p>We're continuously working to enhance Calculator Suite. Future updates may include additional tools while maintaining our commitment to privacy, speed, and simplicity. Have suggestions? Contact us through our Contact page.</p>
                
                <h2>❤️ Support Our Work</h2>
                <p>If you find our tools helpful, please share Calculator Suite with others. For feedback or suggestions, reach out through our Contact page. Your support helps us keep these tools free for everyone.</p>
            </div>
        </div>

        <!-- CONTACT PAGE -->
        <div id="contact-page" class="page-content hidden">
            <div class="info-card">
                <h1>📧 Contact Us</h1>
                <p>Have questions, feedback, or suggestions? We'd love to hear from you! Your input helps us improve Calculator Suite for everyone.</p>
                
                <div class="contact-box">
                    <h2>📨 Email Us</h2>
                    <div class="email-display">
                        <span class="email-address" id="emailAddress">asbusinessprofile@gmail.com</span>
                        <button class="copy-btn" onclick="copyEmail()" aria-label="Copy email address">📋 Copy Email</button>
                    </div>
                </div>
                
                <div class="contact-box">
                    <h2>💬 Response Time</h2>
                    <p>We strive to respond to all inquiries within 24-48 hours on business days. Your patience is appreciated.</p>
                </div>
                
                <div class="contact-box">
                    <h2>📋 What to Include in Your Message</h2>
                    <ul>
                        <li>Your name (optional but helpful)</li>
                        <li>Detailed description of your question or feedback</li>
                        <li>Screenshots (if reporting a technical issue)</li>
                        <li>Browser and device information (for bug reports)</li>
                    </ul>
                </div>
                
                <div class="contact-box">
                    <h2>🌟 Feedback Welcome</h2>
                    <p>We appreciate all feedback! Let us know what calculators you'd like to see added to our suite, or how we can improve existing tools.</p>
                </div>
                
                <div class="contact-box">
                    <h2>🔗 Direct Email Link</h2>
                    <p>Click here to email us directly: 
                        <a href="mailto:asbusinessprofile@gmail.com" style="color: var(--primary-gradient-start); text-decoration: none; font-weight: 600;">
                            asbusinessprofile@gmail.com
                        </a>
                    </p>
                </div>
                
                <p style="text-align: center; margin-top: 20px;">Thank you for using Calculator Suite! 🙏</p>
            </div>
        </div>

        <!-- FOOTER -->
        <footer class="footer">
            <p>© 2026 Calculator Suite. All rights reserved.</p>
            <p>Made with ❤️ for free online tools | All calculations are local and private</p>
            <p><a href="#" onclick="showPage('privacy'); return false;">Privacy Policy</a> | <a href="#" onclick="showPage('about'); return false;">About</a> | <a href="#" onclick="showPage('contact'); return false;">Contact</a></p>
        </footer>
    </div>

    <script>
        // ============ PAGE NAVIGATION ============
        function showPage(page) {
            // Hide all pages
            document.querySelectorAll('.page-content').forEach(el => {
                el.classList.add('hidden');
            });
            
            // Show selected page
            const targetPage = document.getElementById(`${page}-page`);
            if (targetPage) {
                targetPage.classList.remove('hidden');
            }
            
            // Update active button
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('active');
                // Check if button text matches page
                const btnText = btn.textContent.trim().toLowerCase();
                const pageName = page === 'home' ? 'home' : 
                                page === 'calculator' ? 'calculator' :
                                page === 'age' ? 'age calculator' :
                                page === 'privacy' ? 'privacy' :
                                page === 'about' ? 'about' : 'contact';
                if (btnText.includes(pageName) || (page === 'home' && btnText === '🏠 home')) {
                    btn.classList.add('active');
                }
            });
            
            // Reset age calculator display when switching to age page
            if (page === 'age') {
                const ageResult = document.getElementById('ageResult');
                if (ageResult) ageResult.style.display = 'none';
            }
            
            // Scroll to top
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // ============ COPY EMAIL FUNCTION ============
        function copyEmail() {
            const email = "asbusinessprofile@gmail.com";
            navigator.clipboard.writeText(email).then(() => {
                const btn = event.target;
                const originalText = btn.textContent;
                btn.textContent = "✅ Copied!";
                btn.style.background = "#51cf66";
                setTimeout(() => {
                    btn.textContent = originalText;
                    btn.style.background = "linear-gradient(135deg, #667eea, #764ba2)";
                }, 2000);
            }).catch(() => {
                alert("Please manually copy the email: " + email);
            });
        }

        // ============ TOGGLE FAQ ============
        function toggleFAQ(faqId) {
            const faqItem = document.getElementById(faqId);
            if (faqItem) {
                faqItem.classList.toggle('active');
            }
        }

        // ============ MAIN CALCULATOR ============
        const display = document.getElementById('display');
        const previousOperand = document.getElementById('previousOperand');
        
        let currentInput = '0';
        let previousInput = '';
        let operation = null;
        let shouldResetDisplay = false;

        function updateDisplay() {
            display.value = currentInput;
            if (operation && previousInput) {
                const symbols = {'+': '+', '-': '−', '*': '×', '/': '÷'};
                previousOperand.textContent = `${previousInput} ${symbols[operation]}`;
            } else if (previousInput) {
                previousOperand.textContent = previousInput;
            } else {
                previousOperand.textContent = '';
            }
        }

        function appendNumber(number) {
            if (shouldResetDisplay) {
                currentInput = '';
                shouldResetDisplay = false;
            }
            
            if (number === '.') {
                if (currentInput.includes('.')) return;
                if (currentInput === '') currentInput = '0.';
                else currentInput += '.';
            } else {
                if (currentInput === '0' && number !== '.') currentInput = number;
                else currentInput += number;
            }
            updateDisplay();
        }

        function appendOperator(op) {
            if (operation !== null && !shouldResetDisplay) calculateResult();
            if (currentInput === '' || currentInput === 'Error') return;
            previousInput = currentInput;
            operation = op;
            shouldResetDisplay = true;
            updateDisplay();
        }

        function calculateResult() {
            if (operation === null || shouldResetDisplay) return;
            if (previousInput === '') return;
            
            let result;
            const prev = parseFloat(previousInput);
            const current = parseFloat(currentInput);
            
            if (isNaN(prev) || isNaN(current)) return;
            
            switch (operation) {
                case '+': result = prev + current; break;
                case '-': result = prev - current; break;
                case '*': result = prev * current; break;
                case '/': 
                    if (current === 0) {
                        showCalculatorError("Cannot divide by zero!");
                        return;
                    }
                    result = prev / current; 
                    break;
                default: return;
            }
            
            // Format result to avoid floating point issues
            currentInput = Number.isInteger(result) ? result.toString() : parseFloat(result.toFixed(10)).toString();
            previousInput = '';
            operation = null;
            shouldResetDisplay = true;
            
            // Add animation
            display.classList.add('result-pulse');
            setTimeout(() => display.classList.remove('result-pulse'), 300);
            updateDisplay();
        }

        function clearAll() {
            currentInput = '0';
            previousInput = '';
            operation = null;
            shouldResetDisplay = false;
            updateDisplay();
        }

        function deleteLast() {
            if (shouldResetDisplay) return;
            if (currentInput === 'Error') {
                clearAll();
                return;
            }
            currentInput = currentInput.length > 1 ? currentInput.slice(0, -1) : '0';
            updateDisplay();
        }

        function showCalculatorError(message) {
            currentInput = 'Error';
            updateDisplay();
            setTimeout(clearAll, 1500);
        }

        // ============ AGE CALCULATOR ============
        function calculateAge() {
            const dobInput = document.getElementById('dob').value;
            let asOnInput = document.getElementById('asOnDate').value;
            
            if (!dobInput) {
                showAgeError("Please select your date of birth!");
                return;
            }
            
            const dob = new Date(dobInput);
            const asOn = asOnInput ? new Date(asOnInput) : new Date();
            
            if (isNaN(dob.getTime())) {
                showAgeError("Invalid date of birth! Please select a valid date.");
                return;
            }
            
            if (isNaN(asOn.getTime())) {
                showAgeError("Invalid 'as on' date! Please select a valid date.");
                return;
            }
            
            if (dob > asOn) {
                showAgeError("Date of birth cannot be after the selected date!");
                return;
            }
            
            if (dob.getFullYear() < 1900) {
                showAgeError("Please enter a valid date of birth (year should be after 1900).");
                return;
            }
            
            // Calculate age components
            let years = asOn.getFullYear() - dob.getFullYear();
            let months = asOn.getMonth() - dob.getMonth();
            let days = asOn.getDate() - dob.getDate();
            
            if (days < 0) {
                months--;
                const lastMonth = new Date(asOn.getFullYear(), asOn.getMonth(), 0);
                days += lastMonth.getDate();
            }
            
            if (months < 0) {
                years--;
                months += 12;
            }
            
            // Additional calculations
            const totalDays = Math.floor((asOn - dob) / (1000 * 60 * 60 * 24));
            const totalMonths = years * 12 + months;
            const totalWeeks = Math.floor(totalDays / 7);
            const totalHours = totalDays * 24;
            const totalMinutes = totalHours * 60;
            const totalSeconds = totalMinutes * 60;
            
            // Next birthday calculation
            let nextBirthday = new Date(asOn.getFullYear(), dob.getMonth(), dob.getDate());
            if (nextBirthday < asOn) {
                nextBirthday.setFullYear(nextBirthday.getFullYear() + 1);
            }
            const daysToBirthday = Math.ceil((nextBirthday - asOn) / (1000 * 60 * 60 * 24));
            
            // Age group
            let ageGroup = years < 1 ? "👶 Infant" : 
                          years < 3 ? "👧 Toddler" :
                          years < 12 ? "🧒 Child" :
                          years < 18 ? "🧑 Teenager" :
                          years < 60 ? "👨 Adult" : "👴 Senior";
            
            // Zodiac sign
            const zodiac = getZodiacSign(dob);
            
            // Format date
            const formatDate = (date) => {
                return date.toLocaleDateString('en-US', { 
                    year: 'numeric', 
                    month: 'long', 
                    day: 'numeric' 
                });
            };
            
            const resultHTML = `
                <h3>🎉 Age Calculation Results</h3>
                <div class="result-item">
                    <span class="result-label">📅 Date of Birth:</span>
                    <span class="result-value">${formatDate(dob)}</span>
                </div>
                <div class="result-item">
                    <span class="result-label">📆 As on Date:</span>
                    <span class="result-value">${formatDate(asOn)}</span>
                </div>
                <div class="result-item">
                    <span class="result-label">✨ Exact Age:</span>
                    <span class="result-value"><strong>${years} years, ${months} months, ${days} days</strong></span>
                </div>
                <div class="result-item">
                    <span class="result-label">🎂 Age Group:</span>
                    <span class="result-value">${ageGroup}</span>
                </div>
                <div class="result-item">
                    <span class="result-label">⭐ Zodiac Sign:</span>
                    <span class="result-value">${zodiac}</span>
                </div>
                <div class="result-item">
                    <span class="result-label">📊 Total Months:</span>
                    <span class="result-value">${totalMonths} months</span>
                </div>
                <div class="result-item">
                    <span class="result-label">📆 Total Weeks:</span>
                    <span class="result-value">${totalWeeks} weeks</span>
                </div>
                <div class="result-item">
                    <span class="result-label">📈 Total Days:</span>
                    <span class="result-value">${totalDays.toLocaleString()} days</span>
                </div>
                <div class="result-item">
                    <span class="result-label">⏰ Total Hours:</span>
                    <span class="result-value">${totalHours.toLocaleString()} hours</span>
                </div>
                <div class="result-item">
                    <span class="result-label">⏱️ Total Minutes:</span>
                    <span class="result-value">${totalMinutes.toLocaleString()} minutes</span>
                </div>
                <div class="result-item">
                    <span class="result-label">⚡ Total Seconds:</span>
                    <span class="result-value">${totalSeconds.toLocaleString()} seconds</span>
                </div>
                <div class="result-item">
                    <span class="result-label">🎂 Days until next birthday:</span>
                    <span class="result-value">${daysToBirthday} days</span>
                </div>
            `;
            
            const ageResult = document.getElementById('ageResult');
            ageResult.innerHTML = resultHTML;
            ageResult.style.display = 'block';
            ageResult.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        }
        
        function getZodiacSign(dob) {
            const month = dob.getMonth() + 1;
            const day = dob.getDate();
            
            if ((month === 1 && day >= 20) || (month === 2 && day <= 18)) return "♒ Aquarius";
            if ((month === 2 && day >= 19) || (month === 3 && day <= 20)) return "♓ Pisces";
            if ((month === 3 && day >= 21) || (month === 4 && day <= 19)) return "♈ Aries";
            if ((month === 4 && day >= 20) || (month === 5 && day <= 20)) return "♉ Taurus";
            if ((month === 5 && day >= 21) || (month === 6 && day <= 20)) return "♊ Gemini";
            if ((month === 6 && day >= 21) || (month === 7 && day <= 22)) return "♋ Cancer";
            if ((month === 7 && day >= 23) || (month === 8 && day <= 22)) return "♌ Leo";
            if ((month === 8 && day >= 23) || (month === 9 && day <= 22)) return "♍ Virgo";
            if ((month === 9 && day >= 23) || (month === 10 && day <= 22)) return "♎ Libra";
            if ((month === 10 && day >= 23) || (month === 11 && day <= 21)) return "♏ Scorpio";
            if ((month === 11 && day >= 22) || (month === 12 && day <= 21)) return "♐ Sagittarius";
            return "♑ Capricorn";
        }
        
        function showAgeError(message) {
            const ageResult = document.getElementById('ageResult');
            ageResult.innerHTML = `<div class="error-message">❌ ${message}</div>`;
            ageResult.style.display = 'block';
            setTimeout(() => {
                ageResult.style.display = 'none';
            }, 3000);
        }

        // ============ KEYBOARD SUPPORT ============
        document.addEventListener('keydown', (event) => {
            const calculatorPage = document.getElementById('calculator-page');
            if (calculatorPage.classList.contains('hidden')) return;
            
            const key = event.key;
            
            if (/[0-9]/.test(key)) {
                event.preventDefault();
                appendNumber(key);
            }
            if (key === '.') {
                event.preventDefault();
                appendNumber('.');
            }
            if (key === '+') {
                event.preventDefault();
                appendOperator('+');
            }
            if (key === '-') {
                event.preventDefault();
                appendOperator('-');
            }
            if (key === '*') {
                event.preventDefault();
                appendOperator('*');
            }
            if (key === '/') {
                event.preventDefault();
                appendOperator('/');
            }
            if (key === 'Enter' || key === '=') {
                event.preventDefault();
                calculateResult();
            }
            if (key === 'Escape') {
                event.preventDefault();
                clearAll();
            }
            if (key === 'Backspace') {
                event.preventDefault();
                deleteLast();
            }
        });

        // ============ INITIALIZATION ============
        function initialize() {
            updateDisplay();
            
            // Set default date for age calculator (25 years ago)
            const defaultDate = new Date();
            defaultDate.setFullYear(defaultDate.getFullYear() - 25);
            const defaultDateStr = defaultDate.toISOString().split('T')[0];
            const dobInput = document.getElementById('dob');
            if (dobInput) dobInput.value = defaultDateStr;
            
            // Set max date for DOB as today
            const today = new Date().toISOString().split('T')[0];
            if (dobInput) dobInput.max = today;
            const asOnInput = document.getElementById('asOnDate');
            if (asOnInput) asOnInput.max = today;
        }
        
        initialize();
    </script>
</body>
</html>
