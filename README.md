<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NexusXpert - AI Solutions</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Roboto', sans-serif;
      background: #121212;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      text-align: center;
      flex-direction: column;
      background: radial-gradient(circle, rgba(18,18,18,1) 0%, rgba(0,0,0,1) 100%);
      overflow: hidden;
      position: relative;
    }
    header {
      background-color: #1e1e1e;
      padding: 40px 20px;
      width: 100%;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.5);
      position: relative;
      z-index: 2;
    }
    header h1 {
      font-size: 40px;
      color: #00bcd4;
      margin-bottom: 10px;
      text-transform: uppercase;
      letter-spacing: 3px;
      text-shadow: 0 0 20px rgba(0, 188, 212, 1), 0 0 50px rgba(0, 188, 212, 0.5);
    }
    header p {
      font-size: 20px;
      font-style: italic;
      color: #aaa;
    }
    .container {
      width: 90%;
      margin-top: 40px;
      position: relative;
      z-index: 3;
    }
    section {
      padding: 40px 0;
    }
    h2 {
      font-size: 40px;
      color: #00bcd4;
      margin-bottom: 20px;
      letter-spacing: 2px;
      text-shadow: 0 0 20px rgba(0, 188, 212, 0.7);
    }
    .plan-scrollable-container {
      max-height: 500px;
      overflow-y: auto;
      display: flex;
      justify-content: center;
      gap: 30px;
      flex-wrap: wrap;
      margin-top: 20px;
      padding: 0 20px;
      margin-bottom: 40px;
    }
    .plan-card {
      background-color: #1d1d1d;
      border-radius: 15px;
      box-shadow: 0 15px 30px rgba(0, 188, 212, 0.3);
      padding: 20px;
      transition: transform 0.3s ease, background-color 0.5s ease;
      text-align: center;
      margin: 20px;
      max-width: 300px;
      display: inline-block;
      vertical-align: top;
      border: 2px solid #00bcd4;
      position: relative;
      z-index: 1;
      cursor: pointer;
      overflow: hidden;
      font-size: 14px;
    }
    .plan-card:hover {
      transform: translateY(-10px) scale(1.05);
      background-color: #121212;
      box-shadow: 0 20px 40px rgba(0, 188, 212, 0.7);
    }
    .plan-card h3 {
      font-size: 28px;
      margin-bottom: 15px;
      color: #00bcd4;
      text-transform: uppercase;
    }
    .plan-card p {
      font-size: 14px;
      color: #aaa;
      margin-bottom: 15px;
    }
    .plan-card .price {
      font-size: 24px;
      font-weight: bold;
      color: #fff;
      margin-bottom: 15px;
    }
    .plan-card button {
      background-color: #00bcd4;
      color: #fff;
      padding: 15px 30px;
      font-size: 16px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: background-color 0.3s ease, transform 0.2s ease;
      width: 100%;
      position: relative;
      z-index: 2;
    }
    .plan-card button:hover {
      background-color: #00acc1;
      transform: translateY(-5px);
    }
    .beta-warning {
      background-color: #f8d7da;
      color: #721c24;
      padding: 10px;
      font-size: 16px;
      margin: 20px 0;
    }
    footer {
      background-color: #1e1e1e;
      color: #aaa;
      padding: 20px;
      width: 100%;
      position: absolute;
      bottom: 0;
    }
    .contact-section {
      padding: 40px 0;
      background: #333;
    }
    .contact-section a {
      text-decoration: none;
      color: #00bcd4;
      font-weight: bold;
      text-transform: uppercase;
    }
    .contact-section a:hover {
      color: #00acc1;
    }
    .plan-comparison table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 20px;
    }
    .plan-comparison th, .plan-comparison td {
      padding: 12px;
      text-align: left;
      border: 1px solid #333;
      color: #bbb;
    }
    .plan-comparison th {
      background-color: #1e1e1e;
      color: #00bcd4;
    }
    .plan-comparison tr:nth-child(even) {
      background-color: #222;
    }
    .interactive-buttons {
      display: flex;
      justify-content: center;
      gap: 30px;
      margin-top: 30px;
    }
    .interactive-buttons button {
      background-color: #00bcd4;
      color: white;
      padding: 15px 30px;
      font-size: 18px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: background-color 0.3s ease, transform 0.2s ease;
      width: 200px;
    }
    .interactive-buttons button:hover {
      background-color: #00acc1;
      transform: translateY(-5px);
    }
    .particle-background {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      pointer-events: none;
      z-index: 0;
      opacity: 0.2;
    }
  </style>
  <script>
    function sendWhatsAppMessage(plan) {
      let message = '';
      if (plan === 'basic') {
        message = 'I am interested in the Basic Plan ($100/month). Please share more details.';
      } else if (plan === 'standard') {
        message = 'I am interested in the Standard Plan ($500/month). Please share more details.';
      } else if (plan === 'premium') {
        message = 'I am interested in the Premium Plan ($1000/month). Please share more details.';
      }
      const phone = '+918009773835';  // Replace with your WhatsApp number
      const url = `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;
      window.open(url, '_blank');
    }
  </script>
</head>
<body>

  <header>
    <h1>NexusXpert</h1>
    <p><em>Empowering the Future with AI and Technology</em></p>
  </header>

  <div class="container">
    <section>
      <h2>About NexusXpert</h2>
      <p>
        At <strong>NexusXpert</strong>, we specialize in providing cutting-edge AI solutions that transform businesses and enhance user experiences. 
        Our expertise in AI-powered software development enables us to create smarter apps, efficient workflows, and innovative solutions.
      </p>
    </section>
    <div class="beta-warning">
      <strong>Note:</strong> We are currently in the beta phase. Some features might not be fully functional.
    </div>
    <section>
      <h2>Our Subscription Plans</h2>
      <div class="plan-scrollable-container">
        <div class="plan-card">
          <h3>Basic Plan</h3>
          <p>Price: $100/month</p>
          <p>For clients who need essential maintenance and stability. Ideal for small businesses and startups.</p>
          <p class="price">$100</p>
          <p>Features:</p>
          <ul>
            <li>Server Maintenance</li>
            <li>Minor Bug Fixes</li>
            <li>Basic Support</li>
          </ul>
          <button onclick="sendWhatsAppMessage('basic')">Subscribe Now</button>
        </div>
        <div class="plan-card">
          <h3>Standard Plan</h3>
          <p>Price: $500/month</p>
          <p>For businesses looking for more support and features. Ideal for medium-sized companies.</p>
          <p class="price">$500</p>
          <p>Features:</p>
          <ul>
            <li>Server Maintenance</li>
            <li>Minor Bug Fixes</li>
            <li>Software Updates</li>
          </ul>
          <button onclick="sendWhatsAppMessage('standard')">Subscribe Now</button>
        </div>
        <div class="plan-card">
          <h3>Premium Plan</h3>
          <p>Price: $1000/month</p>
          <p>For clients who require premium features and priority support. Ideal for large-scale enterprises.</p>
          <p class="price">$1000</p>
          <p>Features:</p>
          <ul>
            <li>Server Maintenance</li>
            <li>Minor Bug Fixes</li>
            <li>Software Updates</li>
            <li>Priority Support</li>
            <li>Advanced Feature Development</li>
            <li>Custom Solutions</li>
          </ul>
          <button onclick="sendWhatsAppMessage('premium')">Subscribe Now</button>
        </div>
      </div>
      <div class="plan-comparison">
        <h2>Plan Comparison</h2>
        <table>
          <thead>
            <tr>
              <th>Feature</th>
              <th>Basic Plan</th>
              <th>Standard Plan</th>
              <th>Premium Plan</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Server Maintenance</td>
              <td>✔</td>
              <td>✔</td>
              <td>✔</td>
            </tr>
            <tr>
              <td>Minor Bug Fixes</td>
              <td>✔</td>
              <td>✔</td>
              <td>✔</td>
            </tr>
            <tr>
              <td>Software Updates</td>
              <td>❌</td>
              <td>✔</td>
              <td>✔</td>
            </tr>
            <tr>
              <td>Priority Support</td>
              <td>❌</td>
              <td>❌</td>
              <td>✔</td>
            </tr>
          </tbody>
        </table>
      </div>
      <div class="interactive-buttons">
        <button onclick="sendWhatsAppMessage('basic')">Learn More about Basic Plan</button>
        <button onclick="sendWhatsAppMessage('standard')">Learn More about Standard Plan</button>
        <button onclick="sendWhatsAppMessage('premium')">Learn More about Premium Plan</button>
      </div>
    </section>
  </div>
  <footer>
    <p>&copy; 2024 NexusXpert. All rights reserved.</p>
  </footer>
  <!-- Particle Background -->
  <div class="particle-background"></div>
</body>
</html>


