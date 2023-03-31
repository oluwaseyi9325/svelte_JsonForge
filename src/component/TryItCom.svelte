<script>
    let endpoint = 'https://jsonplaceholder.typicode.com/todos/1';
    let isLoading = false;
    let isError = false;
    let errorMessage = '';
    let results = null;
  
    function handleEndpointChange(event) {
      endpoint = event.target.value;
    }
  
    async function handleTestClick() {
      isLoading = true;
      isError = false;
      errorMessage = '';
      results = null;
  
      try {
        const response = await fetch(endpoint);
        const json = await response.json();
        results = json;
      } catch (error) {
        isError = true;
        errorMessage = error.message;
      }
  
      isLoading = false;
    }
  </script>
  
  <section>
    <h2>Try it out</h2>
    <p>
      Enter the API endpoint you want to test and click the "Test" button. The API will be called with the provided endpoint URL and the response will be displayed below.
    </p>
    <div class="try-box">
      <div class="try-box__inputs">
        <label for="endpoint-input">Endpoint:</label>
        <input type="text" id="endpoint-input" bind:value={endpoint} on:input={handleEndpointChange} />
        <button on:click={handleTestClick} disabled={isLoading}>Test</button>
      </div>
      {#if isLoading}
        <p>Loading...</p>
      {:else if isError}
        <p>Error: {errorMessage}</p>
      {:else if results === null}
        <p>Results will be displayed here.</p>
      {:else}
        <pre>{JSON.stringify(results, null, 2)}</pre>
      {/if}
    </div>
  </section>
  
  <style>
    section {
      margin: 2rem 0;
    }
  
    .try-box {
      background-color: #f9f9f9;
      border: 1px solid #ddd;
      border-radius: 4px;
      padding: 1rem;
    }
  
    .try-box__inputs {
      display: flex;
      flex-direction: column;
      margin-bottom: 1rem;
    }
  
    .try-box__inputs label {
      margin-bottom: 0.5rem;
      font-size: 1.2rem;
      font-weight: bold;
      color: #333;
    }
  
    .try-box__inputs input {
      margin-bottom: 1rem;
      padding: 0.5rem;
      border: none;
      border-radius: 4px;
      font-size: 1rem;
    }
  
    .try-box__inputs button {
      background-color: #007aff;
      color: #fff;
      border: none;
      border-radius: 4px;
      padding: 0.5rem;
      font-size: 1rem;
      cursor: pointer;
      transition: background-color 0.2s ease-in-out;
    }
  
    .try-box__inputs button:disabled {
      opacity: 0.5;
      cursor: not-allowed;
    }
  
    .try-box__inputs button:hover {
      background-color: #0055ff;
    }
  
    pre {
      margin: 0;
      font-size: 1.25rem;
      font-family: 'Roboto Mono', monospace;
      overflow-x: auto;
    }
  </style>
  