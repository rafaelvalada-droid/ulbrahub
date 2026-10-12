# UlbraHub — app para o celular

Esta é a "casca" que transforma o **UlbraHub** (Hub de Acessos ULBRA, feito no Google Apps Script)
num app instalável no celular: ícone próprio, nome UlbraHub, tela de abertura e tela cheia.
O hub de verdade continua no Apps Script e abre dentro desta página; para ver os apps é
preciso entrar com a conta Google da ULBRA.

**Endereço do app:** https://rafaelvalada-droid.github.io/ulbrahub/

## Como instalar no Android
1. Abra o endereço acima no Chrome.
2. Toque no menu **⋮** e em **"Instalar app"** (em algumas versões: "Adicionar à tela inicial" → "Instalar").

## Arquivos
- `index.html` — a casca: abre o hub (link `/exec` do Apps Script, na constante `HUB_URL`) em tela cheia,
  mostra a tela de abertura até o hub avisar que carregou e oferece "Abrir no navegador" se ele não abrir.
- `manifest.webmanifest` — nome, cores e ícones do app.
- `sw.js` — guarda a casca no celular para abrir rápido e funcionar sem internet.
- `icon-*.png`, `apple-touch-icon.png`, `favicon-48.png` — ícones.

O código do hub (Apps Script) fica no repositório `nuvem`, pasta `hub-acessos/`.
Se o link `/exec` mudar (nova implantação com outro endereço), atualize `HUB_URL` no `index.html`.
