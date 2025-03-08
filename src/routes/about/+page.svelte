<script lang="ts">
	import { onMount } from 'svelte';
  </script>
  
  <div class="about-container">
	<h1>Over Nieuws in Niveaus</h1>
  
	<p>
	  <span class="highlight">Nieuws in Niveaus</span> is een platform dat nieuwsartikelen in drie verschillende niveaus aanbiedt.
	  Het doel is om taalstudenten te helpen hun <span class="highlight">Nederlands</span> te verbeteren door toegang te geven tot actueel nieuws in
	  begrijpelijke taal.
	</p>
  
	<h2>Hoe werkt het?</h2>
	<p>
	  Elk nieuwsartikel wordt geschreven in <span class="highlight">drie niveaus</span>:
	</p>
	<ul>
	  <li><b>Niveau 1</b> - Eenvoudige en korte zinnen voor beginners.</li>
	  <li><b>Niveau 2</b> - Iets uitgebreidere zinnen voor intermediaire studenten.</li>
	  <li><b>Niveau 3</b> - Volledige, natuurlijke tekst voor gevorderden.</li>
	</ul>
  
	<h2>Waarom Nieuws in Niveaus?</h2>
	<p>
	  - Begrijpelijk Nederlands voor alle niveaus 🎯<br>
	  - Actueel nieuws met woordenschat-uitleg 📰<br>
	  - Interactieve vragen om begrip te testen 📚<br>
	</p>
  
	<div class="contribute">
	  <h2>Wil je bijdragen?</h2>
	  <p>
		Dit project is open-source! Help mee op
		<a href="https://github.com/your-github-repo" target="_blank">GitHub</a> en verbeter samen met ons de website. 💡🚀
	  </p>
	</div>
  
	<div class="linkedin-link">
	  <a href="https://www.linkedin.com/in/breno-nunes/" target="_blank">
		🔗 Bekijk het LinkedIn-profiel van de maker: Breno Nunes
	  </a>
	</div>
  
	<div class="credits">
	  <h2>Speciale dank aan:</h2>
	  <p>
		Dit project werd gebouwd met de hulp van <span class="highlight">ChatGPT</span>, een AI-assistent voor softwareontwikkeling. 🤖  
		Bedankt voor de ondersteuning en code-optimalisatie!
	  </p>
	</div>
  </div>
  
  <style>
	.about-container {
	  max-width: 900px;
	  margin: auto;
	  padding: 40px;
	  background: white;
	  border-radius: 12px;
	  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
	}
  
	h1 {
	  text-align: center;
	  font-size: 2.5rem;
	  color: #ff6700;
	}
  
	p {
	  font-size: 1.1rem;
	  line-height: 1.6;
	  color: #333;
	  text-align: justify;
	}
  
	.highlight {
	  color: #ffffff;
	  font-weight: bold;
	}
  
	.contribute, .credits {
	  margin-top: 30px;
	  padding: 15px;
	  background: #002f6c;
	  color: white; /* Ensure white text for readability */
	  text-align: center;
	  border-radius: 8px;
	  font-size: 1.2rem;
	}

	.contribute p, .credits p {
		color: white; /* Ensure white text for readability */
		
	  text-decoration: none;
	}
  
	.contribute a {
	  color: #ffcc00;
	  font-weight: bold;
	  text-decoration: none;
	}
  
	.contribute a:hover {
	  text-decoration: underline;
	}
  
	.linkedin-link {
	  text-align: center;
	  margin-top: 20px;
	}
  
	.linkedin-link a {
	  display: inline-flex;
	  align-items: center;
	  gap: 10px;
	  background: #0077b5;
	  color: white;
	  padding: 12px 24px;
	  border-radius: 6px;
	  font-weight: bold;
	  font-size: 1.2rem;
	  text-decoration: none;
	  transition: background 0.3s;
	}
  
	.linkedin-link a:hover {
	  background: #005582;
	}
  </style>