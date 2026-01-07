# 📄 Page Generator -# Gerador de Landing Pages Dinâmico

Este projeto é um template de Landing Page de alta conversão, totalmente editável através de um arquivo de configuração JSON. Você não precisa editar HTML ou CSS para alterar textos, imagens, links, preços ou ID do Pixel.

O projeto foi reorganizado em dois exemplos para facilitar o uso:

## Estruturas de Exemplo

### 1. Simple Example (`/simple example`)
A versão padrão e direta.
- **Como usar:** Edite o arquivo `copy.json`.
- **Ideal para:** Quem precisa de uma página única, rápida e sem complexidade de múltiplos idiomas.
- **Funcionalidades:**
  - Carregamento de conteúdo via `copy.json`.
  - Integração fácil com Pixel do Facebook (basta colocar o ID no JSON).

### 2. Multi-language Example (`/multi-language example`)
A versão avançada com suporte a múltiplos idiomas.
- **Como usar:**
  - O sistema detecta automaticamente o idioma do navegador do visitante (ex: `pt-BR`, `en-US`).
  - Tenta carregar o arquivo correspondente na pasta `/languages` (ex: `languages/pt-BR.json`).
  - Se não encontrar, carrega automaticamente o arquivo `default.json` como fallback.
- **Estrutura de Arquivos:**
  - `default.json`: Configuração padrão/fallback.
  - `languages/`: Pasta para adicionar novos idiomas (ex: `es.json`, `fr.json`).

## Funcionalidades Globais

### 🎨 Customização Fácil
Tudo é controlado pelos arquivos JSON (`copy.json` ou `default.json`):
- **Hero:** Título, subtítulo, imagem.
- **Oferta:** Preços (De/Por), badge de garantia, link de checkout.
- **Pixel do Facebook:** Basta adicionar seu ID no campo `"facebook_pixel_id"`.
- **Seções:** Benefícios, Público-Alvo, Depoimentos, Bônus, Chamada Final.

### 📱 100% Responsivo
O layout se adapta perfeitamente a celulares, tablets e desktops.

### ⚡ Instalação
Não requer instalação de dependências (Node.js, etc) para rodar a versão final.
1. Baixe os arquivos.
2. Abra a pasta do exemplo desejado.
3. Edite o JSON.
4. Hospede os arquivos em qualquer servidor estático (Vercel, Netlify, Apache, Nginx) ou abra localmente.

> **Nota:** Para testar localmente (no seu computador), o navegador pode bloquear o carregamento do JSON por segurança (CORS). Recomendamos usar uma extensão como "Live Server" no VS Code.

## Exemplo de Configuração (JSON)
```json
{
    "checkout_url": "https://seu-link-de-checkout.com",
    "facebook_pixel_id": "123456789",
    "hero": {
        "title": "Seu Título Principal",
        "subtitle": "Seu subtítulo matador...",
        "image": "media/sua-imagem.png"
    }
    // ... restante da configuração
}
```

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
