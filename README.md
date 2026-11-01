# GVG & ARTEFAL — PWA de Gastos

Shell instalável que abre o **Controle de Gastos** dentro do próprio app, sem redirecionar
para `script.google.com` e sem exibir a faixa azul do Google Apps Script.

## Arquitetura

```
GitHub Pages (shell + manifest + service worker + ícones)
        └── iframe em tela cheia → Apps Script /exec (app real)
```

O sistema, a planilha e os lançamentos continuam no Google Apps Script da empresa.

## Links

- PWA: `https://higoragenteia.github.io/gvg-gastos/`
- App (Apps Script): `https://script.google.com/macros/s/AKfycbzVpIK4Ov2PPKU6NduyLDQMFo-5UA7nfVKFDANnvv2ej1YIGuimVq2pWngUWnPRK4P_/exec`
- Planilha: `https://docs.google.com/spreadsheets/d/1zj0t-2DbQoz6spian5q-umlg9hu9SJUHUPMaUzgt2XI/edit`

## Login

O app usa login próprio por e-mail e senha, com aprovação do administrador.
Administrador inicial: `higorjose.gvgesquadrias@gmail.com`.

## Instalação

### Android

Abra a URL do GitHub Pages no Chrome e use **📲 Instalar**.

### iPhone

No Safari, abra a URL e use **Compartilhar → Adicionar à Tela de Início**.

> No iPhone, o app instalado abre o Apps Script diretamente para manter o layout correto.

## Atualizações

O service worker usa `CACHE = 'gvg-gastos-pwa-v1'`. Ao publicar uma nova versão do shell,
incremente esse valor. O conteúdo do Apps Script é atualizado pelo próprio Apps Script.
