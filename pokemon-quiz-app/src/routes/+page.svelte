<script>
  let data = {};
  const async function fetchAPI() {
    const res = await fetch('https://graphqlpokemon.favware.tech/v8', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify({
        query: `
          {
            getPokemon(pokemon: dragonite) {
                sprite
                num
                species
                color
            }
          }
        `
      })
    })
    
    data = res.json();
  } fetchAPI();
</script>


<div>hello</div>