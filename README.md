# solid-waffle
# solid-waffle
**My name !s Gl!CH** 
![this is img](https://miro.medium.com/v2/resize:fit:1400/1*M33XmTqDutH1SBdxxp7zQQ.jpeg)
**I'm javascript developer.***There is Example of my code:*
```javascript
function draw(pokemon){
    section.innerHTML = '';
    hideBtn()
    const pokemonCont = document.createElement('div');
    pokemonCont.setAttribute('class', 'pokemon');
    pokemonCont.innerHTML = `
        <p>ID: #${pokemon.id}</p>
        <hr>
        <h1 class="name">${pokemon.name}</h1>
        <img src="${pokemon.sprites.front_default}">
        <h2>TYPE</h2>
    `
    const typeCont = document.createElement('div');
    typeCont.setAttribute('class', 'types');
    let types = pokemon.types;
    for(let i = 0; i < types.length; i++){
        const typeElement = document.createElement('p');
        typeElement.textContent = types[i].type.name;
        typeCont.appendChild(typeElement);
    }
    pokemonCont.appendChild(typeCont);  //   1
    const itemTitle = document.createElement('h2');
    itemTitle.textContent = 'ITEMS';
    pokemonCont.appendChild(itemTitle);
    const items = pokemon.held_items;
    const itemsBox = document.createElement('div');
    itemsBox.setAttribute("class", 'items');
    for(let j = 0; j < items.length; j++){
        fetch(items[j].item.url)
            .then(async function(response){
                let itemInfo = await response.json();
                itemsBox.innerHTML += `
                    <div>
                        <p>${items[j].item.name}</p>
                        <img src='${itemInfo.sprites.default}'>
                    </div>
                `
                pokemonCont.appendChild(itemsBox);  //  2
            })
    }
    section.appendChild(pokemonCont);
    
    const back = document.createElement('p');
    back.textContent = '❌';
    back.setAttribute('class', 'btnBack');
    back.setAttribute('onclick', `pokemonList('${startURL}')`);
    section.appendChild(back);
}
```
This is Unordered list:
* [Cyberpunk 2077](https://store.steampowered.com/app/1091500/Cyberpunk_2077/)
* [Ведьмак 3: Дикая Охота](https://store.steampowered.com/app/292030/Vedmak_3_Dikaya_Oxota/?l=russian)
* [Rust](https://store.steampowered.com/app/252490/Rust/)
