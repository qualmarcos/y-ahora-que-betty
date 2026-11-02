# ¿Y ahora qué, Betty?

Jogo de perguntas em espanhol sobre *Yo soy Betty, la fea*, pronto para ser instalado como app (PWA).

## Arquivos

- `index.html`: o jogo completo
- `manifest.webmanifest`: nome, cores e ícones do app
- `sw.js`: service worker que guarda o jogo para funcionar offline
- `icons/`: ícones feitos a partir do bonequinho da Betty

## Como funciona no celular

Em celular, o jogo só abre depois de instalado na tela inicial. Antes disso, aparece uma tela com o passo a passo:

- **Android (Chrome):** botão "Instalar el juego" ou menu ⋮ → "Instalar app"
- **iPhone (Safari):** Compartilhar → "Agregar a pantalla de inicio"
- **Navegador interno do WhatsApp, Instagram etc.:** pede para abrir o link no Safari ou no Chrome

No computador, o jogo abre normalmente no navegador.

## Como publicar (precisa de HTTPS)

**Opção mais fácil: Netlify Drop**
1. Acesse https://app.netlify.com/drop
2. Arraste a pasta `betty-la-fea` inteira para a página
3. Copie o link `https://...netlify.app` e abra no celular

**Opção GitHub Pages**
1. Crie um repositório público no GitHub e envie estes arquivos
2. Em Settings → Pages, escolha a branch `main` e a pasta `/ (root)`
3. O jogo fica em `https://SEU-USUARIO.github.io/NOME-DO-REPO/`

## Testar no computador

```sh
cd betty-la-fea
python3 -m http.server 8000
```

Depois abra http://localhost:8000

## Atualizar o jogo

Depois de mudar os arquivos, altere `CACHE = "betty-v1"` em `sw.js` para `betty-v2` e assim por diante. Isso faz os celulares baixarem a nova versão.

## Créditos

Homenagem de fãs, sem fins comerciais, a *Yo soy Betty, la fea*, novela criada e escrita por Fernando Gaitán e produzida pela RCN Televisión (Colômbia, 1999–2001).
