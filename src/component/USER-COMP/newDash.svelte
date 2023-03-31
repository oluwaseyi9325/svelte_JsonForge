<script>
    let routes = [];
    let currentRoute = "";
    let apis = {};
    let selectedApi = null;
    let isModalOpen = false;
  
    function addRoute() {
      routes = [...routes, currentRoute];
      currentRoute = "";
    }
  
    function addApi() {
      if (selectedApi && selectedApi.trim() !== "") {
        apis[selectedApi] = {};
        selectedApi = null;
      }
    }
  
    function deleteApi(apiName) {
      delete apis[apiName];
    }
  
    function selectApi(apiName) {
      selectedApi = apiName;
    }
  
    function closeModal() {
      isModalOpen = false;
    }
  
    function viewApi(apiName) {
      selectedApi = apiName;
      isModalOpen = true;
    }
  </script>
  
  <main>
    <div class="container py-3">
      <div class="row">
        <div class="col-md-4">
          <h2>Create Routes</h2>
          <div class="input-group mb-3">
            <input type="text" class="form-control" placeholder="Route Name" bind:value={currentRoute}>
            <div class="input-group-append">
              <button class="btn btn-primary" type="button" on:click={addRoute}>Add Route</button>
            </div>
          </div>
          <ul class="list-group">
            {#each routes as route}
              <li class="list-group-item">{route}</li>
            {/each}
          </ul>
        </div>
        <div class="col-md-8">
          <h2>Create APIs</h2>
          <div class="input-group mb-3">
            <input type="text" class="form-control" placeholder="API Name" bind:value={selectedApi}>
            <div class="input-group-append">
              <button class="btn btn-primary" type="button" on:click={addApi}>Add API</button>
            </div>
          </div>
          <div class="card-columns">
            {#each Object.keys(apis) as apiName}
              <div class="card mb-3">
                <div class="card-body">
                  <h5 class="card-title">{apiName}</h5>
                  <p class="card-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris eu mauris velit.</p>
                  <div class="btn-group" role="group" aria-label="API Actions">
                    <button type="button" class="btn btn-primary" on:click={() => viewApi(apiName)}>View API</button>
                    <button type="button" class="btn btn-danger" on:click={() => deleteApi(apiName)}>Delete API</button>
                  </div>
                </div>
              </div>
            {/each}
          </div>
        </div>
      </div>
    </div>
  
    {#if isModalOpen}
      <div class="modal" tabindex="-1" role="dialog">
        <div class="modal-dialog modal-lg" role="document">
          <div class="modal-content">
            <div class="modal-header">
              <h5 class="modal-title">{selectedApi}</h5>
              <button type="button" class="close" aria-label="Close" on:click={closeModal}>
                <span aria-hidden="true">&times;</span>
              </button>
            </div>
            <div class="modal-body">
              <pre>{JSON.stringify(apis[selectedApi], null, 2)}</pre>
            </div>
          </div>
        </div>
        </div>
    {/if}
    </main>
  