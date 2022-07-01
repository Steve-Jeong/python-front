<script>
  let inputVar1=''
  let inputVar2=''
  let inputVar3=''

  $: output = inputVar1 + inputVar2 + inputVar3;

  const handleSubmit = () => {
    window.open(output, '_blank').focus();
  }
</script>

<main>
  <h1>Python 입력 Frontend</h1>
  <div class="inputFrame">
    <h2>입력</h2>
    <div>
      <label for="inputVar1">입력변수 1</label>
      <input 
        name="inputVar1" 
        type="text" 
        placeholder="type here ..." 
        bind:value={inputVar1}
      />
    </div>
    <div>
      <label for="inputVar2">입력변수 2</label>
      <input 
        name="inputVar2" 
        type="text" 
        placeholder="type here ..." 
        bind:value={inputVar2}
      />
    </div>
    <div>
      <label for="inputVar3">입력변수 3</label>
      <input 
        name="inputVar3" 
        type="text" 
        placeholder="type here ..." 
        bind:value={inputVar3}
      />
    </div>
  </div>
  <div class="outputFrame">
    <h2>출력</h2>
    <p>{output}</p>
    <div>
      <button on:click={handleSubmit}>제출</button>
    </div>
  </div>
</main>

<style>
</style>
