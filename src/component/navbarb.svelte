
<script>
  import SIgnin from "./SIgnin.svelte";

  export let showModal;
</script>
<main class="">

    <nav class="">
        <div class="row justify-content-center ">
            <h1 class="col-lg-6 mt-4 display-5 fw-bold">
                <a href="#/" style="text-decoration:none;">
                  <span class="logo">JSON<span>Forge</span></span>
                </a>
              </h1>
          <div class="col-lg-6 col-md-12 mt-4 d-flex justify-content-md-end justify-content-center align-items-center">
            <nav>
              <ul class="list-inline mb-0">
                <li class="list-inline-item mx-2"><a href="#/guide" style="text-decoration:none;color:black">Docs</a></li>
                <li class="list-inline-item mx-2"><a href="#/blogs" style="text-decoration:none;color:black">Blog</a></li>
                <li class="list-inline-item mx-2"><a href="#/guide" style="text-decoration:none;color:black">Contact</a></li>
              </ul>
            </nav>
          
            <button data-bs-toggle="modal" data-bs-target="#exampleModal1" class="btn btn-success btn-sm rounded-3 px-4 py-2" style="background-color: #00bfa5; border-color: #00bfa5;">
                <span style="font-weight: bold;">Sign in</span>
              </button>
          </div>
       
        </div>
    </nav>

  <SIgnin/>

</main>


<style>
 @media (max-width: 767px) {
    h1 {
      text-align: center;
    }
  }
  .btn-success:hover {
    background-color: #4cae4c;
    border-color: #4cae4c;
  }
  .btn-success:focus,
  .btn-success:active {
    background-color: #3d8b3d;
    border-color: #3d8b3d;
    box-shadow: none;
  }
 
.btn-get-started {
  background-color: #1c7a42;
  border-color: #1c7a42;
  color: #fff;
}

.btn-get-started:hover {
  background-color: #155e34;
  border-color: #155e34;
}

  .logo {
  font-size: 2rem;
  font-weight: bold;
  color: #00bfa5;
  border: 3px solid #00bfa5;
  padding: 5px 10px;
  border-radius: 10px;
}

.logo span {
  font-weight: normal;
  color: #000;
}

@media only screen and (max-width: 767px) {
  .logo {
    font-size: 1.5rem;
  }
}


</style>