<script>
import Board from "./Board.svelte";
import TextInput from "./TextInput.svelte";
</script>

<main class="main-cont">
    <TextInput/>
        <Board/>
            </main>

<style>
.main-cont {
    width: 60%;
    height: 85vh;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
}

@media (max-width:600px) {
    .main-cont {
        width: 97%;
        height: 100vh;
    }
}
</style>
