# 🆘 Guia de Solução de Problemas

> Se algo não está funcionando, você provavelmente encontrará a solução aqui! 🔧

---

## 🔍 Busca Rápida de Problemas

- [A busca não funciona](#-a-busca-não-funciona)
- [A música não toca](#-a-música-não-toca)
- [Imagens não carregam](#-imagens-não-carregam)
- [Página em branco](#-página-em-branco)
- [Easter egg não funciona](#-easter-egg-não-funciona)
- [Erros no Console](#-erros-no-console)
- [Problema não listado](#-problema-não-listado)

---

## 🔧 Problemas e Soluções

### 🔍 A busca não funciona

#### ❌ Sintoma
Você digita um nome/número e nada acontece

#### 🔍 Causas Possíveis

| Causa | Indicador | Solução |
|---|---|---|
| Sem conexão internet | Página carrega vazia | Conecte-se ao WiFi/Internet |
| Pokémon não existe | Carrega "loading...💾" e desaparece | Verificar nome/número |
| Erro de sintaxe | Vê erro no console | F12 → Console → veja erro |
| Servidor não rodando | URL começa com `file://` | Use servidor local (XAMPP, Python, etc) |

#### ✅ Passo-a-Passo

**Passo 1: Verificar Internet**
```
Teste em: https://www.google.com
✓ Se carrega → Internet OK
✗ Se não carrega → Conecte-se ao WiFi
```

**Passo 2: Verificar Pokémon**
```
Nomes válidos:
- pikachu ✓
- charizard ✓
- pikapika ✗ (não existe)
- thunderbolt ✗ (é um movimento, não Pokémon)
```

**Passo 3: Verificar Console**
```
1. Pressione F12
2. Vá na aba "Console"
3. Procure mensagens vermelhas de erro
4. Copie a mensagem completa
```

**Passo 4: Recarregar Página**
```
Técnicas de reload:
- Clique normal: F5 ou Ctrl+R
- Hard refresh: Ctrl+Shift+R (limpa cache)
- Novo abas: Ctrl+T → copie URL
```

#### 🎯 Se Ainda Não Funcionar
1. Teste com número: digite `1` e pressione Enter
2. Se funciona → problema com busca por nome
3. Se não funciona → problema maior

---

### 🎵 A música não toca

#### ❌ Sintoma
Clica no ícone 🎵 mas a música não soa

#### 🔍 Causas Possíveis

| Causa | Indicador | Solução |
|---|---|---|
| Som mudo do navegador | Ícone 🔇 na abeta do navegador | Clique no ícone para desmutar |
| Volume do sistema = 0 | Controle de volume do Windows | Aumente volume |
| Arquivo faltando | Erro no console | Verifique pasta Songs/ |
| Navegador não permite | Chrome/Firefox novo | Clique na página primeiro, depois na música |

#### ✅ Passo-a-Passo

**Passo 1: Verificar Volume**
```
Windows:
1. Clique no ícone de volume (canto inferior direito)
2. Verifique se está em 0
3. Aumente para 50% ou mais
```

**Passo 2: Verificar Som do Navegador**
```
1. Procure o ícone 🔇 na abeta do navegador
2. Se estiver com X → clique para desmutar
3. Tente a música novamente
```

**Passo 3: Verificar Arquivo**
```
1. Abra a pasta do projeto
2. Vá em: Pokedex → Songs
3. Verifique se existem:
   ✓ musictheme.mp3
   ✓ jigglypuffSong.mp3
4. Se faltam → baixe ou redownload do projeto
```

**Passo 4: Autorizar Áudio**
```
Alguns navegadores exigem interação do usuário:
1. Clique em algum lugar da página Pokémon
2. Depois clique no ícone de música
3. O áudio deve funcionar agora
```

**Passo 5: Verificar Formato**
```
Formatos suportados: MP3, WAV, OGG
MP3 é o mais compatível.
Se arquivo é .wav ou .ogg, converta para .mp3
```

#### 🎯 Teste de Som

```javascript
// Abra o console (F12 → Console)
// Cole este código:
const audio = document.getElementById('myMusic');
console.log('Volume:', audio.volume);
console.log('Muted:', audio.muted);
console.log('Src:', audio.src);
audio.play();
```

---

### 🖼️ Imagens não carregam

#### ❌ Sintoma
Vê "não carrega imagem" ou imagem quebrada ❌

#### 🔍 Causas Possíveis

| Tipo | Causa | Solução |
|---|---|---|
| **Imagens do Pokémon** | Sem internet/PokeAPI down | Verifique internet, aguarde |
| **Imagens locais** | Arquivo faltando | Verifique pasta Images/ |
| **Favicons** | Arquivo faltando | Verifique pasta Favicons/ |
| **Cursor** | Caminho incorreto | Verifique css/style.css |

#### ✅ Passo-a-Passo

**Para Imagens do Pokémon:**
```
Essas vêm da internet (PokeAPI)

1. Verifique internet:
   - Abra: https://pokeapi.co
   - Se carrega → PokeAPI funciona
   - Se não carrega → Internet problema

2. Tente outra busca:
   - ID 1 (Bulbassauro)
   - ID 25 (Pikachu)

3. Se funciona em uma mas não em outra:
   → Aquele Pokémon pode não ter imagem

4. Se nenhuma funciona:
   → Aguarde conexão melhorar
```

**Para Imagens Locais:**
```
1. Abra a pasta do projeto
2. Verificar estrutura:
   Pokedex/
   ├── Images/
   │   ├── cursor/          ← Necessário
   │   ├── Icons/           ← Necessário
   │   ├── types/           ← Necessário
   │   ├── pokedex.png      ← Necessário
   │   ├── pokedex_2.png    ← Necessário
   │   └── fundo.gif        ← Necessário

3. Se arquivo falta:
   - Redownload do GitHub
   - Ou procure arquivo online
```

**Para Favicons:**
```
1. Favicons são apenas decoração
2. Se faltar, afeta apenas o ícone da aba
3. Funcionalidade não é afetada
4. Não é crítico corrigir
```

**Para Cursor Customizado:**
```
1. Verificar arquivo: Images/cursor/left_ptr.png
2. Se faltar, usa cursor padrão (sem problema)
3. Verificar style.css linha com:
   cursor: url('../Images/cursor/left_ptr.png'), default;
```

#### 🔍 Verificar via Console

```javascript
// F12 → Console → Cole:
const img = new Image();
img.src = 'Images/pokedex.png';
img.onload = () => console.log('✓ Imagem carrega OK');
img.onerror = () => console.log('✗ Erro ao carregar');
```

---

### ⚪ Página em branco

#### ❌ Sintoma
Abre a página mas vê apenas branco/nada carrega

#### 🔍 Causas Possíveis

| Causa | Indicador | Solução |
|---|---|---|
| JavaScript desativado | Nenhum recurso funciona | Ativar JavaScript |
| Arquivo corrompido | Nenhuma página web carrega | Redownload do projeto |
| Navegador antigo | IE aparece em branco | Use Chrome/Firefox/Edge |
| Erro crítico JS | Ver erro em vermelho no console | Corrigir erro |

#### ✅ Passo-a-Passo

**Passo 1: Ativar JavaScript**
```
Chrome:
1. Menu (⋮) → Configurações
2. Privacidade e segurança → Configurações do site
3. JavaScript → Permitir

Firefox:
1. about:config na URL
2. Procure: javascript.enabled
3. Clique para true
```

**Passo 2: Verificar Arquivo HTML**
```
1. Abra index.html em editor de texto
2. Verifique se começa com: <!DOCTYPE html>
3. Se não → arquivo corrompido
4. Redownload do GitHub
```

**Passo 3: Abrir Console**
```
F12 → Console
Veja se há erros em vermelho:
- Se sim → mensagem de erro pode ajudar
- Se não → abra em outro navegador
```

**Passo 4: Tentar Outro Navegador**
```
Teste em:
✓ Chrome (recomendado)
✓ Firefox
✓ Edge
✗ Internet Explorer (não funciona)
```

---

### 🎭 Easter egg não funciona

#### ❌ Sintoma
Digita "wellington" e nada especial acontece

#### 🔍 Causas Possíveis

| Causa | Indicador | Solução |
|---|---|---|
| Digitou errado | Barra de busca diferentes | Digite exatamente "wellington" |
| Maiúsculas | Viu erro no console | Sistema é case-insensitive (OK) |
| Espaços extras | Campo de busca com espaços | Sem espaços antes/depois |
| JavaScript desativado | Funcionalidades não funcionam | Ativar JavaScript |

#### ✅ Passo-a-Passo

**Passo 1: Deletar e Redigitar**
```
1. Limpe o campo de busca
2. Clique uma vez no campo
3. Digite: wellington
4. Sem espaços antes ou depois
5. Pressione Enter
```

**Passo 2: Verificar Digitação**
```
Correto:      wellington
Incorreto:    Wellington (maiúsculas OK, mas tente minúsculas)
Incorreto:    wellngton (falta i)
Incorreto:    wellington  (espaço depois)
Incorreto:    -wellington (espaço antes)
```

**Passo 3: Refresh e Tentar Novamente**
```
1. Pressione F5 ou Ctrl+R
2. Aguarde carregar completamente
3. Digite "wellington"
4. Pressione Enter
```

**Passo 4: Verificar Arquivo JS**
```
1. Abra js/script.js
2. Procure por: if (inputValue === "wellington")
3. Se não encontrar → easter egg foi removido
4. Se encontrar → veja console para erros
```

---

### 💻 Erros no Console

#### ❌ Como Acessar Console
```
Navegadores:
Chrome/Edge:   Clique F12 → Console
Firefox:       Clique F12 → Console
Safari:        Cmd+Option+I → Console
```

#### 🔴 Erro Comum: "CORS Error"

**Sintoma:**
```
Access to XMLHttpRequest at 'https://...' has been blocked by CORS policy
```

**Causa:** Arquivo aberto como `file://`

**Solução:** Use servidor local
```bash
# Python 3
python -m http.server 8000

# Node.js
npx http-server

# XAMPP
Coloque em htdocs e acesse via http://localhost
```

#### 🔴 Erro: "Cannot find element"

**Sintoma:**
```
Uncaught TypeError: Cannot read property 'innerHTML' of null
```

**Causa:** HTML e JS não sincronizados

**Solução:**
1. Verifique se `index.html` tem todos os elementos
2. Verifique se `script.js` está correto
3. Redownload do GitHub

#### 🔴 Erro: "fetch failed"

**Sintoma:**
```
Failed to fetch: ...pokeapi.co/api/v2/pokemon/...
```

**Causa:** Sem conexão com internet

**Solução:**
1. Verifique conexão internet
2. Teste em https://pokeapi.co
3. Aguarde conexão melhorar

---

### 📋 Problema não listado?

#### 🔍 Diagnóstico Geral

**Passo 1: Coletar Informações**
```
Responda:
□ Qual é o erro que vê?
□ Que ação estava fazendo?
□ Em qual navegador?
□ Qual sistema operacional?
□ Tem internet funcionando?
```

**Passo 2: Verificar Console**
```
F12 → Console
Copie TODA mensagem de erro (vermelha)
```

**Passo 3: Tentar Soluções Básicas**
```
1. □ Refresh: Ctrl+Shift+R
2. □ Reabrir navegador
3. □ Tentar outro navegador
4. □ Redownload do projeto
5. □ Usar servidor local
```

**Passo 4: Procurar Ajuda**
```
1. Busque no Google: [erro exato]
2. Procure no Stack Overflow
3. Contate o desenvolvedor:
   - LinkedIn: https://www.linkedin.com/in/wellingtonlima37/
   - GitHub: https://github.com/WelIingtonLima
```

---

## 📊 Tabela de Compatibilidade

### Navegadores

| Navegador | Versão | Status | Notas |
|---|---|---|---|
| Chrome | 90+ | ✅ Funciona 100% | Recomendado |
| Firefox | 88+ | ✅ Funciona 100% | Ótima alternativa |
| Edge | 90+ | ✅ Funciona 100% | Chromium-based |
| Safari | 14+ | ✅ Funciona 100% | macOS/iOS |
| Opera | 76+ | ✅ Funciona 100% | Chromium-based |
| IE 11 | N/A | ❌ Não funciona | Descontinuado |

### Sistemas Operacionais

| SO | Versão | Status | Notas |
|---|---|---|---|
| Windows | 7+ | ✅ OK | Suportado |
| macOS | 10.12+ | ✅ OK | Suportado |
| Linux | Qualquer | ✅ OK | Suportado |
| iOS | 11+ | ⚠️ Limitado | Funciona, mas mobile |
| Android | 5+ | ⚠️ Limitado | Funciona, mas mobile |

---

## 🎯 Checklist de Troubleshooting

```
Antes de contatar desenvolvedor:

Internet:
□ Testou em https://www.google.com
□ Testou em https://pokeapi.co
□ Testou outro WiFi/Internet

Projeto:
□ Redownload do GitHub
□ Todos os arquivos presentes
□ Estrutura de pastas correta

Navegador:
□ Testou em Chrome
□ Testou em Firefox
□ JavaScript está ativado
□ Cache limpo (Ctrl+Shift+R)

Servidor:
□ Usando servidor local (XAMPP/Python/Node)
□ Não abrindo arquivo como file://
□ URL começa com http:// ou https://

Console:
□ Abri com F12
□ Verifiquei mensagens de erro
□ Copiei mensagem completa
```

---

## 📞 Contato e Suporte

Se após todos os passos acima o problema persiste:

**💬 Formas de Contato:**

1. 📧 **LinkedIn**
   - https://www.linkedin.com/in/wellingtonlima37/
   - Envie mensagem descrevendo o problema

2. 🐙 **GitHub Issues**
   - https://github.com/WelIingtonLima
   - Abra uma issue com detalhes

3. 💻 **Email**
   - Procure contato no GitHub do desenvolvedor

---

## 📚 Recursos Adicionais

Veja também:
- [README.md](README.md) - Visão geral do projeto
- [INSTALLATION.md](INSTALLATION.md) - Como instalar
- [FEATURES.md](FEATURES.md) - Todas as funcionalidades

---

<div align="center">

### ❓ Não achou a solução? 

**Contate o desenvolvedor! Ele está aqui para ajudar! 👨‍💼**

</div>
