# Wavelength — Edição de festa

Site estático responsivo, em português, inspirado na dinâmica do jogo Wavelength. As cartas são **adaptações originais**, não o baralho oficial.

## Publicar (mais fácil)

1. Extraia `wavelength-site.zip`.
2. Acesse https://app.netlify.com/drop e arraste a pasta `wavelength-site` para a área de publicação.
3. O Netlify gera uma URL pública. Nenhum build ou instalação é necessário.

## Outras opções

- **GitHub Pages:** coloque os arquivos na raiz de um repositório e ative Pages (Deploy from branch).
- **Vercel:** importe um repositório contendo os arquivos e escolha a configuração de site estático, sem build.
- **Hospedagem comum:** envie os arquivos para a pasta pública (`public_html`, `www`, etc.).

## Rodar localmente

Abra `index.html` em um navegador moderno. Se preferir servir via HTTP, dentro da pasta execute `python3 -m http.server 8000` e acesse `http://localhost:8000`.

## Arquivos

- `index.html`: estrutura e metadados.
- `styles.css`: aparência responsiva, contraste e espaçamentos.
- `app.js`: cartas, temas, navegação, regras e cronômetro.
- `favicon.svg`: ícone do site.
- `manifest.webmanifest`, `sw.js`, `icons/`: PWA (instalar no celular e jogar offline).

## Instalar como app (PWA)

Precisa estar publicado em HTTPS (a Hostinger já fornece).

- **Android (Chrome):** menu ⋮ → *Instalar app* / *Adicionar à tela inicial*.
- **iPhone (Safari):** botão Compartilhar → *Adicionar à Tela de Início*.

Depois de aberto uma vez, funciona sem internet. Com internet, sempre carrega a versão mais recente.

## Regras implementadas

- Cinco temas, com cartas em português.
- Uma troca por rodada, com possibilidade de voltar à primeira carta.
- Cronômetro configurável (1 a 10 minutos, padrão 5) no menu principal, salvo no aparelho, iniciado manualmente depois da escolha da carta.
- Se o cronômetro zerar, a rodada não pontua.
- Nova rodada sorteia outra carta; menu principal encerra a rodada atual.
- Cartas não se repetem até esgotar o baralho do tema; depois ele é embaralhado novamente.
- Sem dependências, cookies ou backend.

## Personalizar

Edite `SOURCE` em `app.js`: cada carta é `extremo esquerdo|extremo direito`, separada por ponto e vírgula. Os temas ficam em `THEMES`.

## Observação

A partida atual não é persistida se a página for recarregada. Para evitar interrupções no celular, mantenha a tela ativa durante a rodada.
