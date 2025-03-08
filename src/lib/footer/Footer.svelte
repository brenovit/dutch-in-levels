<script lang="ts">
    const currentYear = new Date().getFullYear();
  </script>
  
  <style>
    footer {
      background: linear-gradient(to right, #ff6700, #002f6c); /* Dutch Orange to Blue */
      color: white;
      padding: 20px 0;
      text-align: center;
    }
    
    .footer-container {
      max-width: 800px;
      margin: auto;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
  
    .footer-links {
      display: flex;
      gap: 15px;
      margin-top: 10px;
    }
  
    .footer-links a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }
  
    .footer-links a:hover {
      text-decoration: underline;
    }
  
    .social-icons {
      margin-top: 10px;
      display: flex;
      gap: 15px;
    }
  
    .social-icons a {
      color: white;
      font-size: 20px;
      transition: transform 0.2s;
    }
  
    .social-icons a:hover {
      transform: scale(1.2);
    }
  </style>
  
  <footer>
    <div class="footer-container">
      <p>&copy; {currentYear} Nieuws in Niveaus - Alle rechten voorbehouden.</p>
      
      <div class="footer-links">
        <a href="/">Home</a>
        <a href="/about">Over Ons</a>
      </div>
  
      <div class="social-icons">
        <a href="https://twitter.com" target="_blank" aria-label="Twitter">🐦</a>
        <a href="https://facebook.com" target="_blank" aria-label="Facebook">📘</a>
        <a href="https://instagram.com" target="_blank" aria-label="Instagram">📸</a>
      </div>
    </div>
  </footer>
  