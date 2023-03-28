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
                    <div class="rounded-3 text-white" style="background-color: #2D2D2D;">
                        <div class="text-end p-1">
                            <button class="btn btn-sm bg-white text-end  text-black">copy</button>
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