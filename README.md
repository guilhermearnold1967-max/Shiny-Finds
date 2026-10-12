# Shiny Finds — página de links

Página estilo Linktree da marca **Shiny Finds** (canal de ofertas para casa e bebê), com botões para o canal do WhatsApp e para o grupo do Telegram.

## Tecnologia

**HTML, CSS e JavaScript simples.** Não usa React, Vite, npm nem etapa de build. As únicas dependências externas são as fontes do Google Fonts (Montserrat, Inter e Yellowtail), carregadas por CDN.

## Estrutura

```
shiny-finds-site/
├── index.html      # estrutura e textos da página
├── styles.css      # visual (cores, tipografia, layout)
├── script.js       # links dos botões
├── favicon.svg
├── .nojekyll       # evita processamento do Jekyll no GitHub Pages
├── .gitignore
└── assets/
    ├── logo-shiny-finds.jpg
    ├── hero-cup.jpg
    ├── cozinha.jpg
    └── quarto-bebe.jpg
```

## Executar localmente

Dê dois cliques em `index.html`, ou, para simular um servidor:

```bash
python3 -m http.server 8000
# abra http://localhost:8000
```

## Alterar os links dos botões

Edite as duas primeiras linhas úteis de `script.js`:

```js
var WHATSAPP_URL = "https://whatsapp.com/channel/...";
var TELEGRAM_URL = "https://t.me/+...";
```

## Publicar no GitHub Pages

1. No GitHub, clique em **New repository**, escolha um nome (ex.: `shiny-finds`) e deixe **Public**.
2. Envie os arquivos **da pasta** (o `index.html` precisa ficar na raiz do repositório):
   - Pelo site: **Add file > Upload files**, arraste todo o conteúdo da pasta (incluindo `assets/`) e clique em **Commit changes**; ou
   - Pelo terminal:
     ```bash
     cd shiny-finds-site
     git init
     git add .
     git commit -m "Primeira versão do site"
     git branch -M main
     git remote add origin https://github.com/SEU-USUARIO/shiny-finds.git
     git push -u origin main
     ```
3. Vá em **Settings > Pages**. Em **Build and deployment**, escolha **Deploy from a branch**, branch **main**, pasta **/ (root)** e clique em **Save**.
4. Aguarde 1 a 2 minutos. O site ficará em `https://SEU-USUARIO.github.io/shiny-finds/`.
5. Coloque esse endereço na biografia do Instagram.

Para atualizar o site depois, basta enviar os arquivos alterados (ou fazer `git push`); a publicação é refeita sozinha.

## Domínio próprio (opcional)

Em **Settings > Pages > Custom domain**, informe o domínio e siga as instruções de DNS do GitHub.
