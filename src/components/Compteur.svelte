<script>
  export let title = "Compteur";
  export let header = "Compteur";

  let count = 0;

  const cptInc = () => {
    count++;
  };

  const cptDec = () => {
    count--;
  };
</script>

<h1>{title}</h1>
<h1>{header}</h1>
<button on:click={cptDec}> - </button>

<span> {count} </span>

<button on:click={cptInc}> + </button>
