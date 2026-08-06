# Apulian Routes

Minisito per la proposta di **experiences offline ai turisti in Puglia**.

- **Dominio**: [apulianroutes.com](https://apulianroutes.com)
- **Hosting**: GitHub Pages (branch `main`, root `/`)
- **Stack**: sito statico HTML/CSS/JS — nessun build step al momento

## Struttura

```
index.html        homepage
assets/
  css/
  js/
  img/
CNAME             dominio custom per GitHub Pages
```

## Sviluppo locale

```bash
python3 -m http.server 8080
# → http://localhost:8080
```

## Deploy

Push su `main` → GitHub Pages pubblica automaticamente.
Configurazione: *Settings → Pages → Source: Deploy from a branch → `main` / `(root)`*.

Il file `CNAME` deve restare in root e contenere `apulianroutes.com`.

## DNS

Per il dominio apex su GitHub Pages, presso il registrar impostare:

| Tipo | Nome | Valore |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | gfanizza.github.io |

Poi in *Settings → Pages* spuntare **Enforce HTTPS** (dopo l'emissione del certificato).
