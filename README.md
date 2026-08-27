# 1000 Cosas que debe saber un Bachiller Venezolano

Quiz interactivo de selección múltiple basado en el pensum oficial de Educación Media General de Venezuela (Resolución Ministerial 41.221, 2017 — 14 áreas de formación, 5 años).

Sitio 100% estático: un solo archivo `index.html` con HTML, CSS y JavaScript sin dependencias externas (aparte de Google Fonts) ni servidor. No hay backend, no se recopilan datos personales; los puntajes de práctica solo se guardan en el navegador de quien juega.

## Uso local

Abre `index.html` directamente en cualquier navegador, o sirve la carpeta con cualquier servidor estático:

```bash
python -m http.server 8000
```

## Estructura del contenido

Las preguntas viven en el arreglo `Q` dentro de `index.html`, con este esquema:

```js
{ a: "CAS", y: 1, q: "Pregunta...", o: ["Opción A","Opción B","Opción C","Opción D"], c: 0, e: "Explicación opcional" }
```

- `a`: código de área (ver `AREAS` en el mismo archivo)
- `y`: año (1 a 5)
- `o`: las 4 opciones
- `c`: índice (0-3) de la opción correcta
- `e`: explicación breve (opcional)

**Estado actual:** lote 1, 140 preguntas (10 por área). Meta del proyecto: 1000-2000 preguntas.

## Publicación

Pensado para desplegarse como sitio estático (GitHub Pages, Netlify, Vercel, Cloudflare Pages) sin ningún paso de build.
