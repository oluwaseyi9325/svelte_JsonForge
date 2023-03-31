<script>
     let username="";
     let password="";
    let loader="Sign In"
   const signInBtn=()=>{
      loader='.........'
    let details={username,password}
        if (username&&password) {
          loader="Validating your details"
          console.log(details) 
        }else{
          loader="Sign In"
          alert("Dear Dev,\nKindly enter your sign-in details!")
        }
     }

</script>

<main>
    <div class="modal fade" id="exampleModal1" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
      <div class="modal-dialog modal-sm modal-dialog-centered">
        <div class="modal-content">
          <div class="modal-header" style="background-color: #00bfa5; color: white;">
            <h1 class="modal-title fs-5" id="exampleModalLabel">JSONforge Sign-In</h1>
            <!-- <h1 class="modal-title fs-5" id="exampleModalLabel">Sign up</h1> -->
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body">
            <form>
              <div class="mb-3">
                <label for="username" class="form-label">Username</label>
                <input type="text" bind:value={username} class="form-control" id="username" placeholder="Enter username">
              </div>
              <div class="mb-3">
                <label for="password" class="form-label">Password</label>
                <input bind:value={password} type="password" class="form-control" id="password" placeholder="Enter password">
              </div>
              <div class="mb-1">
                <button type="button" on:click={signInBtn} class="btn btn-primary col-12" style="background-color: #00bfa5; color: white;">{loader} <span class="spinner spinner-border"></span></button>
                <button type="button" on:click={signInBtn} class="btn btn-primary col-12" style="background-color: #00bfa5; color: white;"><span class="spinner-grow spinner-grow-sm"></span>Loading...</button>
              </div>
            </form>
          </div>
          <div class="modal-footer" style="background-color: #00bfa5;">
            <button type="button" class="btn btn-primary btn-sm" style="background-color: white;color:#00bfa5">Sign Up</button>
          </div>
        </div>
      </div>
    </div>
  </main>
  
  