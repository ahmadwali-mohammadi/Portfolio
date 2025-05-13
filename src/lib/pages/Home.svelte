<!-- components/Home.svelte -->
<script>
  export let name = "Your Name";
</script>

<section id="home">
  <div class="home-dev">
      <h4> {name}</h4>
      <h1 class="programmer-sentence">I build modern web applications that solve real problems</h1>
  </div>
    <div class="button-group">
        <button class="cta my-works" on:click={() => alert('View Projects')}>My Works</button>
        <button class="cta about-me" on:click={() => alert('About Me')}>About Me</button>
     </div>
 
</section>




<style>
  section {
    padding: 0rem 2rem;
    margin: 100px 5px 5px;
    text-align: center;
    background-color: #ffffff;
    min-height: 80vh;
    align-items: center;
    border-radius: 64px 64px 0px 0px;
    background: radial-gradient(80.08% 53% at 50% 69.5%, #FAFFE6 0%, #FAFFE6 100%);
    /* position: relative; */
  }

 
  .cta {
    
    padding: 0.75rem 1.5rem;
    font-size: 1rem;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  .cta:hover {
    background-color: #0056b3;
  }
  .programmer-sentence {
    font-size: 2.5rem;
    width: 100%;
    font-weight: bold;
    color: #333;
    margin-bottom: 1rem;
  }

.button-group {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
    justify-content: center;
}

.cta.my-works {
   background-color:black;
  color: white;
  padding: 0.75rem 1.5rem;
  font-size: 1rem;
  width: 150px;
  border: none;
  border-radius: 20px;

}

.cta.my-works:hover {
  background-color: #333;
}

.cta.about-me {
  background-color:white;
  color: black;
  padding: 0.75rem 1.5rem;
  font-size: 1rem;
  width: 150px;
  border: none;
  border-radius: 20px;
  outline: 1px solid black;
  outline-offset: -2px;
  font-weight: bold;
}

.cta.about-me:hover {
  background-color: #f0f0f0;
  outline: 1px solid #333;
}

  .home-dev{
    width:70%;
    margin: 0 auto;
    padding: 0.5rem 1rem;
    }

  @media (max-width: 768px) {
    h1 {
      font-size: 2.2rem;
    }

    .programmer-sentence {
      font-size: 20px;
      width: 100%;
    }
  
   section {
    padding: 1rem 2rem;
    margin: -140px 5px 5px;
    text-align: center;
    background-color: #ffffff;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border-radius: 64px 64px 0px 0px;
    background: radial-gradient(80.08% 53% at 50% 69.5%, #FAFFE6 0%, #FAFFE6 100%);
  }

  .home-dev{
    width:100%;
    margin: 0 auto;
    padding: 0.5rem 1rem;
    }
.programmer-sentence{
  font-size: 17px;
  width: 100%;
  font-weight: bold;
  color: #333;
  margin-bottom: 1rem;
}


}
</style>
