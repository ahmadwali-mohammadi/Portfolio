<script>
  import { fly } from 'svelte/transition';
  import Menu from './lib/pages/NavBar.svelte';
  import Home from './lib/pages/Home.svelte';
  import Projects from './lib/pages/Projects.svelte';
  let name = 'Hi Ahmad Wali Mohammadi 👋';


  let loading = true;

// loading state
  setTimeout(() => {
    loading = false;
  }, 1500); 
  
</script>

<main>
  {#if loading}
    <div class="loader-wrapper">
     
      <h4>{name}</h4>
    </div>
    {:else}
      <Menu />
      <div in:fly={{y: 80, duration: 1000}}>
        <Home name={name}/>
        <Projects />
      </div>
      
  {/if}
  
</main>

<style>

.loader-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
  }

 

  .loader-wrapper h4 {
    font-size: 2rem;
    color: #333;
    margin-bottom: 20px;
    text-align: center;
  }


  @media (max-width: 768px) {
    .loader-wrapper h4 {
      font-size: 1.5rem;
    }
  }

  @media (max-width: 480px) {
    .loader-wrapper h4 {
      font-size: 1.2rem;
    }
  }

</style>
