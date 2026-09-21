# Sitio de Splitline

Las páginas públicas de la app: características, preguntas frecuentes, soporte y política de
privacidad. **El código de la app no está aquí** — vive en un repositorio privado aparte. Este
repositorio es público solo porque GitHub Pages no sirve repositorios privados en el plan gratuito,
y las dos URLs tienen que ser accesibles para Apple y para quien use la app.

## Publicación

GitHub Pages, sirviendo desde la raíz de `main`:
**Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)`**

Un push a `main` republica en un par de minutos.

## Para qué sirve cada URL

| Página | Campo de App Store Connect |
|---|---|
| `index.html` | Support URL |
| `privacidad.html` | Privacy Policy URL |

Las dos tienen que cargar sin pedir acceso: Apple las abre durante la revisión.

## Al tocar la política

Si cambia lo que la app hace con los datos, hay que actualizar **tres sitios a la vez** o dejan de
coincidir, que es exactamente lo que Apple busca:

1. La fecha de vigor y el texto de `privacidad.html`.
2. Las etiquetas de privacidad de la ficha en App Store Connect.
3. `PrivacyInfo.xcprivacy` en el repositorio de la app.

## Sin dependencias

HTML y CSS a mano. No hay build, ni generador de sitios, ni paquetes que actualizar. Se edita el
fichero y se hace push.
