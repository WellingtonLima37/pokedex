# 🎮 Pokedex Interativa

> Uma Pokedex web interativa e animada, com design retro inspirado nos anos 90! Busque informações de qualquer Pokémon usando a PokeAPI e explore suas estatísticas.

---

## 🌟 Destaques do Projeto

✨ **Funcionalidades Principais:**
- 🔍 Busca de Pokémon por nome ou número
- 📊 Exibição de estatísticas completas (HP, Ataque, Defesa, Peso)
- 🎵 Trilha sonora temática do Pokémon
- ✨ Animações e efeitos visuais retro
- 🎨 Design responsivo inspirado na Pokedex clássica
- 🎭 Easter egg especial (tente digitar "wellington")
- 🖼️ Imagens dinâmicas dos Pokémon da PokeAPI

---

## 🎯 Demonstração

| Funcionalidade | Descrição |
|---|---|
| 🔍 **Busca Inteligente** | Procure por nome ou ID do Pokémon |
| ⬅️➡️ **Navegação** | Botões Prev/Next para navegar entre Pokémon |
| 🏷️ **Tipos** | Visualize o tipo(s) do Pokémon com cores temáticas |
| 📈 **Estatísticas** | Veja CP, HP, Ataque, Defesa e Peso |
| 🎪 **Easter Egg** | Procure por "wellington" para uma surpresa! |

---

## 📁 Estrutura do Projeto

```
Pokedex/
│
├── 📄 index.html           # Arquivo principal HTML
├── 📄 README.md            # Este arquivo
│
├── 📁 css/
│   └── style.css           # Estilos e animações (CSS puro)
│
├── 📁 js/
│   └── script.js           # Lógica JavaScript e integração com PokeAPI
│
├── 📁 Images/
│   ├── cursor/             # Cursores customizados
│   ├── Icons/              # Ícones (música, etc)
│   ├── types/              # Ícones dos tipos de Pokémon
│   ├── pokedex.png         # Imagem da Pokedex
│   ├── pokedex_2.png       # Imagem da Pokedex (lado direito)
│   ├── fundo.gif           # Fundo animado
│   ├── bush.png            # Efeito visual
│   └── memberRocket.png    # Membro do Time Rocket
│
├── 📁 Favicons/            # Ícones do site
│
└── 📁 Songs/
    ├── musictheme.mp3      # Trilha sonora principal
    └── jigglypuffSong.mp3  # Som especial do Jigglypuff

```

---

## 🚀 Como Usar

### 1️⃣ **Abra o Projeto**
- Abra o arquivo `index.html` em seu navegador favorito
- Ou coloque em um servidor local (XAMPP, Live Server, etc)

### 2️⃣ **Busque um Pokémon**
- Digite o **nome** ou **número** do Pokémon na barra de pesquisa
- Pressione Enter ou clique em outro lugar

### 3️⃣ **Navegue Entre Pokémons**
- Use os botões **< Prev** e **Next >** para navegar
- Você pode também editar o número na barra de pesquisa

### 4️⃣ **Controle de Música** 🎵
- Clique no ícone de música no canto superior direito para:
  - ▶️ Ativar/Desativar a trilha sonora
  - 🎼 Controlar a música temática

### 5️⃣ **Easter Egg Secreto** 🎭
- Digite **"wellington"** na barra de pesquisa
- Veja as informações especiais do desenvolvedor!
- Apareça os ícones de LinkedIn e GitHub

---

## 🛠️ Tecnologias Utilizadas

```
┌─────────────────────────────────────────────────┐
│          TECNOLOGIAS E FERRAMENTAS             │
├─────────────────────────────────────────────────┤
│ 🎨 HTML5                   - Estrutura         │
│ 🎭 CSS3                    - Estilos & Anim.   │
│ ⚙️  JavaScript ES6          - Funcionalidades   │
│ 🌐 PokeAPI                 - Dados dos Pokémon │
│ 🖼️  Google Fonts            - Tipografia        │
│ 🎵 Audio API               - Controle de Som   │
└─────────────────────────────────────────────────┘
```

