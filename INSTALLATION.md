# 🚀 Guia de Instalação e Execução

## ⚡ Quick Start (Início Rápido)

### Opção 1: Abrir Diretamente no Navegador
1. Navegue até a pasta do projeto
2. Clique duas vezes em `index.html`
3. Seu navegador padrão abrirá automaticamente

**✅ Pronto! O projeto está funcionando!**

---

## 🖥️ Opção 2: Usando um Servidor Local

### 📦 Com XAMPP (Recomendado)

#### Windows:
1. **Instale o XAMPP** (https://www.apachefriends.org)
2. **Coloque o projeto** em `C:\xampp\htdocs\Pokedex`
3. **Inicie o Apache** no painel de controle do XAMPP
4. **Acesse no navegador:**
   ```
   http://localhost/Pokedex/
   ```

#### Mac/Linux:
1. **Instale o XAMPP** para seu sistema
2. **Copie o projeto** para `/Applications/XAMPP/htdocs/Pokedex`
3. **Inicie o Apache**
4. **Acesse:**
   ```
   http://localhost/Pokedex/
   ```

---

### 🐍 Com Python (Sem Instalação Adicional)

#### Python 3.x:
```bash
# Navigate to project directory
cd /caminho/para/Pokedex

# Iniciar servidor na porta 8000
python -m http.server 8000

# Acessar no navegador
# http://localhost:8000
```

#### Python 2.x (Legado):
```bash
python -m SimpleHTTPServer 8000
```

---

### 🟢 Com Node.js

#### Usando http-server:
```bash
# Instalar globalmente (uma única vez)
npm install -g http-server

# No diretório do projeto
http-server

# Ou especificar porta
http-server -p 8080
```

---

### 🎯 Com Live Server (VS Code)

1. **Instale a extensão** "Live Server" no VS Code
2. **Clique direito** em `index.html`
3. **Selecione** "Open with Live Server"
4. **Seu navegador abrirá automaticamente**

---

## 📋 Pré-requisitos

| Requisito | Versão Mínima | Tipo |
|---|---|---|
| Navegador Web | Qualquer moderno | Obrigatório |
| JavaScript | ES6+ | Obrigatório |
| Conexão Internet | Qualquer uma | Obrigatório (para PokeAPI) |
| Node.js | 12+ | Opcional |
| Python | 2.7+ ou 3.5+ | Opcional |
| XAMPP | Qualquer versão | Opcional |

---

## 🌐 Navegadores Suportados

| Navegador | Versão Mínima | Status |
|---|---|---|
| Chrome | 90+ | ✅ Totalmente Suportado |
| Firefox | 88+ | ✅ Totalmente Suportado |
| Safari | 14+ | ✅ Totalmente Suportado |
| Edge | 90+ | ✅ Totalmente Suportado |
| Opera | 76+ | ✅ Totalmente Suportado |
| Internet Explorer | - | ❌ Não Suportado |

---

## 🎮 Primeiro Uso

### 1️⃣ Página Inicial
Ao abrir o projeto:
- Você verá a interface da Pokedex clássica
- Por padrão, o Pokémon #1 (Bulbassauro) é exibido
- A música tema pode estar tocando

### 2️⃣ Sua Primeira Busca
```
Exemplos para testar:
- Digite: pikachu
- Digite: 25 (ID do Pikachu)
- Digite: charizard
- Digite: 6 (ID do Charizard)
```

### 3️⃣ Explore as Funcionalidades
- 🎵 Clique no ícone de música para controlar a trilha
- ⬅️➡️ Use os botões Prev/Next para navegar
- 🎭 Digite "wellington" para o easter egg
- 🎭 Caso veja um "?" no cursor, não exite em clicar! 

---

## 🔧 Configuração Adicional

### Mudando o Pokémon Padrão
No arquivo `script.js`, procure por:
```javascript
let searchPokemon = '1';  // Mude o número aqui
```

Altere o número `'1'` para qualquer ID de Pokémon válido (1-1025).

### Desativando Música na Inicialização
No arquivo `script.js`, procure por:
```javascript
// Descomente para desativar música ao carregar
// myMusic.pause();
```

---

## 📊 Estrutura de Pastas Esperada

```
Pokedex/
├── index.html              ← Arquivo principal
├── README.md               ← Documentação
├── INSTALLATION.md         ← Este arquivo
│
├── css/
│   └── style.css
│
├── js/
│   └── script.js
│
├── Images/
│   ├── cursor/
│   ├── Icons/
│   ├── types/
│   ├── pokedex.png
│   ├── pokedex_2.png
│   ├── fundo.gif
│   ├── bush.png
│   ├── memberRocket.png
│   └── wellGif.gif
│
├── Songs/
│   ├── musictheme.mp3
│   └── jigglypuffSong.mp3
│
└── Favicons/
    ├── favicon-16x16.png
    ├── favicon-32x32.png
    └── ...
```

Se uma pasta ou arquivo estiver faltando, o projeto pode não funcionar corretamente!

---

## 🚨 Erros Comuns

### ❌ Erro: "Cannot GET /index.html"
**Causa:** Tentando abrir via `file://` sem servidor
**Solução:** Use um servidor local (XAMPP, Python, Node.js)

### ❌ Erro: "CORS Error"
**Causa:** Arquivo aberto diretamente sem servidor
**Solução:** Use um servidor HTTP local

### ❌ Aviso: "Mixed Content"
**Causa:** Páginas HTTPS tentando carregar recursos HTTP
**Solução:** Use HTTPS ou servidor local

### ❌ Imagens não carregam
**Causa:** Caminho de pasta incorreto ou arquivo faltando
**Solução:** Verifique estrutura de pastas acima

---

## 🔐 Segurança

✅ **Seguro para usar:**
- Nenhum dado pessoal é coletado
- Sem rastreamento
- Sem cookies desnecessários
- Apenas lê dados da PokeAPI pública

---

## 📚 Próximos Passos

Após instalação bem-sucedida:

1. **Explore a Interface** - Teste todas as funcionalidades
2. **Leia a Documentação** - Entenda como funciona
3. **Customize** - Modifique cores, sons, fontes
4. **Compartilhe** - Mostre seu projeto!

---

## 💬 Precisa de Ajuda?

- 📖 Veja [README.md](README.md) para visão geral
- 🆘 Veja [TROUBLESHOOTING.md](TROUBLESHOOTING.md) para problemas
- 🎨 Veja [FEATURES.md](FEATURES.md) para recursos
- 📧 Contate o desenvolvedor no LinkedIn

---

## ✅ Checklist de Instalação

```
[ ] Navegador web instalado
[ ] Projeto baixado/clonado
[ ] Todas as pastas estão presentes
[ ] Arquivos de mídia (Songs/, Images/) existem
[ ] Acessou o projeto via servidor local ou navegador
[ ] Página carrega sem erros de console
[ ] Consegue buscar um Pokémon
[ ] Música toca ao clicar no ícone
[ ] Easter egg "wellington" funciona
```

Se todos os itens estão marcados, você está pronto! 🎉

---

<div align="center">

### 🎮 Divirta-se! Bem-vindo à Pokedex! 🎮

</div>
