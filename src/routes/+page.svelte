<script lang="ts">
  import { onMount } from 'svelte';
  import newsData from '../news.json';

  let news = newsData;
  let level = 1;
  let selectedAnswers:any = {};

  function checkAnswer(articleIndex: number, questionIndex: number, choice: any) {
    const correctAnswer = news[articleIndex].questions[questionIndex].answer;
    selectedAnswers[`${articleIndex}-${questionIndex}`] = {
      choice,
      correct: choice === correctAnswer
    };
  }
</script>

<style>
  .news-container { max-width: 800px; margin: auto; padding: 20px; }
  .news-card { border: 1px solid #ddd; border-radius: 10px; padding: 15px; margin-bottom: 15px; }
  .button { padding: 10px 15px; margin-right: 10px; cursor: pointer; }
  .highlight { font-weight: bold; color: blue; }
  .choice-button { margin-top: 5px; padding: 5px 10px; cursor: pointer; }
  .correct { background-color: #4CAF50; color: white; }
  .incorrect { background-color: #F44336; color: white; }
</style>

<div class="news-container">
  <h1 class="text-3xl font-bold mb-4">Nieuws in Niveaus</h1>
  <div class="flex gap-4 mb-4">
    <button class="button" on:click={() => level = 1}>Niveau 1</button>
    <button class="button" on:click={() => level = 2}>Niveau 2</button>
    <button class="button" on:click={() => level = 3}>Niveau 3</button>
  </div>
  
  {#each news as article, articleIndex}
    <div class="news-card">
      <h2 class="text-xl font-semibold">{article.title}</h2>
      <p class="mt-2">{article[`level${level}`]}</p>
      <p class="highlight">Belangrijke Woorden: {article.highlights.join(', ')}</p>

      <h3 class="mt-3 font-semibold">Begrijpingsvragen:</h3>
      <ul>
        {#each article.questions as question, questionIndex}
          <li class="mt-2">
            <p>{question.question}</p>
            {#each question.choices as choice}
              <button 
                class="choice-button"
                class:correct={selectedAnswers[`${articleIndex}-${questionIndex}`]?.choice === choice && selectedAnswers[`${articleIndex}-${questionIndex}`]?.correct}
                class:incorrect={selectedAnswers[`${articleIndex}-${questionIndex}`]?.choice === choice && !selectedAnswers[`${articleIndex}-${questionIndex}`]?.correct}
                on:click={() => checkAnswer(articleIndex, questionIndex, choice)}
              >
                {choice}
              </button>
            {/each}
          </li>
        {/each}
      </ul>
    </div>
  {/each}
</div>