### Dependências:
- **PokeAPI** (https://pokeapi.co/) - API pública e gratuita
- **Google Fonts** - Fontes "VT323", "Caveat", "Oxanium"
- Nenhuma dependência de bibliotecas externas!

---

## 🎨 Características Visuais

### 🎭 Design Retro
- Interface inspirada na Pokedex clássica do Game Boy
- Animações com efeito "flicker" de lâmpadas
- Cursor customizado em toda a página
- Fundo animado com tema Pokémon

### 🌈 Sistema de Tipos com Cores
Cada tipo de Pokémon possui uma cor temática:
- 🔥 Fire (Fogo) - Vermelho
- 💧 Water (Água) - Azul
- 🌿 Grass (Grama) - Verde
- ⚡ Electric (Elétrico) - Amarelo
- ❄️ Ice (Gelo) - Ciano
- ... E mais 14 tipos!

### 🎬 Efeitos Especiais
- 👻 Overlay semitransparente
- 🎪 Animações de Jigglypuff
- 🎭 Team Rocket aparecendo e desaparecendo
- ✨ Transições suaves entre Pokémons

---

## 📊 Estatísticas Exibidas

Cada Pokémon mostra as seguintes informações:

| Estatística | Descrição | Símbolo |
|---|---|---|
| **Número** | ID único do Pokémon | # |
| **Nome** | Nome do Pokémon | 📛 |
| **HP** | Pontos de Vida | ❤️ |
| **Attack** | Poder de Ataque | ⚔️ |
| **Defense** | Poder de Defesa | 🛡️ |
| **Weight** | Peso em kg | ⚖️ |
| **CP** | Pontos de Combate | 🎯 |
| **Type** | Tipo(s) do Pokémon | 🏷️ |
| **Abilities** | Habilidades especiais | ✨ |

---

## 🔧 Como o JavaScript Funciona

### 🔌 Conexão com a API
```javascript
const fetchPokemon = async (pokemon) => {
    const APIResponse = await fetch(
        `https://pokeapi.co/api/v2/pokemon/${pokemon}`
    );
    
    if(APIResponse.status === 200){
        const data = await APIResponse.json();
        return data;
    }
};
```

### 🎯 Renderização Dinâmica
- Busca dados da PokeAPI
- Atualiza elementos HTML com as informações
- Muda cores de acordo com o tipo
- Exibe a imagem do Pokémon

### 🎭 Easter Egg
Quando digita "wellington", o código detecta e exibe:
- Dados pessoais do desenvolvedor
- Links para LinkedIn e GitHub
- Foto customizada
- Tipos especiais (Linkedin e Github)

---

## 📱 Responsividade

O projeto foi desenvolvido para funcionar em:
- ✅ Computadores Desktop
- ✅ Tablets
- ✅ Dispositivos Móveis

Usa `viewport` meta tag e CSS responsivo com `clamp()` para dimensionamento flexível!

---

## 🎵 Áudio

O projeto inclui dois arquivos de áudio:

1. **musictheme.mp3** 🎼
   - Trilha sonora temática do Pokémon
   - Toca continuamente quando ativada
   - Toggle com ícone de música

2. **jigglypuffSong.mp3** 🎤
   - Som associado ao Jigglypuff
   - Toca quando o easter egg está ativo

---

## 🌐 API de Dados

### PokeAPI
- **URL Base:** `https://pokeapi.co/api/v2/pokemon/`
- **Método:** GET
- **Autenticação:** Não necessária
- **Rate Limit:** ✅ Generoso

### Exemplos de Requisição:
```
GET https://pokeapi.co/api/v2/pokemon/1         → Bulbassauro
GET https://pokeapi.co/api/v2/pokemon/pikachu   → Pikachu
GET https://pokeapi.co/api/v2/pokemon/charizard → Charizard
```

---

## 🎓 Aprendizados Principais

Este projeto demonstra:

1. **📡 Fetch API & Async/Await**
   - Comunicação com APIs externas
   - Tratamento de respostas assíncronas

2. **🎨 CSS Avançado**
   - Animações complexas
   - Layout responsivo com CSS Grid/Flexbox
   - Efeitos visuais com filtros e transformações

3. **⚙️ JavaScript Moderno**
   - Seletores de DOM
   - Event Listeners
   - Manipulação dinâmica de HTML

4. **🎭 UX/UI**
   - Design intuitivo
   - Feedback visual ao usuário
   - Acessibilidade básica

---

## 🐛 Troubleshooting

### ❓ "A busca não funciona"
- Verifique sua conexão com a internet (precisa acessar PokeAPI)
- Tente refresh da página
- Confirme que o nome/número está correto

### 🔇 "A música não toca"
- Verificar se o navegador permite áudio
- Clicar primeiro na página (alguns navegadores exigem interação do usuário)
- Checar se os arquivos `.mp3` estão na pasta `/Songs`

### 🖼️ "Imagens não carregam"
- Verificar conexão com internet (PokeAPI)
- Estrutura de pastas está correta?
- Limpar cache do navegador

### 🎯 "Easter egg não funciona"
- Digitou exatamente "wellington"?
- Verificar o console para erros
- Recarregar a página

---

## 👨‍💻 Desenvolvedor

Criado por **Wellington Lima** 👨‍💼

- 🔗 [LinkedIn](https://www.linkedin.com/in/wellingtonlima37/)
- 🐙 [GitHub](https://github.com/WelIingtonLima)

---

## 📝 Licença

Este projeto é **livre para usar, modificar e distribuir**.
Creditos ao desenvolvedor e à PokeAPI serão apreciados! 🙏

---

## 🎉 Agradecimentos

- 🎮 **Pokémon** - Criadores do universo Pokémon
- 🌐 **PokeAPI** - Pela excelente API pública
- 🎨 **Google Fonts** - Pelas fontes incríveis
- ❤️ **Você** - Por usar e apreciar este projeto!

---

## 🔗 Links Úteis

- [PokeAPI Documentação](https://pokeapi.co/)
- [MDN - Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
- [CSS Animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations)
- [JavaScript Async/Await](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Promises)

---

<div align="center">

### ⭐ Se gostou, deixe uma estrela! ⭐

**Divirta-se capturando Pokémons!** 🎮✨

</div>
