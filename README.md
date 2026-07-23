# Tarjeta de visita digital — Erik Tomás

Página estática de una sola pantalla para grabar en un sticker NFC: quien lo acerque
al móvil ve la tarjeta y puede guardar el contacto con un toque.

## Archivos

- `index.html` — la tarjeta (rojo Voltamper #E40918, Fraunces + Archivo, sello giratorio).
- `erik-tomas.vcf` — la ficha de contacto que descarga el botón "Guardar contacto".
  En iPhone, al abrirse desde una web pública, Safari muestra directamente la
  vista previa del contacto con "Crear contacto nuevo".

## ⚠️ PENDIENTE de rellenar (2 sitios, mismos datos)

1. `index.html` → objeto `DATOS` al final (cargo + móvil).
2. `erik-tomas.vcf` → líneas `TITLE:` y `TEL;TYPE=CELL:`.

El móvil va SIN espacios y con prefijo: `+34612345678`.

## Probar en local

```
cd C:\Users\etomas\Desktop\tarjeta-visita
py -m http.server 8001
```
→ `http://localhost:8001/` (desde el iPhone en la misma wifi: `http://IP-DEL-PC:8001/`).
Ojo: el botón "Guardar contacto" solo abre la ficha bonita en iPhone si se sirve
por web (no abriendo el archivo con doble clic).

## Publicación (GitHub Pages)

Publicada en **https://eriktomas.github.io/tarjeta-visita/** desde el repo
`github.com/eriktomas/tarjeta-visita` (rama `main`, raíz). Esa URL es la que va
grabada en el sticker NFC (NFC Tools, registro tipo URL).

Si algún dato cambia, NO hay que regrabar el sticker (solo guarda la URL):
editar los 2 archivos, `git add . && git commit && git push` y en ~1 minuto
la web se actualiza sola.
