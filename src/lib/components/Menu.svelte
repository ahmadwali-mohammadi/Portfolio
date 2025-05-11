<script>
    let menuItems = ['Home', 'About', 'Services', 'Contact'];
    let active = 'Home';
  
    function navigate(item) {
      active = item;
      // Add routing logic here if needed
    }
  </script>
  
  

    <!-- Right: Menu items -->
    <nav>
        <!-- Left: Logo -->
        <div class="logo">AHMAD WALI </div>
      
        <!-- Right: Menu items -->
        <div class="menu">
          {#each menuItems as item}
            <span
              class="menu-item {item === active ? 'active' : ''}"
              on:click={() => navigate(item)}
            >
              {item}
            </span>
          {/each}
        </div>
      </nav>
  

  <style>
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 16px 60px;
    

    }
  
    .logo {
      font-weight: bold;
      font-size: 1.2rem;
      color: #222;
    }
  
    .menu {
      display: flex;
      gap: 20px;
      
     

    }
  
    .menu-item {
      cursor: pointer;
      font-weight: 500;
      color: #333;
      text-decoration: none;
    }
  
    .menu-item.active {
      color: blue;
    }
  </style>
  