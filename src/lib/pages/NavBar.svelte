
<script>

  let menuOpen = false;
</script>


<nav class="navbar">
  <div class="logo">Ahmad wali Mohammadi</div>
  <button class="menu-toggle" on:click={() => menuOpen = !menuOpen}>☰</button>
  <div class="links {menuOpen ? 'open' : ''}">
    <a href="#home" class="link" on:click={() => menuOpen = false}>Home</a>
    <a href="#projects" class="link" on:click={() => menuOpen = false}>Projects</a>
    <a href="#tools" class="link" on:click={() => menuOpen = false}>Tools</a>
    <a href="#contact"  class="link about-me" on:click={() => menuOpen = false}>Contact</a>
  </div>
</nav>



<style>
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 16px 60px;
    background: #FFF;
    flex-wrap: wrap;
    position: sticky;
  }
  .logo {
    font-weight: bold;
    font-size: 1.2rem;
  }
  .links {
    display: flex;
    gap: 1rem;
  }
  .link {
    cursor: pointer;
    font-weight: 500;
    color: #333;
    text-decoration: none;
  }
 
  .menu-toggle {
    display: none;
    font-size: 1.5rem;
    background: none;
    border: none;
    cursor: pointer;
  }

  .about-me {
    background-color:black;
    color: white;
    border-radius: 20px;
    text-align: center;
    width: 80px;
    height: 30px;
    
}

.about-me:hover {
  background-color: #f0f0f0;
  outline: 1px solid #333;
}
  @media (max-width: 768px) {
    .menu-toggle {
      display: block;
    }
    .links {
      display: none;
      flex-direction: column;
      width: 100%;
      margin-top: 1rem;
    }
    .links.open {
      display: flex;
    }
    .link {
      padding: 0.5rem 0;
    }
    .navbar {
      padding: 16px 15px;
    }

    .menu-toggle{
      width: 30px;
      padding-right: 20px;
    }
  
  }
</style> 