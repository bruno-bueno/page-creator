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
A versão avançada com suporte "inteligente" a múltiplos idiomas.

- **Como funciona a detecção:**
  1. O sistema detecta o idioma do navegador (ex: `pt-BR`, `en-US`, `es-AR`).
  2. **Tentativa Específica:** Tenta carregar o arquivo exato (ex: `languages/en-US.json`).
  3. **Tentativa Genérica:** Se falhar, tenta carregar o código geral (ex: `languages/en.json` para qualquer variação de inglês).
  4. **Fallback:** Se nenhum for encontrado, carrega o `default.json` (Geralmente em Português).
  
- **Estrutura de Arquivos:**
  - `default.json`: Configuração padrão se nenhum idioma for detectado.
  - `languages/`: Pasta onde ficam os arquivos de tradução.

#### 🌍 Lista de Códigos de Idiomas
Para criar novos idiomas, basta criar um arquivo `.json` dentro da pasta `languages/` com o código ISO correspondente. Abaixo os principais códigos:

| Idioma | Nome do Arquivo (Recomendado) | Abrange |
| :--- | :--- | :--- |
| **Inglês** | `en.json` | EUA, Reino Unido, Austrália, Canadá, etc. |
| **Espanhol** | `es.json` | Espanha, México, Argentina, Colômbia, etc. |
| **Português** | `pt.json` (ou use o default) | Brasil, Portugal, Angola. |
| **Francês** | `fr.json` | França, Canadá, Bélgica, Suíça. |
| **Alemão** | `de.json` | Alemanha, Áustria, Suíça. |
| **Italiano** | `it.json` | Itália, Suíça. |
| **Chinês** | `zh.json` | China, Singapura, Taiwan. |
| **Japonês** | `ja.json` | Japão. |
| **Russo** | `ru.json` | Rússia, Bielorrússia. |

> **Dica:** Você pode ser específico se quiser. Se criar um arquivo `pt-PT.json`, ele será carregado APENAS para usuários de Portugal, enquanto `pt.json` (ou o default) servirá para os demais.

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
