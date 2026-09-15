# ArrayListJs

## Para todos os tipos utilizarei a seguinte lista:

```
const jogos = [
  {nome: 'Hunt: Showdown 1896', preco: 89, estilo: 'FPS Extraction'},
  {nome: 'Valhein', preco: 60, estilo: 'Survival'},
  {nome: 'Minecraft', preco: 100, estilo: 'Sandbox/Survival'},
  {nome: 'Subnautica 2', preco: 120, estilo: 'Survival'}
];
```

## .map
Ele consegue percorrer por toda lista e manipular cada item, retornando uma nova lista de igual quantidade da lista original

# Exemplo:

```
const nomeEpreco = jogos.map(({ nome, preco }) => ({ nome, preco }));
console.log(nomeEpreco);

```
Nesse exemplo foi passado uma desestruturação dentro dos parâmetros (função callback) do .map para extrair apenas o nome e preço e armazena-los dentro de nomeEpreco.

## .filter
Ele irá filtrar (com base em sua preferência) toda a lista original e retornará uma nova lista com igual ou menor quantidade

# Exemplo:

```
const precoMaior = jogos.filter(jogo => preco > 65);
console.log(precoMaior)
```
Neste exemplo foi passado um filtro (função callback) para retornar apenas jogos que possuem valores maiores que 65 em sua variável preco.

## .reduce
Diferentemente dos .map e .filter, o reduce retornará apenas um único item

# Exemplo:

```
const somaPrecos = jogos.reduce((accumulator, produto) => { return accumulator + produto.preco;}, 0);
console.log(somaPrecos);
```
