<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>QuickFund - Personal & Business Loans</title>

  <!-- Tailwind -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css">

  <!-- AOS Animations -->
  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">

  <style>
    body { font-family: 'Inter', system-ui, sans-serif; }

    /* Hero background fade-in */
    .hero-bg {
      background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)),
                  url('https://source.unsplash.com/random/1600x900/?finance') center/cover;
      opacity: 0;
      animation: fadeInHero 1.5s ease-out forwards;
    }
    @keyframes fadeInHero {
      to { opacity: 1; }
    }

    /* Floating icons */
    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0); }
    }
    .float {
      animation: float 3s ease-in-out infinite;
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
  <section id="home" class="hero-bg text-white py-32" data-aos="fade-up">
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

        <div class="border border-gray-200 rounded-3xl p-8 hover:shadow-xl transition" data-aos="zoom-in" data-aos-delay="100">
          <i class="fa-solid fa-user text-4xl text-blue-600 mb-6 float"></i>
          <h4 class="text-2xl font-semibold mb-3">Personal Loan</h4>
          <p class="text-4xl font-bold mb-2">$500 - $50,000</p>
          <p class="text-gray-600 mb-6">Flexible repayment terms from 6 to 72 months</p>
          <button class="w-full bg-blue-600 text-white py-4 rounded-2xl font-semibold">Apply Now</button>
        </div>

        <div class="border border-gray-200 rounded-3xl p-8 hover:shadow-xl transition" data-aos="zoom-in" data-aos-delay="200">
          <i class="fa-solid fa-briefcase text-4xl text-emerald-600 mb-6 float"></i>
          <h4 class="text-2xl font-semibold mb-3">Business Loan</h4>
          <p class="text-4xl font-bold mb-2">$10,000 - $100,000</p>
          <p class="text-gray-600 mb-6">For startups and growing businesses</p>
          <button class="w-full bg-emerald-600 text-white py-4 rounded-2xl font-semibold">Apply Now</button>
        </div>

        <div class="border border-gray-200 rounded-3xl p-8 hover:shadow-xl transition" data-aos="zoom-in" data-aos-delay="300">
          <i class="fa-solid fa-car text-4xl text-purple-600 mb-6 float"></i>
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
      <h3 class="text-4xl font-bold text-center mb-4">Loan Application</h3>
      <p class="text-center text-gray-600 mb-10">Takes less than 5 minutes • Secure & encrypted</p>

      <form id="loanForm" class="bg-white rounded-3xl shadow-xl p-10 space-y-8" data-aos="fade-up">

        <div class="grid md:grid-cols-2 gap-6">
          <div>
            <label for="firstName" class="block text-sm font-medium mb-2">First Name</label>
            <input id="firstName" type="text" class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:outline-none focus:border-blue-500" required>
          </div>

          <div>
            <label for="lastName" class="block text-sm font-medium mb-2">Last Name</label>
            <input id="lastName" type="text" class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:outline-none focus:border-blue-500" required>
          </div>
        </div>

        <div class="grid md:grid-cols-2 gap-6">
          <div>
            <label for="email" class="block text-sm font-medium mb-2">Email Address</label>
            <input id="email" type="email" class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:outline-none focus:border-blue-500" required>
          </div>

          <div>
            <label for="phone" class="block text-sm font-medium mb-2">Phone Number</label>
            <input id="phone" type="tel" class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:outline-none focus:border-blue-500" required>
          </div>
        </div>

        <div>
          <label for="amount" class="block text-sm font-medium mb-2">Loan Amount Requested</label>
          <div class="flex items-center gap-3">
            <span class="text-3xl font-bold text-gray-400">$</span>
            <input type="number" id="amount" class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:outline-none focus:border-blue-500 text-2xl" placeholder="5000" required>
          </div>
        </div>

        <div class="grid md:grid-cols-2 gap-6">
          <div>
            <label class="block text-sm font-medium mb-2">Loan Purpose</label>
            <select class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:outline-none focus:border-blue-500">
              <option>Debt Consolidation</option>
              <option>Home Improvement</option>
              <option>Business Expansion</option>
              <option>Vehicle Purchase</option>
              <option>Medical Expenses</option>
              <option>Other</option>
            </select>
          </div>

          <div>
            <label for="income" class="block text-sm font-medium mb-2">Annual Income ($)</label>
            <input id="income" type="number" class="w-full border border-gray-300 rounded-2xl px-5 py-4 focus:outline-none focus:border-blue-500" required>
          </div>
        </div>

        <div class="pt-6">
          <button type="submit"
                  class="w-full bg-gradient-to-r from-blue-600 to-blue-700 text-white py-6 text-xl font-semibold rounded-3xl hover:from-blue-700 hover:to-blue-800 transition">
            Submit Application
          </button>
        </div>

      </form>

      <p class="text-center text-sm text-gray-500 mt-8">
        Your information is protected with bank-level encryption.<br>
        This is a demo website for educational and portfolio purposes only.
      </p>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-gray-900 text-white py-16">
    <div class="max-w-7xl mx-auto px-6 text-center">
      <h2 class="text-3xl font-bold mb-4">QuickFund</h2>
      <p class="text-gray-400">Fast. Transparent. Reliable.</p>
      <p class="text-sm text-gray-500 mt-8">© 2026 QuickFund Demo. This is a fictional website for educational and portfolio purposes.</p>
    </div>
  </footer>

  <!-- Scripts -->
  <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
  <script>
    AOS.init({ duration: 1000, once: true });

    document.getElementById('loanForm').addEventListener('submit', function(e) {
      e.preventDefault();

      const amount = document.getElementById('amount').value;
      if (amount < 500 || amount > 100000) {
        alert("Loan amount must be between $500 and $100,000.");
        return;
      }

      alert("✅ Application submitted successfully!\n\n(This is a demo. In a real app, data would be securely processed.)");
      this.reset();
    });
  </script>

</body>
</html>
