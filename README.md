# Resuelto

Sitio web de **Resuelto** — agencia de Inteligencia Artificial y Automatización para
E-commerce, Medios y Creadores de Contenido.

🌐 **En vivo:** [reviu.com.ar](https://reviu.com.ar)

> **Nota sobre el nombre:** la empresa se llama **Resuelto**, pero el sitio se
> sigue accediendo por el dominio `reviu.com.ar` (el nombre anterior). El dominio
> y el correo de contacto no cambian: solo cambió la marca que se muestra.

## Qué hay en este repo

| Archivo / carpeta  | Qué es                                                              |
| ------------------ | ------------------------------------------------------------------- |
| `index.html`       | La página principal completa (navegación, hero, servicios, casos, método, contacto) |
| `legal/index.html` | Política de Privacidad y Términos del Servicio                       |
| `CNAME`            | Dominio propio del sitio: `reviu.com.ar`                             |
| `.gitattributes`   | Configuración de Git para el manejo de archivos de texto             |

## Cómo está hecho

Es un sitio **estático**: no necesita servidor, base de datos ni proceso de build.
Todo el HTML, los estilos y el poco JavaScript que usa viven dentro de `index.html`.

Las herramientas se cargan directamente desde internet (CDN), así que no hay
`npm install` ni dependencias que instalar:

- **[Tailwind CSS](https://tailwindcss.com/)** — los estilos y el diseño responsive
- **[Lucide](https://lucide.dev/)** — los íconos
- **[Google Fonts](https://fonts.google.com/specimen/Inter)** — la tipografía Inter

### Colores de marca

Definidos en el bloque `tailwind.config` dentro de `index.html`:

| Nombre        | Color     | Uso                          |
| ------------- | --------- | ---------------------------- |
| `dark`        | `#0B1120` | Fondo principal              |
| `card`        | `#1E293B` | Fondo de tarjetas            |
| `accent`      | `#D4AF37` | Dorado — botones y destacados |
| `accentHover` | `#B3932E` | Dorado al pasar el mouse     |

## Cómo verlo en tu computadora

No hace falta instalar nada: alcanza con abrir `index.html` con doble clic en el navegador.

Si preferís levantarlo en un servidor local (recomendado para que las rutas
funcionen igual que en producción):

```bash
python3 -m http.server 8000
```

Y después entrá a <http://localhost:8000>.

## Cómo publicar cambios

El sitio se publica solo con **GitHub Pages**: cada cambio que llega a la rama
principal (`main`) queda online en `reviu.com.ar` en un par de minutos.

```bash
git add .
git commit -m "Descripción del cambio"
git push
```
