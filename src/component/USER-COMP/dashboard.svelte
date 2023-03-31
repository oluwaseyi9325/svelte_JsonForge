<script>
  // import { onMount } from "svelte";


  let inputValue=""

  const addBtn=()=>{
     alert(inputValue)
  }

    let isLoading = false;
    let isError = false;
    let errorMessage = '';
    let results = null;
    let apiData=null;
    async function hand(){
        isLoading = true;
      isError = false;
      errorMessage = '';
      results = null;
      try {
        const response = await fetch("http://localhost:5000/posts");
        const json = await response.json();
        results = json;
      } catch (error) {
        isError = true;
        errorMessage = error.message;
      }
  
      isLoading = false;
      
    }
   
</script>

<main  class="my-3">

    <div class="shadow rounded-4 border" style="background-color:white">
        <section class="py-3 px-2">
            <h4 class="text-center">Create APIs</h4> 

            <div class="text-center col-lg-7 mx-auto">
                <div class="text-center input-group"> 
                 
                    <input bind:value={inputValue} placeholder="Enter the name of your api" class="form-control" />
                    <button on:click={addBtn} style="background-color: #00bfa5;" class="btn  btn-lg text-white" >Create API</button>
                    
                </div>
            </div>
            <hr/>
            <div class="row">
               <section class="col-lg-6 col-md-7">
                
                    <div>
                        <h4 style="background-color:#00bfa5;" class="text-center text-white py-2">List of APIs</h4>
                        <div style="overflow:auto;height:400px">
                            <ol>
                                {#each [1,2,3,4,5,5] as val,i}
                               
                                   <!-- svelte-ignore a11y-click-events-have-key-events -->
                                   <li on:click={()=>hand()} class="bg-white my-3 apiLIst p-3 rounded-4 shadow border " style="border-color: #00bfa5 !important;">
                                   <span class="d-flex justify-content-between">
                                    <span>
                                      https://jsonforge/onrender/12344post-e32dhjdasdjh
                                    
                                  </span>
                                  <span class="bg-white text-danger  rounded-2 text-end"><i class="bi shadow border p-1 rounded-3 bi-trash-fill p-"></i></span> 
                                   </span>
                                   </li>
                                  
                                {/each}
                            </ol>
                        </div>
                       
                    </div>
                 

               </section>
               <section class="col-lg-6 col-md-7">
                    
                    <div style="overflow:auto;height:400px" class="">

                        {#if isLoading}
        <p>Loading...</p>
      {:else if isError}
        <p>Error: {errorMessage}</p>
      {:else if results === null}
        <p>Results will be displayed here.</p>
      {:else}
        <pre class="bg-black text-white p-3">{JSON.stringify(results, null, 2)}</pre>
      {/if}
                        
                       
                    </div>
               </section>
            </div>

        </section>
    </div>

</main>


<style>

    .btn-create{
        background-color: white;
  color: #00bfa5;
  border-color: white;
    }

    .apiLIst:hover{
      cursor: pointer;
    background-color: #00bfa5 !important;
    color: white !important;
    }

</style>

 <!-- this is the user dashboard for the "JSONforge" api project, please redesign the ui for me and male it interractive using boostrap and css with svelte, and my primary colors is #00bfa5 ,white,black  -->