<script>
    export let text = "Click Me!"
</script>

<div class="d-flex"> 
    <div id="entity">
        &lt;
    </div>
    <div id="class"> 
        button
    </div>
    <div id="identifier" style="margin-left: 4px;">
        onclick
    </div>
    <div>
        =
    </div>
    <div id="string">
        "
    </div>
    <div id="function">
        viewProject()
    </div>
    <div id="string">
        "
    </div>
    <div id="entity">
        &gt;
    </div>
    <div class="function_hover">
        {text}
    </div>
    <div id="entity">
        &lt;/
    </div>
    <div id="class">
        button
    </div>
    <div id="entity">
        &gt;
    </div>
</div>

<style>
    .function_hover {
    display: inline-block;
    position: relative;
  }

  .function_hover::before {
    content: "";
    position: absolute;
    left: 50%; /* Position the pseudo-element at the middle */
    transform: translateX(-50%); /* Center it horizontally */
    bottom: 0;
    width: 0;
    height: 2px;
    background-color: green;
    transition: width 0.5s ease; /* Transition for growing underline */
    margin-bottom: -5px;
  }

  .function_hover:hover {
    cursor: pointer;
  }

  .function_hover:hover::before {
    width: 100%;
  }
</style>