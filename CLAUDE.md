# CLAUDE.md

Guía para agentes que editen este repo. Ver también `README.md` para deploy y contexto general.

## Qué es esto

Landing estática de un solo archivo (`index.html`), sin build step, sin dependencias, sin framework.
Todo el HTML, CSS y JS vive en ese único archivo. `bienvenida-ia-abogados-v14.html` es una versión
anterior que se conserva como referencia — no editarla salvo que se pida explícitamente.

## Dónde están las cosas en `index.html`

- Vista principal (`#view-main`): headline + nav `.quiero` con 3 botones numerados (01, 02, 03) +
  botón CTA "Empezar mi proceso de onboarding".
- Vista onboarding (`#view-onboarding`): se muestra al hacer click en el CTA (toggle por JS via
  `data-go`, sin routing real). Contiene los botones `.commbtn` a WhatsApp y Circle.
- El cambio de vista es puramente CSS/JS (`.view.is-active`), no hay navegación de URL.

## Editando links

Los links que cambian con frecuencia (programa de clases, contacto, grupos de WhatsApp/Circle por
cohorte) son simples atributos `href` en tags `<a>`. Para cambiar uno:

1. Ubicarlo por el texto visible (`qtext` o `commlabel`), no por posición.
2. Reemplazar solo el `href`, no tocar estructura, clases ni SVGs.
3. Si es un link `wa.me`/`api.whatsapp.com` con mensaje precargado, el texto va URL-encoded — no
   reescribir a mano, generar el encoding correcto.
4. Actualizar la tabla "Enlaces que suelen cambiar" en `README.md` si cambia qué representa cada botón
   (no hace falta si solo cambia la URL de un botón existente).

## Convenciones

- Sin comentarios salvo que aclaren algo no obvio (ya se sigue así en el archivo).
- No introducir build tools, frameworks ni dependencias — el punto de este sitio es ser deploy directo.
- Mantener el archivo como una sola pieza autocontenida (inline CSS/JS), como está ahora.

## Deploy

Ver `README.md` — Netlify, `netlify deploy --prod --dir=.` o deploy continuo conectando el repo.
