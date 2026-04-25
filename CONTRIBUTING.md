# 🤝 Guia de Contribuição

> Quer contribuir para o projeto Pokedex? Adoraríamos sua ajuda! ✨

---

## 📋 Índice

- [Como Começar](#-como-começar)
- [Regras de Contribuição](#-regras-de-contribuição)
- [Tipos de Contribuição](#-tipos-de-contribuição)
- [Processo de Pull Request](#-processo-de-pull-request)
- [Padrões de Código](#-padrões-de-código)
- [Reportar Bugs](#-reportar-bugs)
- [Sugestões de Melhoria](#-sugestões-de-melhoria)

---

## 🚀 Como Começar

### 1️⃣ Faça um Fork do Projeto
```bash
# Clique em "Fork" no GitHub
# Isso cria sua cópia pessoal do repositório
```

### 2️⃣ Clone o Repositório Forked
```bash
git clone https://github.com/[seu-usuario]/Pokedex.git
cd Pokedex
```

### 3️⃣ Crie uma Branch
```bash
# Para novo recurso
git checkout -b feature/sua-funcionalidade

# Para correção de bug
git checkout -b bugfix/descricao-bug

# Para documentação
git checkout -b docs/melhorias-doc
```

### 4️⃣ Faça suas Alterações
```bash
# Modifique os arquivos conforme necessário
# Teste suas mudanças
```

### 5️⃣ Commit e Push
```bash
git add .
git commit -m "Descrição clara da mudança"
git push origin sua-branch
```

### 6️⃣ Abra um Pull Request
```
Ir ao GitHub → Compare & Pull Request
```

---

## ✅ Regras de Contribuição

### 📋 Padrões Obrigatórios

✅ **DO (Faça):**
- ✓ Escreva código limpo e bem comentado
- ✓ Teste suas mudanças antes de submeter
- ✓ Use nomes descritivos para variáveis
- ✓ Mantenha compatibilidade com navegadores antigos
- ✓ Atualize a documentação se necessário
- ✓ Use commits com mensagens claras
- ✓ Teste em múltiplos navegadores
- ✓ Respeite o código existente

❌ **DON'T (Não faça):**
- ✗ Não envie código quebrado
- ✗ Não remova funcionalidades sem discussão
- ✗ Não mude estilos de forma drástica
- ✗ Não adicione dependências desnecessárias
- ✗ Não escreva código ofensivo ou discriminatório
- ✗ Não reclame por rejeição de PR
- ✗ Não spam ou abuso

---

## 🎯 Tipos de Contribuição

### 🐛 1. Correção de Bugs

**O que fazer:**
- Identificar e corrigir erros
- Testar a solução
- Documentar a mudança

**Exemplo:**
```markdown
**Tipo:** Bug Fix
**Descrição:** Corrigir busca que não funciona com números de 3 dígitos
**Como Testar:** Digite 100 na barra de busca
**Resultado:** Deve exibir Voltorb corretamente
```

### ✨ 2. Novas Funcionalidades

**Antes de começar:**
- Abra uma ISSUE para discussão
- Aguarde aprovação
- Descreva a funcionalidade

**Exemplo de Issue:**
```markdown
**Título:** [FEATURE] Adicionar favoritos
**Descrição:** 
- Permitir marcar Pokémons como favorito
- Salvar em localStorage
- Mostrar página de favoritos

**Benefício:** Usuários conseguem acompanhar seus Pokémons preferidos
```

### 📚 3. Melhorias na Documentação

**Tipos de melhorias:**
- Corrigir erros de digitação
- Adicionar exemplos
- Melhorar clareza
- Traduzir para outros idiomas
- Adicionar imagens/diagramas

**Processo:**
1. Edite os arquivos `.md`
2. Verifique formatação
3. Faça PR com mudanças

### 🎨 4. Melhorias de UX/UI

**Tipos de mudanças:**
- Melhorar design visual
- Otimizar mobile
- Adicionar animações
- Melhorar acessibilidade

**Antes de começar:**
- Tire screenshots antes/depois
- Explique a melhoria
- Mantenha compatibilidade

### ⚡ 5. Otimizações de Performance

**Focos:**
- Reduzir tamanho de arquivos
- Melhorar velocidade de carregamento
- Otimizar requisições à API
- Melhorar eficiência de código

**Teste:**
```javascript
// Meça performance antes/depois
console.time('operação');
// seu código
console.timeEnd('operação');
```

---

## 📝 Processo de Pull Request

### 📋 Checklist Antes de PR

```
□ Testei em múltiplos navegadores
□ Meu código segue o padrão do projeto
□ Não há console.log() ou código de debug
□ Atualizei a documentação
□ Meu commit message é claro e descritivo
□ Minha branch está atualizada com main
□ Não há conflitos de merge
□ Código está bem comentado
```

### 💬 Template de PR

```markdown
## Descrição
Descreva as mudanças de forma clara e concisa.

## Tipo de Mudança
- [ ] Bug fix
- [ ] Nova funcionalidade
- [ ] Melhoria na documentação
- [ ] Otimização de performance
- [ ] Outra (descreva):

## Como Testar
Descreva os passos para testar a mudança:
1. ...
2. ...

## Screenshots (se aplicável)
Adicione screenshots mostrando as mudanças.

## Checklist
- [ ] Testei em Chrome
- [ ] Testei em Firefox
- [ ] Testei em mobile
- [ ] Documentação atualizada
- [ ] Sem console.log() ou debug code
```

### 📞 O Que Esperar

1. **Review do Código** (1-7 dias)
   - Desenvolvedor vai revisar
   - Pode pedir mudanças
   - Vai comentar sugestões

2. **Feedback**
   - ✅ Aprovado e merged
   - ⚠️ Mudanças requisitadas
   - ❌ Rejeitado com explicação

3. **Merge**
   - Se aprovado, será mergeado para main
   - Aparecerá na próxima versão

---

## 🎨 Padrões de Código

### JavaScript

**Boas Práticas:**
```javascript
// ✓ Use const/let, não var
const name = "Wellington";
let count = 0;

// ✓ Use funções arrow quando apropriado
const fetchData = async (url) => {
    const response = await fetch(url);
    return response.json();
};

// ✓ Use nomes descritivos
const fetchPokemonData = async (id) => {
    // ...
};

// ✗ Evite nomes confusos
const fp = async (i) => {
    // ...
};

// ✓ Comente código complexo
const calculateStats = (base, level) => {
    // Fórmula de cálculo Pokémon: 2 * base/5 + 5
    return (2 * base / 5) + 5;
};

// ✓ Use template literals
const url = `https://pokeapi.co/api/v2/pokemon/${id}`;

// ✗ Evite concatenação
const url = "https://pokeapi.co/api/v2/pokemon/" + id;
```

### CSS

**Boas Práticas:**
```css
/* ✓ Use classes bem nomeadas */
.pokemon-card { }
.search-input { }

/* ✓ Organize propriedades logicamente */
.element {
    display: flex;
    margin: 10px;
    padding: 5px;
    color: white;
    background: blue;
}

/* ✓ Use variáveis CSS */
:root {
    --primary-color: #007bff;
    --border-radius: 8px;
}

.element {
    background: var(--primary-color);
    border-radius: var(--border-radius);
}

/* ✗ Evite IDs para estilos */
#myElement { } /* Ruim */
.my-element { } /* Bom */
```

### HTML

**Boas Práticas:**
```html
<!-- ✓ Use semântica correta -->
<header>
    <nav>...</nav>
</header>
<main>
    <article>...</article>
</main>
<footer>...</footer>

<!-- ✓ Use atributos alt em imagens -->
<img src="pokemon.png" alt="Imagem do Pokémon Pikachu">

<!-- ✓ Indentação clara -->
<div class="container">
    <div class="item">
        <h2>Título</h2>
        <p>Descrição</p>
    </div>
</div>
```

---

## 🐛 Reportar Bugs

### Como Reportar

**Vá para:** GitHub Issues → New Issue

**Template:**
```markdown
## 🐛 Descrição do Bug
Descrição clara do problema.

## 🔍 Como Reproduzir
1. Clique em...
2. Digite...
3. O erro ocorre quando...

## ❌ Comportamento Esperado
O que deveria acontecer

## 📌 Comportamento Atual
O que realmente acontece

## 🖥️ Ambiente
- Navegador: Chrome 100
- SO: Windows 10
- Resolução: 1920x1080

## 📎 Screenshots/Logs
Adicione screenshots ou logs do console

## 📝 Notas Adicionais
Outras informações relevantes
```

### Bons Títulos de Issue

✓ "Busca não funciona com números de 3 dígitos"
✓ "Cursor customizado não carrega em Firefox"
✓ "Música ativa por padrão causa lag"

✗ "Bug"
✗ "Não funciona"
✗ "AJUDA!!!"

---

## 💡 Sugestões de Melhoria

### Como Sugerir

**Vá para:** GitHub Issues → New Issue → Feature Request

**Template:**
```markdown
## ✨ Descrição da Sugestão
Descreva a funcionalidade desejada.

## 🎯 Problema que Resolve
Qual problema ou limitação isso resolve?

## 💭 Solução Proposta
Como você imagina que funcione?

## 📚 Alternativas Consideradas
Outras abordagens?

## 📊 Valor Agregado
Por que isso seria bom para o projeto?

## 📝 Contexto Adicional
Screenshots, exemplos, etc
```

---

## 📚 Recursos Úteis

### Documentação
- [README.md](README.md) - Visão geral
- [FEATURES.md](FEATURES.md) - Funcionalidades
- [INSTALLATION.md](INSTALLATION.md) - Instalação

### Git
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)

### JavaScript
- [MDN Web Docs](https://developer.mozilla.org/)
- [JavaScript.info](https://javascript.info/)

### API
- [PokeAPI Documentation](https://pokeapi.co/)

---

## 🎓 Convenções do Projeto

### Nomes de Branch

```
feature/nome-da-funcionalidade
bugfix/descricao-do-bug
docs/melhorias-documentacao
refactor/descricao-refactor
test/testes-adicionados
```

### Nomes de Commit

```
✨ feat: Adicionar busca por tipo
🐛 fix: Corrigir overflow em mobile
📚 docs: Atualizar README
♻️ refactor: Simplificar função search
🧪 test: Adicionar testes
🎨 style: Melhorar indentação
⚡ perf: Otimizar requisições à API
```

### Versionamento

Seguimos Semantic Versioning: `MAJOR.MINOR.PATCH`
- MAJOR: Mudanças incompatíveis
- MINOR: Novas funcionalidades compatíveis
- PATCH: Correções de bugs

---

## 🎉 Reconhecimento

Todos os contribuidores serão reconhecidos em:
- 📄 Lista de Contribuidores no README
- 🏆 Seção especial no GitHub
- 💜 Nosso agradecimento eterno

---

## ❓ Dúvidas?

**Não tem certeza?**
- 📖 Releia este guia
- 💬 Abra uma discussion no GitHub
- 📧 Contate o desenvolvedor

**Principais Contatos:**
- 🔗 LinkedIn: https://www.linkedin.com/in/wellingtonlima37/
- 🐙 GitHub: https://github.com/WelIingtonLima

---

## 📜 Código de Conduta

Este projeto adota um código de conduta baseado em:
- ✅ Ser respeitoso
- ✅ Ser inclusivo
- ✅ Ser construtivo
- ❌ Sem discriminação
- ❌ Sem assédio
- ❌ Sem comportamento abusivo

**Violações:** Serão reportadas aos moderadores.

---

<div align="center">

### 🙌 Obrigado por Contribuir! 🙌

**Sua ajuda torna este projeto melhor para todos!** ✨

</div>
