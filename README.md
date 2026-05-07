<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QuickCash Loan - Fast Loans in Nigeria</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
        }
        
        header {
            background: #1e3a8a;
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            margin-left: 2rem;
            font-weight: 500;
        }
        
        .hero {
            background: linear-gradient(rgba(30, 58, 138, 0.9), rgba(30, 58, 138, 0.9)), url('https://picsum.photos/id/1015/2000/800') center/cover;
            color: white;
            text-align: center;
            padding: 120px 20px;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            background: #22c55e;
            color: white;
            padding: 14px 32px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s;
        }
        
        .btn:hover {
            background: #16a34a;
            transform: translateY(-3px);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        .form-section {
            background: white;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            padding: 40px;
            margin: 40px auto;
            max-width: 700px;
        }
        
        h2 {
            text-align: center;
            margin-bottom: 30px;
            color: #1e3a8a;
        }
        
        form {
            display: grid;
            gap: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 6px;
            font-weight: 600;
        }
        
        input, select, textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
        }
        
        .submit-btn {
            background: #1e3a8a;
            color: white;
            border: none;
            padding: 16px;
            font-size: 1.2rem;
            border-radius: 8px;
            cursor: pointer;
            margin-top: 10px;
        }
        
        .telegram-info {
            background: #229ED9;
            color: white;
            padding: 25px;
            border-radius: 12px;
            text-align: center;
            margin: 40px 0;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 60px 0;
        }
        
        .feature-card {
            background: white;
            padding: 30px;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
        }
        
        footer {
            background: #1e3a8a;
            color: white;
            text-align: center;
            padding: 40px 20px;
            margin-top: 60px;
        }
        
        .success-message {
            display: none;
            background: #22c55e;
            color: white;
            padding: 20px;
            border-radius: 8px;
            text-align: center;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">QuickCash</div>
            <div class="nav-links">
                <a href="#">Home</a>
                <a href="#">Loans</a>
                <a href="#">How it Works</a>
                <a href="#">Contact</a>
            </div>
        </nav>
    </header>

    <section class="hero">
        <h1>Get Instant Loans in Minutes</h1>
        <p>Up to ₦5,000,000 with minimal documentation. Fast approval and disbursement to your bank account.</p>
        <a href="#apply" class="btn">Apply Now</a>
    </section>

    <div class="container">
        <section id="apply" class="form-section">
            <h2>Loan Application Form</h2>
            
            <form id="loanForm">
                <div>
                    <label>Full Name</label>
                    <input type="text" id="fullName" required placeholder="John Doe">
                </div>
                
                <div>
                    <label>Phone Number</label>
                    <input type="tel" id="phone" required placeholder="+234 801 234 5678">
                </div>
                
                <div>
                    <label>Email Address</label>
                    <input type="email" id="email" required placeholder="you@example.com">
                </div>
                
                <div>
                    <label>National ID / BVN</label>
                    <input type="text" id="idNumber" required placeholder="Enter your NIN or BVN">
                </div>
                
                <div>
                    <label>Loan Amount (₦)</label>
                    <input type="number" id="amount" required min="10000" max="5000000" placeholder="500000">
                </div>
                
                <div>
                    <label>Loan Duration</label>
                    <select id="duration" required>
                        <option value="">Select duration</option>
                        <option value="1">1 Month</option>
                        <option value="3">3 Months</option>
                        <option value="6" selected>6 Months</option>
                        <option value="12">12 Months</option>
                    </select>
                </div>
                
                <div>
                    <label>Purpose of Loan</label>
                    <textarea id="purpose" rows="3" placeholder="Business expansion, personal use, etc."></textarea>
                </div>
                
                <button type="submit" class="submit-btn">Submit Application</button>
            </form>
            
            <div id="successMessage" class="success-message">
                ✅ Application Submitted Successfully!<br>
                Your Application ID: <strong>QC-2026-</strong><span id="appId"></span><br><br>
                <strong>Track your result via Telegram</strong>
            </div>
        </section>

        <div class="telegram-info">
            <h3>📱 Check Your Loan Status on Telegram</h3>
            <p style="font-size: 1.3rem; margin: 15px 0;">
                <strong>@QuickCashLoanBot</strong>
            </p>
            <p>Send your Application ID to the bot above to get instant updates on approval status and disbursement.</p>
            <a href="https://t.me/QuickCashLoanBot" target="_blank" style="color: white; text-decoration: underline; font-size: 1.1rem;">
                Open Telegram Bot →
            </a>
        </div>

        <div class="features">
            <div class="feature-card">
                <h3>⚡ Instant Approval</h3>
                <p>Get approved in under 15 minutes with just your BVN/NIN and basic details.</p>
            </div>
            <div class="feature-card">
                <h3>💰 Flexible Repayment</h3>
                <p>Choose from 1 to 12 months repayment plans with competitive interest rates.</p>
            </div>
            <div class="feature-card">
                <h3>🔒 Secure &amp; Trusted</h3>
                <p>Bank-level security. Licensed by the Central Bank of Nigeria.</p>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; 2026 QuickCash Loans Nigeria. All Rights Reserved.</p>
        <p>Telegram Support: <strong>@QuickCashLoanBot</strong> | Customer Care: 0800-QUICKCASH</p>
        <p style="margin-top: 10px; font-size: 0.9rem;">
            This is a demo website for illustration purposes only.
        </p>
    </footer>

    <script>
        document.getElementById('loanForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Generate random application ID
            const randomId = Math.floor(10000 + Math.random() * 90000);
            document.getElementById('appId').textContent = randomId;
            
            // Show success message
            document.getElementById('successMessage').style.display = 'block';
            
            // Scroll to success message
            document.getElementById('successMessage').scrollIntoView({ behavior: 'smooth' });
            
            // Reset form after 5 seconds (optional)
            setTimeout(() => {
                this.reset();
                document.getElementById('successMessage').style.display = 'none';
            }, 8000);
        });
        
        // Make phone number nicer on mobile
        document.getElementById('phone').addEventListener('input', function(e) {
            let val = e.target.value.replace(/\D/g, '');
            if (val.length > 11) val = val.substring(0, 11);
            e.target.value = val;
        });
    </script>
</body>
</html>
