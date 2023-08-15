<script>
    import { onDestroy } from "svelte";

    const birthTimestamp = 945177705;

    let currFilter = ""
    let hasFiltered = false
    let filteredSkills = []
    let filteredOpts = []

    // best > worst
    let skills = [ 
        // JS Frameworks
        {name: "Svelte", type: "JS Frameworks", experience: 1, favourite: 2, eager: 3}, 
        {name: "React", type: "JS Frameworks", experience: 2, favourite: 1, eager: 1}, 
        {name: "Vue", type: "JS Frameworks", experience: 3, favourite: 3, eager: 2}, 
        // Databases
        {name: "Firebase", type: "Databases", experience: 3, favourite: 3, eager: 3}, 
        {name: "MSSQL", type: "Databases", experience: 2, favourite: 2, eager: 2}, 
        {name: "PostgreSQL", type: "Databases", experience: 1, favourite: 1, eager: 1}, 
        // Mobile
        {name: "Flutter", type: "Mobile", experience: 2, favourite: 2, eager: 1}, 
        {name: "React Native", type: "Mobile", experience: 1, favourite: 1, eager: 2}, 
        // CSS Frameworks
        {name: "Bootstrap", type: "CSS Frameworks", experience: 3, favourite: 3, eager: 3}, 
        {name: "Tailwind", type: "CSS Frameworks", experience: 1, favourite: 1, eager: 1}, 
        {name: "Fomantic-UI", type: "CSS Frameworks", experience: 2, favourite: 2, eager: 2}, 
        // Languages
        {name: "Javascript", type: "Languages", experience: 6, favourite: 6, eager: 4}, 
        {name: "Typescript", type: "Languages", experience: 3, favourite: 4, eager: 6},
        {name: "Java", type: "Languages", experience: 2, favourite: 1, eager: 1}, 
        {name: "C#", type: "Languages", experience: 5, favourite: 3, eager: 3}, 
        {name: "Dart", type: "Languages", experience: 4, favourite: 5, eager: 5}, 
        {name: "C++", type: "Languages", experience: 1, favourite: 2, eager: 2},
        // Testing Frameworks
        // Other
    ]

    const filterOpts = ["JS Frameworks", "Databases", "Mobile", "Languages", "CSS Frameworks"]

    const orderOpts = ["Experience", "Favourite", "Eager to learn more"]

    filteredSkills = skills
    filteredOpts = filterOpts


    let currentTimestamp = Math.floor(Date.now() / 1000);
    let secondsDiff = currentTimestamp - birthTimestamp;
    let yearsDiff = secondsDiff / (365.25 * 24 * 60 * 60);
    
    let myBd = yearsDiff

    const interval = setInterval(() => {
        currentTimestamp = Math.floor(Date.now() / 1000);
        secondsDiff = currentTimestamp - birthTimestamp;
        yearsDiff = secondsDiff / (365.25 * 24 * 60 * 60);

        myBd = yearsDiff
    }, 3500);

    onDestroy(() => {
        clearInterval(interval);
    });

    function filterSkills(filter) {
        currFilter = filter
        hasFiltered = true 
        filteredSkills = skills.filter(skill => skill.type === filter)
        filteredOpts = filterOpts.filter(type => type === filter)
    }

    function orderSkills(order) {
        switch(order) {
            case "Experience":
                filteredSkills = filteredSkills.sort((skillA, skillB) =>  skillB?.experience - skillA?.experience)
                break;
            case "Favourite":
                filteredSkills = filteredSkills.sort((skillA, skillB) =>  skillB?.favourite - skillA?.favourite)
                break;
            case "Eager to learn more":
                filteredSkills = filteredSkills.sort((skillA, skillB) =>  skillB?.eager - skillA?.eager)
                break;
            default:
                filteredSkills = skills
                break;
        }
    }

    function resetSkills() {
        currFilter = ""
        hasFiltered = false
        filteredSkills = skills
        filteredOpts = filterOpts
    }
</script>

