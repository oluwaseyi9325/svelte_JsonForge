<!-- <main>
  <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h1 class="modal-title fs-5" id="exampleModalLabel">Modal title</h1>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          ...
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
          <button type="button" class="btn btn-primary">Save changes</button>
        </div>
      </div>
    </div>
  </div>
</main> -->

<!-- 
<main>
  <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content bg-dark text-light">
        <div class="modal-header">
          <h1 class="modal-title fs-5" id="exampleModalLabel">JSONforge</h1>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <form>
            <div class="mb-3">
              <label for="username" class="form-label">Username</label>
              <input type="text" class="form-control" id="username" placeholder="Enter your username">
            </div>
            <div class="mb-3">
              <label for="password" class="form-label">Password</label>
              <input type="password" class="form-control" id="password" placeholder="Enter your password">
            </div>
          </form>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
          <button type="button" class="btn btn-primary">Sign up</button>
        </div>
      </div>
    </div>
  </div>
</main> -->


<main>
  <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-sm modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header" style="background-color: #00bfa5; color: white;">
          <h1 class="modal-title fs-5" id="exampleModalLabel">JSONforge Sign-Up</h1>
          <!-- <h1 class="modal-title fs-5" id="exampleModalLabel">Sign up</h1> -->
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <form>
            <div class="mb-3">
              <label for="username" class="form-label">Username</label>
              <input type="text" class="form-control" id="username" placeholder="Enter username">
            </div>
            <div class="mb-3">
              <label for="password" class="form-label">Password</label>
              <input type="password" class="form-control" id="password" placeholder="Enter password">
            </div>
            <div class="mb-1">
              <button type="button" class="btn btn-primary col-12" style="background-color: #00bfa5; color: white;">Sign up</button>
            </div>
          </form>
        </div>
        <div class="modal-footer" style="background-color: #00bfa5;">
          <button type="button" class="btn btn-primary btn-sm" style="background-color: white;color:#00bfa5">Sign in</button>
          <!-- <button type="button" class="btn btn-secondary" data-bs-dismiss="modal" style="color: white;">Close</button> -->
          <!-- <button type="button" class="btn btn-primary text-white" style="background-color: #00bfa5;">Sign up</button> -->
        </div>
      </div>
    </div>
  </div>
</main>


<!-- <main>
  <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content bg-primary">
        <div class="modal-header">
          <h1 class="modal-title text-white fs-5" id="exampleModalLabel">JSONforge</h1>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <form>
            <div class="mb-3">
              <label for="username" class="form-label text-white">Username</label>
              <input type="text" class="form-control" id="username" placeholder="Enter username">
            </div>
            <div class="mb-3">
              <label for="password" class="form-label text-white">Password</label>
              <div class="input-group">
                <input type="password" class="form-control" id="password" placeholder="Enter password">
                <button class="btn btn-secondary" type="button" on:click={generatePassword}>Generate Password</button>
              </div>
            </div>
            <div class="mb-3">
              <label for="confirm-password" class="form-label text-white">Confirm Password</label>
              <input type="password" class="form-control" id="confirm-password" placeholder="Confirm password">
            </div>
            <div class="d-grid gap-2">
              <button type="submit" class="btn btn-dark">Sign up</button>
            </div>
          </form>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        </div>
      </div>
    </div>
  </div> -->
  <!-- <script>
    function generatePassword() {
      const lowercaseLetters = "abcdefghijklmnopqrstuvwxyz";
      const uppercaseLetters = lowercaseLetters.toUpperCase();
      const numbers = "0123456789";
      const characters = lowercaseLetters + uppercaseLetters + numbers;
      let password = "";
      for (let i = 0; i < 6; i++) {
        const randomIndex = Math.floor(Math.random() * characters.length);
        password += characters[randomIndex];
      }
      document.getElementById("password").value = password;
      console.log(password)
    }
  </script>
</main> -->
