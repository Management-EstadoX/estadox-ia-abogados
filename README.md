# estadox-ia-abogados

Landing de bienvenida / onboarding del programa **IA para Abogados** (Estadox).

Sitio estático de un solo archivo, sin build step.

## Archivos

- `index.html` — la página en producción.
- `bienvenida-ia-abogados-v14.html` — versión anterior, se conserva como referencia.

## Deploy

Publicado en Netlify: https://estadox-ia-abogados.netlify.app

Para desplegar desde esta carpeta con el CLI de Netlify:

```bash
netlify link      # solo la primera vez
netlify deploy --prod --dir=.
```

Alternativamente se puede conectar este repo a Netlify para deploy continuo:
publish directory = `.`, sin build command.

## Enlaces que suelen cambiar

Todos viven en `index.html`, dentro del nav `.quiero` (vista principal) o del bloque `.comm` (vista de onboarding):

- Programa de clases (Google Drive, item 01 del nav `.quiero`)
- Contacto/grupo de WhatsApp de la cohorte activa (item 02 del nav `.quiero`)
- Grupo de WhatsApp de la comunidad general (`chat.whatsapp.com/...`, vista de onboarding)
- Invitación a la comunidad de Circle (`estadox.circle.so/join?invitation_token=...`, vista de onboarding)
