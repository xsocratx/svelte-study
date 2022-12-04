<script>
    let m = {x:0, y:0};

    function handleMouseMove(event){
        m.x = event.clientX;
        m.y = event.clientY;
    }
</script>
<style>
    div {
        width: 50%;
        height: 50%;
        border-color: black;
        border: 1px;
    }
</style>

<div on:mousemove={handleMouseMove}>
    The mouse position is {m.x} x {m.y}
</div>