<div id="about_container">
    <div class="d-flex flex-row" style="height: 529px">
        <div id="keyword" class="space">
            export default
        </div>
        <div id="class" class="space">
            class
        </div>
        <div id="class_name" class="space">
            Thomas_Taulo
        </div>
        <div id="classEntity">
            &#123;
        </div>
        <div id="constructor">
            <div class="d-flex" style="height: 88px;">
                <div id="class">
                    constructor
                </div>
                <div id="keyword" class="space">
                    ()
                </div>
                <div id="keyword">
                    &#123;
                </div>
                <div class="d-flex flex-column" id="constructor_content">
                    <div id="constructor_name" class="d-flex">
                        <div id="class">
                            this
                        </div>
                        <div id="identifier" class="space">
                            .name
                        </div>
                        <div class="space">
                            =
                        </div>
                        <div id="string">
                            "Thomas Taulo"
                        </div>
                    </div>
                    <div id="constructor_age" class="d-flex">
                        <div id="class">
                            this
                        </div>
                        <div id="identifier" class="space">
                            .age
                        </div>
                        <div class="space">
                            =
                        </div>
                        <div id="string">
                            "{myBd.toFixed(7)} years old"
                        </div>
                    </div>
                    <div id="constructor_email" class="d-flex">
                        <div id="class">
                            this
                        </div>
                        <div id="identifier" class="space">
                            .email
                        </div>
                        <div class="space">
                            =
                        </div>
                        <div id="string">
                            "taulo@live.dk"
                        </div>
                    </div>
                </div>
            </div>
            <!-- END OF CONSTRUCTOR '}' -->
            <div id="keyword">
                &#125;
            </div>
        </div>
        <div id="education_function">
            <div class="d-flex" style="height: 40px;">
                <div id="function">
                    education
                </div>
                <div id="keyword" class="space">
                    ()
                </div>
                <div id="keyword">
                    &#123;
                </div>
                <div class="d-flex flex-row" id="education_content">
                    <div id="keyword" class="space">
                        return
                    </div>
                    <div id="class" class="space">
                        [
                    </div>
                    <div id="classEntity" class="space">
                        &#123;
                    </div>
                    <div id="string">
                        "2021-2023"
                    </div>
                    <div class="space">
                        :
                    </div>
                    <div id="string">
                        "AP Degree in Computer Science"
                    </div>
                    <div id="classEntity" class="space">
                        &#125;
                    </div>
                    <div id="class">
                        ]
                    </div>
                </div>
            </div>
            <!-- END OF EDUCATION '}' -->
            <div id="keyword">
                &#125;
            </div>
        </div>
        <div id="work_function">
            <div class="d-flex" style="height: 40px;">
                <div id="function">
                    workExperience
                </div>
                <div id="keyword" class="space">
                    ()
                </div>
                <div id="keyword">
                    &#123;
                </div>
                <div class="d-flex flex-row" id="work_content">
                    <div id="keyword" class="space">
                        return
                    </div>
                    <div id="class" class="space">
                        [
                    </div>
                    <div id="classEntity" class="space">
                        &#123;
                    </div>
                    <div id="string">
                        "2022-"
                    </div>
                    <div class="space">
                        :
                    </div>
                    <div id="string">
                        "Sirenia A/S"
                    </div>
                    <div id="classEntity" class="space">
                        &#125;
                    </div>
                    <div id="class">
                        ]
                    </div>
                </div>
            </div>
            <!-- END OF WORK '}' -->
            <div id="keyword">
                &#125;
            </div>
        </div>
        <div id="skills_function">
            <div class="d-flex" style="height: 116px;">
                <div id="function">
                    skills
                </div>
                <div id="keyword" class="space">
                    ()
                </div>
                <div id="keyword">
                    &#123;
                </div>
                <div class="d-flex flex-row" id="skills_content">
                    <div id="keyword" class="space">
                        return
                    </div>
                    <div id="class" class="space">
                        [
                    </div>
                    <!-- SKILLS START -->
                    <div class="d-flex flex-wrap">
                        {#each filteredSkills as skill, index}
                            {#if filteredSkills.length - 1 === index}
                                <div id="string"> 
                                    "{skill.name}"
                                </div>
                                <div id="keyword">
                                    ]
                                </div>
                            {:else}
                            <div id="string" class="skill_item">
                                "{skill.name}"
                            </div>
                            <div class="space">,</div>
                            {/if}
                        {/each}
                    </div>
                    <!-- SKILLS END -->
                </div>
            </div>
            <!-- FILTER START -->
            <div class="d-flex" style="margin-left: 65px;">
                <div>
                    .
                </div>
                <div id="function">
                    filter
                </div>
                <div id="keyword">
                    (
                </div>
                <div> 
                    {#each filteredOpts as filter, index}
                    {#if filteredOpts.length - 1 === index}
                    <div class="d-flex">
                        <div id="string">
                            "
                        </div>
                        <div class="filter_item" on:click={filterSkills(filter)} tabindex=0 role="button" on:keypress={null}>
                            {filter}
                        </div>
                        <div id="string">
                            "
                        </div>
                        <div id="keyword">
                            )
                        </div>
                    </div>
                    {:else}
                    <div class="d-flex">
                        <div id="string">
                            "
                        </div>
                        <div class="filter_item" on:click={filterSkills(filter)} tabindex=0 role="button" on:keypress={null}>
                            {filter}
                        </div>
                        <div id="string">
                            "
                        </div>
                        <div>
                            ,
                        </div>
                    </div>
                    {/if}
                    {/each}
                </div>
            </div>
            <!-- FILTER END -->
            <!-- ORDER START -->
            {#if hasFiltered}
            <div class="d-flex" style="margin-left: 65px;">
                <div>
                    .
                </div>
                <div id="function">
                    order
                </div>
                <div id="keyword">
                    (
                </div>
                <div> 
                    {#each orderOpts as order, index}
                    {#if orderOpts.length - 1 === index}
                    <div class="d-flex">
                        <div id="string">
                            "
                        </div>
                        <div class="filter_item" on:click={() => orderSkills(order)} tabindex=0 role="button" on:keypress={null}>
                            {order}
                        </div>
                        <div id="string">
                            "
                        </div>
                        <div id="keyword">
                            )
                        </div>
                    </div>
                    {:else}
                    <div class="d-flex">
                        <div id="string">
                            "
                        </div>
                        <div class="filter_item" on:click={() => orderSkills(order)} tabindex=0 role="button" on:keypress={null}>
                            {order}
                        </div>
                        <div id="string">
                            "
                        </div>
                        <div>
                            ,
                        </div>
                    </div>
                    {/if}
                    {/each}
                </div>
            </div>
            {/if}
            
            <!-- ORDER END -->
            <div id="keyword">
                &#125;
            </div>
            <!-- END OF SKILLS '}' -->
        </div>
    </div>
    <!-- END OF CLASS '}'-->
    <div id="classEntity">
        &#125;
    </div>
</div>

<button class="btn btn-primary position-absolute" on:click={resetSkills}>reset</button>

<style>
    #about_container{
        width: 500px;
        transform: translateY(-3px);
    }

    #constructor {
        margin-top: 20px;
        margin-left: 35px;
        width: 100%;
        position: absolute;
    }

    #constructor_content {
        margin-top: 20px;
        margin-left: 35px;
        position: absolute;
    }

    #education_function {
        margin-left: 35px;
        margin-top: 135px;
        width: 100%;
        position: absolute;
    }

    #education_content {
        margin-top: 20px;
        margin-left: 35px;
        position: absolute;
    }

    #work_function {
        margin-left: 35px;
        margin-top: 203px;
        width: 100%;
        position: absolute;
    }

    #work_content {
        margin-top: 20px;
        margin-left: 35px;
        position: absolute;
    }

    #skills_function {
        margin-left: 35px;
        margin-top: 270px;
        width: 100%;
        position: absolute;
    }

    #skills_content {
        margin-top: 20px;
        margin-left: 35px;
        position: absolute;
    }

    .filter_item {
        color: #c48e76;
    }

    .filter_item:hover {
        color: white;
        cursor: pointer;
    }   
</style>