<script>
    import ProjectCart from "../components/ProjectCart.svelte";
</script>


<section id="projects" >
<div style="display: flex; flex-wrap: wrap; justify-content: center;">
     <ProjectCart
        title="My App"
        description="This is a demo application."
        imageUrl="/images/myapp.jpg"
        appStoreLink="https://apps.apple.com/app/id..."
        playStoreLink="https://play.google.com/store/apps/details?id=..."
        bgColor="#F9E6FF"
     />
</div>
<div style="display: flex; flex-wrap: wrap; justify-content: center;">
     <ProjectCart
        title="My App"
        description="This is a demo application."
        imageUrl="/projects/drugs.jpg"
        appStoreLink="https://apps.apple.com/app/id..."
        playStoreLink="https://play.google.com/store/apps/details?id=..."
        bgColor="#F9E6FF"
     />
</div>
</section>


<style>
    section{
        position: relative;
        top: -50px;
    }
</style>