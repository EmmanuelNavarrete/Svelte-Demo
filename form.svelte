<script>
  const movies = [
    {
      name: "Terminator",
      boletos: 0,
      available: 5
    },
    {
      name: "La catrina",
      boletos: 0,
      available: 2
    }
  ];
</script>

{#each movies as movie}

<form>
	<h3>{movie.name}</h3>
	<button type="button" disabled={movie.boletos <= 0} on:click = {()=> movie.boletos -=1}>
  -
  </button>
	{movie.boletos}
	<button type="button" disabled={movie.boletos >= movie.available} on:click = {()=> movie.boletos +=1}>
  +
  </button>
</form>
{/each}