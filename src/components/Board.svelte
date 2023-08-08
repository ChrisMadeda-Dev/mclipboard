<script>
import {
    TextStore
} from '../store/Store.js'
  import TextCont from './TextCont.svelte';
</script>

<div class="board">
    {#each $TextStore as text (text.id)}
    <TextCont {text}/>

    {/each}

</div>

<style>
.board {
    width: 97%;
    height: 60%;
    border-radius: 10px;
    background-color: '';
    border: .5px solid #353839;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    padding: 20px 0px;
    margin: 10px;
    overflow-x: hidden;
    overflow-y: auto;
}
</style>
