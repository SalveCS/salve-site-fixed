# Salve Comunicação Sustentável

Site institucional da Salve. Página única em HTML, CSS e JavaScript puros, sem build e sem dependências.

## Estrutura

```
index.html                     página principal
politica-de-privacidade.html   política de privacidade, LGPD
termos-de-uso.html             termos de uso
assets/logo-salve.png          logo, usado como máscara e colorido pelo CSS
og-image.jpg                   imagem de compartilhamento, 1200 x 630
favicon.ico, favicon-512.png, apple-touch-icon.png, site.webmanifest
robots.txt, sitemap.xml
vercel.json                    cabeçalhos de segurança e cache
```

## Publicar no repositório atual, projeto Vite

O projeto que já está na Vercel usa Vite. Nele, os arquivos estáticos precisam ficar na pasta `public`, senão não vão para o ar.

1. Na raiz do repositório, substitua `index.html` e `vercel.json` por estes.
2. Copie o conteúdo da pasta `public` deste pacote para a pasta `public` do repositório, substituindo os arquivos antigos.
3. Apague `public/manifest.json` e `public/favicon.png`, que são do site antigo.
4. Faça o commit. A Vercel publica sozinha.

O arquivo `public/sw.js` desativa o service worker do site antigo, que guardava a versão velha no navegador de quem já tinha visitado o site. Ele precisa ficar no ar por alguns meses.

## Publicar como site estático, sem Vite

1. No GitHub, crie um repositório, por exemplo `salve-site`.
2. Envie o conteúdo desta pasta para a raiz do repositório. Pelo site do GitHub, use Add file, Upload files e arraste todos os arquivos e a pasta assets.
3. Na Vercel, clique em Add New, Project, e importe o repositório.
4. Em Framework Preset escolha Other. Deixe Build Command e Output Directory vazios.
5. Clique em Deploy.

Se o domínio salv3.vercel.app já pertence a outro projeto na Vercel, conecte o novo repositório a esse mesmo projeto em Settings, Git, ou troque o conteúdo do repositório antigo por esta pasta.

## Ao trocar de domínio

Substitua `https://salv3.vercel.app` pelo novo endereço em `index.html`, nas duas páginas legais, em `robots.txt` e em `sitemap.xml`.

## Medição

Google Analytics 4, ID `G-BJ72P2VW3S`. Cliques em WhatsApp, email e Instagram geram o evento `generate_lead`, com o canal em `method` e a seção da página em `local`.
