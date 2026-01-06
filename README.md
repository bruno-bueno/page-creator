# 📄 Page Generator - Landing Pages Dinâmicas

Este projeto é um **template universal de Landing Page** de alta conversão. A estrutura foi desenhada para permitir que qualquer pessoa crie uma página de vendas completa apenas editando um arquivo de configuração simples e trocando imagens, sem tocar em HTML.

## 🎯 Conceito do Projeto
A ideia é simples:
1. **Baixe** este repositório.
2. **Edite** o arquivo `copy.json` com seus textos e caminhos de imagem.
3. **Pronto!** Sua página está criada.

Precisa mudar cores, fontes ou layout? Peça para sua IA de preferência (como o Antigravity!) ajustar o `styles.css`. O código é limpo e modular, facilitando essas customizações.

---

## 🚀 Como Rodar

Devido à segurança dos navegadores modernos (que bloqueiam carregamento de arquivos JSON locais), você **precisa de um servidor local** para ver a página funcionando.

### Usando VS Code (Recomendado)
1. Instale a extensão **Live Server**.
2. Clique com o botão direito em `nova_pagina.html`.
3. Escolha **"Open with Live Server"**.

---

## 🛠 Como Personalizar (Passo a Passo)

### 1. Texto e Imagens (`copy.json`)
Abra o arquivo `copy.json`. Ele contém todo o conteúdo do site.
- **Imagens**: Coloque suas imagens na pasta `media/` e atualize os caminhos no JSON (ex: `"image": "media/minha-foto.png"`).
- **Textos**: Altere títulos, descrições, preços e itens de lista diretamente nas linhas de texto. HTML básico (como `<br>` e `<span>`) é aceito para formatação.

### 2. Estilização (`styles.css`)
O design visual está isolado no arquivo `styles.css`.
- Quer mudar de verde para azul?
- Quer aumentar a fonte?
- Quer mudar o espaçamento?

**Dica:** Peça para a IA! Exemplo de prompt:
> *"Mude a cor principal do site para azul marinho e deixe os títulos com fonte roboto."*

---

## 📁 Estrutura de Arquivos

- **`copy.json`**: O "cérebro" da página. Todo o conteúdo editável vive aqui.
- **`nova_pagina.html`**: A estrutura base. Você raramente precisará mexer aqui.
- **`styles.css`**: O design. Edite aqui para mudar cores e visuais.
- **`media/`**: Pasta para suas imagens.

## ✨ Recursos Automáticos
- **Carregamento Dinâmico**: O site só mostra o que está no JSON.
- **Ícones SVG**: Ícones de alta qualidade (checks, setas, presentes) são inseridos automaticamente pelo sistema.
