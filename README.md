# ⚽ Álbum Copa 2026 — controle de figurinhas

App web simples para marcar as figurinhas do álbum da Copa do Mundo 2026
(Panini). Funciona em celular e PC, **salva as marcações no próprio navegador**
e pode ser hospedado de graça no **GitHub Pages**.

## Arquivos
- `index.html` — o aplicativo (visual, lógica).
- `dados.js` — **os dados** (nomes, números, seleções, Legends, Update Set).
  É **este** arquivo que você edita para atualizar o app.
- `README.md` — este guia.

## Como publicar (uma vez)
1. Crie um repositório no GitHub (público) e envie estes arquivos (veja comandos abaixo).
2. No GitHub: **Settings → Pages → Branch: `main` / `root` → Save**.
3. Em ~1 minuto o app abre em `https://SEU-USUARIO.github.io/album-copa-2026/`.
4. No celular, use **Adicionar à tela de início** para abrir como um app.

### Comandos para enviar ao GitHub
```bash
cd album-copa-2026
git init && git add . && git commit -m "Álbum Copa 2026"
# Opção A — com GitHub CLI (gh):
gh repo create album-copa-2026 --public --source=. --push
# Opção B — manual: crie o repo no site e depois:
git remote add origin https://github.com/SEU-USUARIO/album-copa-2026.git
git branch -M main
git push -u origin main
```

## Como atualizar (ex.: preencher o Update Set)
1. Abra `dados.js` num editor de texto.
2. Em `updateSet`, **descomente** a linha (tire as `//`) e preencha nome e seleção. Ex.:
   ```js
   "1": {nome:"Neymar Jr", sel:"Brasil"},
   ```
   Você também pode **corrigir qualquer nome** dentro de `nomes`.
3. Salve e rode:
   ```bash
   git add . && git commit -m "atualiza nomes" && git push
   ```
4. O site no GitHub Pages atualiza sozinho em ~1 minuto.

## Backup das suas marcações
As marcações ficam no navegador de cada aparelho. Use os botões **Backup**
(baixa um `.json`) e **Restaurar** (lê o `.json`) para passar de um aparelho a outro.

> Nomes do álbum a partir de checklist da comunidade; podem existir pequenas
> diferenças de grafia — corrija em `dados.js` quando quiser.
