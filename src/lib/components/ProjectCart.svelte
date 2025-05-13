<script>
  export let title = "Project Title";
  export let description = "Short description of the project.";
  export let imageUrl = "/projects/drugs.jpg";
  export let appStoreLink = "#";
  export let playStoreLink = "#";
  export let bgColor = "#ffffff";
</script>

<div class="card" style="background-color: {bgColor};">

  <div class="card-content">
    <div class="card-body">
      <div class="card-title">{title}</div>
      <div class="card-description">{description}</div>
    </div>
    <div class="card-footer">
      <a class="store-button" href={appStoreLink} target="_blank">App Store</a>
      <a class="store-button" href={playStoreLink} target="_blank">Play Store</a>
    </div>
  </div>

  <div class="card-image">
    <img src={imageUrl} alt={title} />
  </div>
</div>

<style>
  .card {
    display: flex;
    flex-direction: row;
    width: 100%;
    max-width: 1000px;
    border-radius: 16px;
    overflow: hidden;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    margin: 1rem auto;
    transition: all 0.3s ease;
  }

  .card-content {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 1.5rem;
    background-color: inherit;
  }

  .card-title {
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 0.5rem;
  }

  .card-description {
    font-size: 1rem;
    color: #555;
    margin-bottom: 1rem;
  }

  .card-footer {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .store-button {
    background-color: #000;
    color: #fff;
    text-decoration: none;
    padding: 0.6rem 1rem;
    border-radius: 6px;
    flex: 1 1 auto;
    text-align: center;
    font-size: 0.9rem;
    transition: background 0.3s;
  }

  .store-button:hover {
    background-color: #333;
  }

  .card-image {
    flex: 1;
    height: auto;
    overflow: hidden;
  }

  .card-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  /* 📱 ریسپانسیو برای موبایل */
  @media (max-width: 768px) {
    .card {
      flex-direction: column;
    }

    .card-image {
      height: 200px;
    }

    .card-footer {
      flex-direction: column;
    }

    .store-button {
      width: 100%;
    }
  }
</style>
