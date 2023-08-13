<script>
    import { onDestroy } from "svelte";

    let currentDate = new Date();

    function updateDate() {
    currentDate = new Date();
    }

        // Update the date every second
    const interval = setInterval(updateDate, 1000);

    // Cleanup the interval when the component is destroyed
    onDestroy(() => {
        clearInterval(interval);
    });


    function myBD() {
        const date = new Date()
        // date.ge
    }
</script>

<div id="about_container">
    <div class="d-flex flex-row justify-content-between" style="height: 265px">
        <div id="export_defualt" class="space">
            export default
        </div>
        <div id="class" class="space">
            class
        </div>
        <div id="class_name" class="space">
            Thomas_Taulo
        </div>  
        <div id="entity">
            &#123;
        </div>
        <div id="constructor">
            <div class="d-flex" style="height: 88px;">
                <div id="class">
                    constructor
                </div>
                <div id="export_defualt" class="space">
                    ()
                </div>
                <div id="export_defualt">
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
                            .dayOfBirthTS
                        </div>
                        <div class="space">
                            =
                        </div>
                        <div id="string">
                            "{currentDate}"
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
            <div id="export_defualt">
                &#125;
            </div>
        </div>
        <!-- <div class="empty_line"></div>
        <div class="empty_line"></div> -->
        <div id="education_function">
            <div class="d-flex" style="height: 40px;">
                <div id="function">
                    education
                </div>
                <div id="export_defualt" class="space">
                    ()
                </div>
                <div id="export_defualt">
                    &#123;
                </div>
                <div class="d-flex flex-row" id="education_content">
                    <div id="export_defualt" class="space">
                        return
                    </div>
                    <div id="class" class="space">
                        [
                    </div>
                    <div id="entity" class="space">
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
                    <div id="entity" class="space">
                        &#125;
                    </div>
                    <div id="class">
                        ]
                    </div>
                </div>
            </div>
            <!-- END OF EDUCATION '}' -->
            <div id="export_defualt">
                &#125;
            </div>
        </div>
        <div id="work_function">
            <div class="d-flex" style="height: 40px;">
                <div id="function">
                    workExperience
                </div>
                <div id="export_defualt" class="space">
                    ()
                </div>
                <div id="export_defualt">
                    &#123;
                </div>
                <div class="d-flex flex-row" id="work_content">
                    <div id="export_defualt" class="space">
                        return
                    </div>
                    <div id="class" class="space">
                        [
                    </div>
                    <div id="entity" class="space">
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
                    <div id="entity" class="space">
                        &#125;
                    </div>
                    <div id="class">
                        ]
                    </div>
                </div>
            </div>
            <!-- END OF WORK '}' -->
            <div id="export_defualt">
                &#125;
            </div>
        </div>
    </div>
    <!-- END OF CLASS '}'-->
    <div id="entity">
        &#125;
    </div>
</div>

<style>
    #about_container {
        /* transform: translateY(-5px); */
    }

    #export_defualt {
        color: #b87db6;
    }

    #class {
        color: #5296cb;
    }

    #class_name {
        color: #49c0aa;
    }

    #identifier {
        color: #93ceed;
    }

    #entity {
        color: #e7c30d
    }
    
    #string {
        color: #c48e76;
    }

    #function {
        color: #cecea1;
    }

    .space{
        margin-right: 4px;
    }

    .empty_line {
        margin-top: 20px;
        margin-left: 35px;
        position: absolute;
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
        margin-top: 20px;
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
        margin-top: 20px;
        margin-left: 35px;
        margin-top: 200px;
        width: 100%;
        position: absolute;
    }

    #work_content {
        margin-top: 20px;
        margin-left: 35px;
        position: absolute;
    }
</style>