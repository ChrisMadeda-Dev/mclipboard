<script>
export let text;
</script>

<div class="text-cont">
<p>{text.text}</p>
</div>

<style>
    .text-cont{
        width: 95%;
        min-height: 50px;
        max-height: auto;
        flex: 0 0 auto;
        margin: 5px 0px;
        border-radius: 100px;
        background-color: #353839;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .text-cont>p{
        font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
        font-size: 15px;
        color: white;
    }
</style>