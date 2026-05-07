<DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>QuickFund - Personal & Business Loans</title>

  <!-- Tailwind -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css">

  <!-- GSAP -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>

  <!-- Confetti -->
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

  <style>
    body { font-family: 'Inter', system-ui, sans-serif; }

    .hero-bg {
      background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)),
                  url('https://source.unsplash.com/random/1600x900/?finance') center/cover;
    }

    /* 3D card */
    .card-3d {
      transform-style: preserve-3d;
      transition: transform 0.2s ease-out;
    }
  </style>
</head>

<body class="bg-gray-50">

  <!-- Navbar -->
  <nav class="bg-white shadow-md sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
      <h1 class="text-3xl font-bold text-blue-600">QuickFund</h1>
      <div class="space-x-8 text-gray-700 font-medium">
        <a href="#home" class="hover:text-blue-600">Home</a>
        <a href="#loans" class="hover:text-blue-600">Loans</a>
        <a href="#apply" class="hover:text-blue-600">Apply Now</a>
        <a href="#faq" class="hover:text-blue-600">FAQ</a>
      </div>
      <button onclick="document.getElementById('apply-section').scrollIntoView({ behavior: 'smooth' })"
              class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-xl font-semibold">
        Apply Now
      </button>
    </div>
  </nav>

  <!-- Hero -->
  <section id="home" class="hero-bg text-white py-32">
    <div class="max-w-7xl mx-auto px-6 text-center">
      <h2 class="text-5xl md:text-6xl font-bold mb-6">Get the money you need,<br>when you need it.</h2>
      <p class="text-xl mb-10 max-w-2xl mx-auto">Fast, secure, and transparent personal & business loans up to $100,000. Approval in minutes.</p>
      <button onclick="document.getElementById('apply-section').scrollIntoView({ behavior: 'smooth' })"
              class="bg-blue-600 hover:bg-blue-700 text-white text-xl px-10 py-5 rounded-2xl font-semibold transition">
        Start Your Application →
      </button>
      <p class="mt-8 text-sm">No hidden fees • No impact on credit score for pre-qualification</p>
    </div>
  </section>

  <!-- Loan Types -->
  <section id="loans" class="py-20 bg-white">
    <div class="max-w-7xl mx-auto px-6">
      <h3 class="text-4xl font-bold text-center mb-12">Choose Your Loan Type</h3>
      <div class="grid md:grid-cols-3 gap-8">

        <div class="border border-gray-200 rounded-3xl p-8 hover:shadow-xl transition">
          <i class="fa-solid fa-user text-4xl text-blue-600 mb-6"></i>
          <h4 class="text-2xl font-semibold mb-3">Personal Loan</h4>
          <p class="text-4xl font-bold mb-2">$500 - $50,000</p>
          <p class="text-gray-600 mb-6">Flexible repayment terms from 6 to 72 months</p>
          <button class="w-full bg-blue-600 text-white py-4 rounded-2xl font-semibold">Apply Now</button>
        </div>

        <div class="border border-gray-200 rounded-3xl p-8 hover:shadow-xl transition">
          <i class="fa-solid fa-briefcase text-4xl text-emerald-600 mb-6"></i>
          <h4 class="text-2xl font-semibold mb-3">Business Loan</h4>
          <p class="text-4xl font-bold mb-2">$10,000 - $100,000</p>
          <p class="text-gray-600 mb-6">For startups and growing businesses</p>
          <button class="w-full bg-emerald-600 text-white py-4 rounded-2xl font-semibold">Apply Now</button>
        </div>

        <div class="border border-gray-200 rounded-3xl p-8 hover:shadow-xl transition">
          <i class="fa-solid fa-car text-4xl text-purple-600 mb-6"></i>
          <h4 class="text-2xl font-semibold mb-3">Auto Loan</h4>
          <p class="text-4xl font-bold mb-2">Competitive Rates</p>
          <p class="text-gray-600 mb-6">Finance your new or used vehicle</p>
          <button class="w-full bg-purple-600 text-white py-4 rounded-2xl font-semibold">Apply Now</button>
        </div>

      </div>
    </div>
  </section>

  <!-- Application Form -->
  <section id="apply-section" class="py-20 bg-gray-100">
    <div class="max-w-4xl mx-auto px-6">

      <!-- FORM -->
      <form id="loanForm" class="bg-white rounded-3xl shadow-xl p-10 space-y-8">

        <h3 class="text-4xl font-bold text-center mb-4">Loan Application</h3>

        <div class="grid md:grid-cols-2 gap-6">
          <div>
            <label class="block text-sm font-medium mb-2">First Name</label>
            <input type="text" class="w-full border border-gray-300 rounded-2xl px-5 py-4" required>
          </div>
          <div>
            <label class="block text-sm font-medium mb-2">Last Name</label>
            <input type="text" class="w-full border border-gray-300 rounded-2xl px-5 py-4" required>
          </div>
        </div>

        <div class="grid md:grid-cols-2 gap-6">
          <div>
            <label class="block text-sm font-medium mb-2">Email Address</label>
            <input type="email" class="w-full border border-gray-300 rounded-2xl px-5 py-4" required>
          </div>
          <div>
            <label class="block text-sm font-medium mb-2">Phone Number</label>
            <input type="tel" class="w-full border border-gray-300 rounded-2xl px-5 py-4" required>
          </div>
        </div>

        <div>
          <label class="block text-sm font-medium mb-2">Loan Amount Requested</label>
          <div class="flex items-center gap-3">
            <span class="text-3xl font-bold text-gray-400">$</span>
            <input type="number" id="amount" class="w-full border border-gray-300 rounded-2xl px-5 py-4 text-2xl" placeholder="5000" required>
          </div>
        </div>

        <div class="grid md:grid-cols-2 gap-6">
          <div>
            <label class="block text-sm font-medium mb-2">Loan Purpose</label>
            <select class="w-full border border-gray-300 rounded-2xl px-5 py-4">
              <option>Debt Consolidation</option>
              <option>Home Improvement</option>
              <option>Business Expansion</option>
              <option>Vehicle Purchase</option>
              <option>Medical Expenses</option>
              <option>Other</option>
            </select>
          </div>
          <div>
            <label class="block text-sm font-medium mb-2">Annual Income ($)</label>
            <input type="number" class="w-full border border-gray-300 rounded-2xl px-5 py-4" required>
          </div>
        </div>

        <button type="submit"
                class="w-full bg-gradient-to-r from-blue-600 to-blue-700 text-white py-6 text-xl font-semibold rounded-3xl hover:from-blue-700 hover:to-blue-800 transition">
          Submit Application
        </button>

      </form>

      <!-- SUCCESS CARD (HIDDEN INITIALLY) -->
      <div id="successCard" class="hidden card-3d bg-white shadow-2xl rounded-3xl p-10 text-center max-w-lg mx-auto mt-10">
        <h1 class="text-4xl font-bold text-blue-600 mb-4">Application Submitted</h1>
        <p class="text-gray-700 text-lg mb-6">Your application number is:</p>
        <p id="appNumber" class="text-3xl font-bold text-green-600 mb-8"></p>
      </div>

    </div>
  </section>

  <!-- GSAP + LOGIC -->
  <script>
    // FORM SUBMISSION
    document.getElementById('loanForm').addEventListener('submit', function(e) {
      e.preventDefault();

      const amount = document.getElementById('amount').value;
      if (amount < 500 || amount > 100000) {
        alert("Loan amount must be between $500 and $100,000.");
        return;
      }

      // Generate application number
      const appNumber = "QF-" + Math.floor(100000 + Math.random() * 900000);
      document.getElementById("appNumber").textContent = appNumber;

      // Hide form
      gsap.to("#loanForm", {
        opacity: 0,
        scale: 0.8,
        duration: 0.5,
        onComplete: () => {
          document.getElementById("loanForm").classList.add("hidden");

          // Show success card
          const card = document.getElementById("successCard");
          card.classList.remove("hidden");

          // POP-IN animation
          gsap.from(card, {
            opacity: 0,
            scale: 0.5,
            duration: 0.8,
            ease: "back.out(1.7)"
          });

          // Confetti celebration
          launchConfetti();
        }
      });
    });

    // CONFETTI
    function launchConfetti() {
      const duration = 2000;
      const end = Date.now() + duration;

      (function frame() {
        confetti({ particleCount: 6, angle: 60, spread: 55, origin: { x: 0 } });
        confetti({ particleCount: 6, angle: 120, spread: 55, origin: { x: 1 } });

        if (Date.now() < end) requestAnimationFrame(frame);
      })();
    }

    // 3D CARD HOVER
    const card = document.getElementById("successCard");

    card.addEventListener("mousemove", (e) => {
      const rect = card.getBoundingClientRect();
      const x = e.clientX - rect.left - rect.width / 2;
      const y = e.clientY - rect.top - rect.height / 2;

      const rotateX = (y / 20) * -1;
      const rotateY = x / 20;

      card.style.transform = `rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;
    });

    card.addEventListener("mouseleave", () => {
      card.style.transform = "rotateX(0deg) rotateY(0deg)";
    });
  </script>

</body>
</html>
