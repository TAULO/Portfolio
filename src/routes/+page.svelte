<script>
    import CodeLine from "../components/CodeLine.svelte";
    import CodeTag from "../components/CodeTag.svelte";
    import About from "../components/About.svelte";
    import EmptyLine from "../components/EmptyLine.svelte";
    import Comment from "../components/Comment.svelte";
    import OnClick from "../components/OnClick.svelte";
    import Stack from "../components/Stack.svelte";
    import Icon from "../components/Service.svelte";
</script>

<div class="container-fluid">   
    <header class="route py-3">
        src > routes > index.js
    </header>	
    <div class="mb-2" style="color: #9e9e9e;">
        Thomas Taulo, 1 second ago | 1 author (Thomas Taulo)
    </div>     
    <div class="d-flex">  

        <CodeLine />

        <div class="d-flex flex-column ms-4 color_transition">
            <Comment comment="about me"/>
            <CodeTag tagName="script" --tag-color=#5296cb>
                <slot>
                    <About/>
                </slot>
            </CodeTag>

            <EmptyLine/>

            <Comment comment="school projects"/>
            <CodeTag tagName="Project" projectNameProp="Vending Macine" --tag-color=#49c0aa>
                <slot>
                    <Comment comment="click to view this project"/>
                    <OnClick/>
                </slot>
            </CodeTag>

            <EmptyLine/>
            
            <CodeTag tagName="Project" projectNameProp="Task Mining" --tag-color=#49c0aa>
                <slot>
                    <Comment comment="my final exam project for the computer science education program"/>
                    <Comment comment="the project involved developing a software-related product for the company where I completed a 6-month internship"/>
                    <EmptyLine/>
                    <Comment comment="click to view this project"/>
                    <OnClick/>
                    <EmptyLine/>
                    <Comment comment="the tech stack"/>
                    <CodeTag tagName="Stack">
                        <slot>
                            <Icon name="React"/>
                            <Icon name="ASP.NET RESTful API"/>
                            <i class="bi bi-0-circle" style="color: green;"></i>
                        </slot>
                    </CodeTag>
                </slot>
            </CodeTag>
            
            <EmptyLine/>

            <Comment comment="work projects"/>
            <CodeTag tagName="Project" --tag-color=#49c0aa>
                <slot>
                    <Comment comment="TODO"/>
                </slot>
            </CodeTag>

            <EmptyLine/>
            
            <Comment comment="hobby / personal projects"/>
            <CodeTag tagName="Project" projectNameProp="ringe-og-omegns-biavlerforening.dk" --tag-color=#49c0aa>
                <slot>
                    <OnClick/>
                </slot>
            </CodeTag>

            <EmptyLine/>

            <CodeTag tagName="Project" projectNameProp="ATaulo.dk" --tag-color=#49c0aa>
                <slot>
                    <OnClick/>
                </slot>
            </CodeTag>
        </div>
    </div>
</div>

<style>
    .color_transition {
        color: blue;
    /* Add any styles you want for the container here */
  }

  .color_transition * {
    transition: color 0.6s ease, background-color 0.3s ease; /* Add transition for color and background-color */
  }

  .color_transition:hover * {
    color: green; /* New text color on hover */
    background-color: yellow; /* New background color on hover */
    /* Add any other style changes for hover state */
  }
</style>