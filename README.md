# Finanças 360 — publicar no Netlify

Este repositório contém a página `index.html` e os recursos do PWA.

## Ativar instalação/offline no PWA

No `index.html`:

1. No `<head>`, use a viewport com `viewport-fit=cover` e inclua o link para `manifest.webmanifest` e a meta de cor do tema.
2. Antes de `</body>`, registre `service-worker.js` usando `navigator.serviceWorker.register('./service-worker.js')`.

A publicação deve ser feita por HTTPS para que o service worker funcione. Os dados financeiros ficam no armazenamento local do navegador e não são sincronizados automaticamente entre aparelhos.
