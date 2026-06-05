# Conversor SpEL → JS

Ferramenta web para converter expressões **Spring Expression Language (SpEL)** usadas no IBM Watson Assistant / Watson Dialog para sintaxe **JavaScript** compatível com fluxos modernos.

## ✨ Funcionalidades

- Conversão em tempo real com atalho `Ctrl+Enter`
- Saída formatada (multilinha) e em linha única para fácil cópia
- Interface com suporte a tema claro/escuro (segue o sistema)
- Exibe as regras de conversão ativas na tela

## 🔄 Regras de conversão

| SpEL | JavaScript |
|------|-----------|
| `$variavel` | `conversation.context.variavel` |
| `@Intent` / `#Intent` | `workflow.Intent.result === "intent"` |
| `input.text` | `event.preview` |
| `intents[0].confidence > x &&` | removido |
| `context['chave']` | `context.chave` |
| `.append(item)` | `[...arr, item]` |
| `.size()` | `.length` |
| `.length()` | `.length` |
| `.contains(x)` | `.includes(x)` |
| `.remove(i)` | `.filter((_, i) => i !== idx)` |
| `==` | `===` |
| `!=` | `!==` |
| `(expr) ? false : true` | `!(expr)` |
| `<? ... ?>` | removido |

## 🚀 Como usar

Não requer instalação. É um único arquivo HTML estático.

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/seu-repo.git
   ```
2. Abra o arquivo `index.html` no navegador.

Ou hospede em qualquer serviço de páginas estáticas (GitHub Pages, Netlify, Vercel etc.).

## 🛠️ Tecnologias

- HTML, CSS e JavaScript puros — sem dependências ou bundlers
- [Tabler Icons](https://tabler-icons.io/) via CDN para os ícones

