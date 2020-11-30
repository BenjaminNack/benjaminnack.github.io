<script>
    const cards = [
        { 
            title: "Watermelon Lol",
            bannerURL: "https://brainfactorygraphicsengine.files.wordpress.com/2013/07/shutterstock-1.jpg",
            bannerAlt: "Test card",
            description: "This is a test"
        },
        { 
            title: "Ur dum",
            bannerURL: "https://brainfactorygraphicsengine.files.wordpress.com/2013/07/shutterstock-1.jpg",
            bannerAlt: "Test card",
            description: "It's true"
        }
    ];

</script>

<header>
    <section class="header-tags">
        <h1>Hi,</h1>
        <h1>my name is Benjamin,</h1>
        <h1>but you can call me Ben</h1>
        <h3>I'm a self taught software developer/engineer.</h3>
    </section>
</header>

<p>Here are some of my projects</p>
<div class="projects">
    {#each cards as { title, bannerURL, bannerAlt, description }}
        <div class="card">
            <h3>{ title }</h3>
            <div class="card-banner-crop">
                <img src="{ bannerURL }" alt="{bannerAlt} banner"/>
            </div>
            <p>{ description }</p>
        </div>
    {/each}
</div>

<style>
    header {
        display: flex;
        justify-content: center;
        align-items: center;
        
        flex-direction: column;
        width: 100%;
    }

    header h1 {
        margin-top: 0;
        margin-bottom: 3vh;
    }

    header h3 {
        margin-top: 5vh;
    }

    .projects {
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        flex-shrink: 0;
        justify-items: flex-start;
        align-items: stretch;
        gap: 10px;
        height: 300px;

        overflow: auto;

        border: gray 1px solid;
        border-radius: 3px;
        padding: 10px;
    }

    .card {
        display: flex;
        flex-direction: column;

        background-color: white;
        color: #000;

        height: 100%;
        width: 250px;
        min-width: 250px;
        border-radius: 5%;
        box-shadow: 4px 4px 4px black;
    }

    .card * {
        margin-left: 10%;
    }

    .card-banner-crop {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 80%;
        overflow: hidden;
        max-height: 200px;
        
    }
    .card-banner-crop img {
        max-width: 100%;
        max-height: 100%;
    }
</style>