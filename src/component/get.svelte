<script>
    import { onMount } from 'svelte';
    function copyToClipboard(text) {
      const el = document.createElement('textarea');
      el.value = text;
      document.body.appendChild(el);
      el.select();
      document.execCommand('copy');
      document.body.removeChild(el);
    }
    let users = [];
  
    onMount(async () => {
      const response = await fetch('https://jsonforge.example.com/users');
      users = await response.json();
    });
  </script>
  
  <style>
    .card-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      grid-gap: 1rem;
      margin: 1rem;
    }
  
    .card {
      background-color: #f9f9f9;
      border: 1px solid #ddd;
      border-radius: 4px;
      padding: 1rem;
    }
  
    .card__header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 1rem;
    }
  
    .card__title {
      margin: 0;
      font-size: 1.5rem;
      font-weight: 700;
      color: #333;
    }
  
    .card__copy-btn {
      background-color: #007aff;
      color: #fff;
      border: none;
      border-radius: 4px;
      padding: 0.5rem;
      font-size: 1rem;
      cursor: pointer;
      transition: background-color 0.2s ease-in-out;
    }
  
    .card__copy-btn:hover {
      background-color: #0055ff;
    }
  
    .card__code {
      margin: 0;
      font-size: 1.25rem;
      font-family: 'Roboto Mono', monospace;
      overflow-x: auto;
    }
  </style>
  
  <section>
    <h2>Users</h2>
    <div class="card-grid">
      {#each [1,2,3,4,5,5,6333] as user}
        <div class="card">
          <div class="card__header">
            <h3 class="card__title">{"hey"}</h3>
            <button class="card__copy-btn" on:click={() => copyToClipboard(JSON.stringify(user))}>Copy</button>
          </div>
          <pre class="card__code">{JSON.stringify(user, null, 2)}</pre>
        </div>
      {/each}
    </div>
  </section>
  
  <!-- <script>
    function copyToClipboard(text) {
      const el = document.createElement('textarea');
      el.value = text;
      document.body.appendChild(el);
      el.select();
      document.execCommand('copy');
      document.body.removeChild(el);
    }
  </script> -->
  