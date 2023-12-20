<script>
    import planningSystem from "$lib/img/planningSystem.png"
    import Page from "./+page.svelte";

    const projects = [
        {
            name: "Planning System",
            discription: "Simple planning system for an ironing service, to plan in employees.",
            img: planningSystem,
            link: "https://github.com/wuringMatt/planningSystem",
            status: [
                {
                    name: "Svelte",
                    color: "255, 80, 0"
                },
                {
                    name: "W.i.P",
                    color: "0,150,0"
                },
            ]
        },
        {
            name: "Project 2",
            discription: "This is project number 2",
            img: "",
            link: "",
            status: []
        },
        {
            name: "Project 3",
            discription: "This is project number 3",
            img: "",
            link: "",
            status: []
        },
        {
            name: "Project 4",
            discription: "This is project number 4",
            img: "",
            link: "",
            status: []
        }
    ]
</script>

<div class="projects">
    <h2>Projects</h2>
    <div class="grid">
        {#each projects as project}
            <a class="gridItem" href="{project.link}" target="_blank">
                <img src="{project.img}" alt="">
                <div class="bottom">
                    <div class="title">
                        <h3>{project.name}</h3>
                        <ul class="status">
                            {#each project.status as state}
                                <li style="background-color: rgb({state.color});">{state.name}</li>
                            {/each}
                        </ul>
                    </div>
                    <p>{project.discription}</p>
                </div>
            </a>
        {/each}
    </div>
</div>

<style scoped>
    h2{
        font-size: 1.5rem;
        font-weight: 600;
        background-color: rgb(36, 36, 49);
        padding: 10px;
        padding-left: 15px;
    }

    .grid{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: auto;
        gap: 10px;
        padding-top: 10px;
    }

    .grid .gridItem{
        width: 100%;
        border: 1px solid rgb(36, 36, 49);
        border-radius: 15px;
        display: grid;
        grid-template-columns: 1fr;
        overflow: auto;
        text-decoration: none;
    }

    .grid .gridItem img {
        object-fit: cover;
        width: 100%;
        height: 225px;
    }

    .grid .gridItem .bottom {
        background-color: rgb(36, 36, 49);
        padding: 10px;
        filter: drop-shadow(0px -5px 15px rgba(0, 0, 0, 0.452));
    }

    .grid .gridItem h3 {
        font-size: 1.3rem;
    }

    .grid .gridItem p {
        margin-top: 10px;
        height: 50px;
    }

    .grid .gridItem .title{
        display: flex;
        justify-content: space-between;
    }

    .grid .gridItem .status{
        display: flex;
        gap: 5px;
    }

    .grid .gridItem .status li{
        padding: 5px 10px 5px 10px;
        border-radius: 15px;
    }
</style>