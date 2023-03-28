<script>
  import { each } from "svelte/internal";

</script>
<main>
    <div class="my-5">
        <h4>Guides</h4>

        <section>
            <div>
                <h5>Getting Started</h5>
                <p>Learn how to get started with JSON Forge</p>
                <a href="">Read the guide</a>
            </div>
            <div>
                <h3>Resource</h3>

                {#each [1,2,3,4,5,6,7] as item}

                <div class="mt-5">
                    <h6>Making a get Request</h6>
                    <div sty class="rounded-3 text-white" style="background-color: #2D2D2D;border: 3px dashed #00bfa5">
                        <div class="text-end p-1">
                            <button style="background-color: #00bfa5;" class="btn btn-sm rounded-pill text-end  text-white">copy</button>
                        </div>
                        <div class="px-5 pb-5">
                           fetch('https://onrender/jsonforge/users')<br/>
                               <span class="ml-4"> .then((response) => response.json())</span><br/>
                                .then((json) => console.log(json));
                        </div>
                    </div>

                </div>

                {/each}

            </div>
        </section>
    </div>

       
</main>


<!-- <script>
    let request = `fetch('https://onrender/jsonforge/users')\n  .then(response => response.json())\n  .then(json => console.log(json));`;
    let isCopied = false;
  
    function copyToClipboard() {
      const el = document.createElement('textarea');
      el.value = request;
      document.body.appendChild(el);
      el.select();
      document.execCommand('copy');
      document.body.removeChild(el);
      isCopied = true;
    }
  </script> -->
  
  <!-- <section>
    <h2>Make a GET request</h2>
    <p>
      You can retrieve data from JSON Forge by sending a GET request to the API endpoint. The endpoint URL is formed as follows:
    </p>
    <code>https://jsonforge.example.com/your_api_routes</code>
    <p>
      Replace <code>your_api_routes</code> with the name of the data you want to retrieve, such as <code>users</code>.
    </p>
  
    <div class="request-box">
      <div class="request-box__header">
        <h3 class="request-box__title">Example Request</h3>
        <button class="request-box__copy-btn" on:click={copyToClipboard}>{isCopied ? 'Copied!' : 'Copy'}</button>
      </div>
      <pre class="request-box__code">{request}</pre>
    </div>
    
  </section> -->

  
  <!-- <style>
    section {
      margin: 2rem 0;
    }
  
    .request-box {
      background-color: #f9f9f9;
      border: 1px solid #ddd;
      border-radius: 4px;
      padding: 1rem;
    }
  
    .request-box__header {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
  
    .request-box__title {
      margin: 0;
      font-size: 1.5rem;
      font-weight: 700;
      color: #333;
    }
  
    .request-box__copy-btn {
      background-color: #007aff;
      color: #fff;
      border: none;
      border-radius: 4px;
      padding: 0.5rem;
      font-size: 1rem;
      cursor: pointer;
      transition: background-color 0.2s ease-in-out;
    }
  
    .request-box__copy-btn:hover {
      background-color: #0055ff;
    }
  
    .request-box__code {
      margin: 0;
      font-size: 1.25rem;
      font-family: 'Roboto Mono', monospace;
      overflow-x: auto;
    }
  </style> -->
  