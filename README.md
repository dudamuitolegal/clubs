# Clubs JSON API

Arquivo JSON estático hospedado na Vercel com CORS habilitado, para consumo via `fetch` em popups HTML.

## Estrutura

```
clubs.json     → Dados dos clubes (Série A, Série B, Premier League, La Liga)
vercel.json    → Configuração de headers CORS
```

## Endpoint

Após o deploy, o JSON fica disponível em:

```
https://clubs-coral.vercel.app/clubs.json
```

## Uso

```js
fetch('https://<seu-dominio>.vercel.app/clubs.json')
  .then(res => res.json())
  .then(data => console.log(data.leagues));
```

## Deploy

1. Instale a Vercel CLI: `npm i -g vercel`
2. Na raiz do projeto, rode: `vercel`
3. Para produção: `vercel --prod`
