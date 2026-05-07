<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>QuickLoan App</title>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family: Arial, sans-serif;
    }

    body{
      background:#f4f7fb;
      color:#333;
    }

    header{
      background:#0a4cff;
      color:white;
      padding:20px;
      text-align:center;
    }

    .hero{
      padding:60px 20px;
      text-align:center;
    }

    .hero h1{
      font-size:40px;
      margin-bottom:15px;
    }

    .hero p{
      font-size:18px;
      margin-bottom:25px;
      color:#555;
    }

    .btn{
      background:#0a4cff;
      color:white;
      padding:12px 25px;
      border:none;
      border-radius:5px;
      cursor:pointer;
      font-size:16px;
    }

    .loan-form{
      max-width:400px;
      margin:40px auto;
      background:white;
      padding:25px;
      border-radius:10px;
      box-shadow:0 0 10px rgba(0,0,0,0.1);
    }

    .loan-form h2{
      margin-bottom:20px;
      text-align:center;
    }

    .loan-form input{
      width:100%;
      padding:12px;
      margin-bottom:15px;
      border:1px solid #ccc;
      border-radius:5px;
    }

    .loan-form button{
      width:100%;
    }

    footer{
      text-align:center;
      padding:20px;
      background:#111;
      color:white;
      margin-top:40px;
    }
  </style>
</head>

<body>

  <header>
    <h2>QuickLoan</h2>
  </header>

  <section class="hero">
    <h1>Get Instant Loans Fast</h1>
    <p>Apply for quick personal loans online with low interest rates.</p>
    <button class="btn">Apply Now</button>
  </section>

  <section class="loan-form">
    <h2>Loan Application</h2>

    <form onsubmit="submitLoan(event)">
      <input type="text" placeholder="Full Name" required />
      <input type="email" placeholder="Email Address" required />
      <input type="number" placeholder="Loan Amount" required />
      <input type="tel" placeholder="Phone Number" required />

      <button class="btn" type="submit">
        Submit Application
      </button>
    </form>
  </section>

  <footer>
    <p>© 2026 QuickLoan. All rights reserved.</p>
  </footer>

  <script>
    function submitLoan(event){
      event.preventDefault();
      alert("Loan application submitted successfully!");
    }
  </script>

</body>
</html>
