<script>
    import {v4 as uuidv4} from 'uuid'
    import {TextStore} from '../store/Store'
    let text;
    let disabled=true

    function handleInput(){
      if(text){
        const newText={
            id:uuidv4(),
            text:text,
        }
          TextStore.update((values)=>{
            return [newText,...values]
        })
      }
    }

</script>
<div class="text-input-sec">
    <input type="text" placeholder="Paste Here" bind:value={text}/>
    <button on:click={handleInput}>Board It</button>
</div>
<style>
    .text-input-sec{
        width: 95%;
        height: 35%;
        border-radius: 10px;
        background-color:'';
        display: flex;
        flex-direction: column;
        justify-content:flex-start;
        align-items: center;
    }

    .text-input-sec>input{
        height: 60%;
        width: 77%;
        border-radius: 10px;
        text-align: center;
        background-color: #353839;
        color: white;
    }

    .text-input-sec>button{
        margin: 5px 0px;
        width:77%;
        height: 40px;
        border-radius: 10px;
        background-color: darkorange;
    }

    @media (max-width:600px){
        .text-input-sec{
            justify-content: center;
        }
    }
</style>