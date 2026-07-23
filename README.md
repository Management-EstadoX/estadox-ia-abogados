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

Ambos viven dentro del bloque de onboarding en `index.html`:

- Grupo de WhatsApp (`chat.whatsapp.com/...`)
- Invitación a la comunidad de Circle (`estadox.circle.so/join?invitation_token=...`)
