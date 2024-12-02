<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NexusXpert - AI Solutions</title>
</head>
<body>

  <header>
    <h1>NexusXpert</h1>
    <p><em>Empowering the Future with AI and Technology</em></p>
  </header>

  <div class="container">
    <section>
      <h2>Our AI Plans</h2>
      <div class="plan-scrollable-container">
        <div class="plan-card" onclick="sendWhatsAppMessage('basic')">
          <h3>Basic Plan</h3>
          <p>For individuals looking to use AI in their daily tasks.</p>
          <div class="price">$100/month</div>
          <button>Contact us</button>
        </div>
        <div class="plan-card" onclick="sendWhatsAppMessage('standard')">
          <h3>Standard Plan</h3>
          <p>For small businesses with AI-powered solutions.</p>
          <div class="price">$500/month</div>
          <button>Contact us</button>
        </div>
        <div class="plan-card" onclick="sendWhatsAppMessage('premium')">
          <h3>Premium Plan</h3>
          <p>For large enterprises requiring advanced AI technologies.</p>
          <div class="price">$1000/month</div>
          <button>Contact us</button>
        </div>
      </div>
    </section>
    <section class="beta-warning">
      <p>Our platform is currently in beta. Please be aware that some features may not be available yet.</p>
    </section>
    <section class="contact-section">
      <h2>Contact Us</h2>
      <p>Have questions or want to learn more about our plans? Reach out to us directly on <a href="https://wa.me/918009773835" target="_blank">WhatsApp</a>.</p>
    </section>
    <section class="plan-comparison">
      <h2>Compare Plans</h2>
      <table>
        <thead>
          <tr>
            <th>Feature</th>
            <th>Basic</th>
            <th>Standard</th>
            <th>Premium</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Monthly Cost</td>
            <td>$100</td>
            <td>$500</td>
            <td>$1000</td>
          </tr>
          <tr>
            <td>Support</td>
            <td>Email</td>
            <td>Email & Phone</td>
            <td>Priority Support</td>
          </tr>
          <tr>
            <td>Access to AI Models</td>
            <td>Basic Models</td>
            <td>Standard Models</td>
            <td>Premium Models</td>
          </tr>
        </tbody>
      </table>
    </section>
    <div class="interactive-buttons">
      <button onclick="sendWhatsAppMessage('basic')">Basic Plan</button>
      <button onclick="sendWhatsAppMessage('standard')">Standard Plan</button>
      <button onclick="sendWhatsAppMessage('premium')">Premium Plan</button>
    </div>
  </div>
  <footer>
    <p>&copy; 2024 NexusXpert. All rights reserved.</p>
  </footer>

  <!-- Scroll to Top Button -->
  <button id="scrollToTopBtn" onclick="scrollToTop()">↑</button>

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

    // Scroll to Top Button functionality
    window.onscroll = function() {
      if (document.body.scrollTop > 100 || document.documentElement.scrollTop > 100) {
        document.getElementById("scrollToTopBtn").style.display = "block";
      } else {
        document.getElementById("scrollToTopBtn").style.display = "none";
      }
    };

    function scrollToTop() {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
  </script>

</body>
</html>
