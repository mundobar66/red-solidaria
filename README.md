# Red Solidaria — Panel de Coordinación

Web estática (sin backend), pensada para publicarse en GitHub Pages igual que
`tasazo-guadarrama`. Sirve para centralizar la información de las campañas
activas en un único enlace, mientras WhatsApp se sigue usando para avisos urgentes.

## Estructura

```
red-solidaria/
├── index.html                     → portada con los proyectos activos
├── proyecto-fauna-incendios.html  → campaña de ayuda a la fauna
├── proyecto-agua-tiemblo.html     → campaña de agua en El Tiemblo
└── assets/
    ├── style.css
    └── logos/                     → logos de las asociaciones
```

## Cómo publicarlo (igual que hiciste con tasazo-guadarrama)

1. Crea un repositorio nuevo en tu cuenta de GitHub, por ejemplo `red-solidaria`.
2. Sube el contenido de esta carpeta a la raíz del repo (puedes arrastrar los
   archivos desde la web de GitHub, sin necesidad de terminal).
3. Ve a **Settings → Pages**, y en "Source" selecciona la rama `main` y
   carpeta `/ (root)`.
4. En un par de minutos tu web estará en:
   `https://mundobar66.github.io/red-solidaria/`

## Cómo actualizar los datos

No hay base de datos: cada vez que cambie una necesidad, un punto de recogida
o un teléfono, edita el `.html` del proyecto correspondiente directamente en
GitHub (botón del lápiz ✏️ en cada archivo) y confirma el cambio ("Commit
changes"). La web se actualiza sola en menos de un minuto.

## Añadir un proyecto nuevo

1. Duplica `proyecto-fauna-incendios.html`, cámbiale el nombre
   (ej. `proyecto-nombre.html`) y edita el contenido.
2. Añade una tarjeta nueva en `index.html`, dentro de `<div class="proyectos">`,
   enlazando al archivo que acabas de crear.

## Formularios públicos (voluntario, vehículo, donación, necesidad)

El brief original pedía formularios públicos con validación antes de publicar.
La forma más rápida de tenerlos ya, sin programar un backend, es usar
Google Forms (gratis, y tú ya sabes montarlos porque `tasazo-guadarrama` los usa):

1. Crea un Google Form por tipo de formulario (voluntario, vehículo, punto de
   recogida, donación, necesidad).
2. Pega el enlace del formulario en el `.html` del proyecto correspondiente
   (busca el comentario `<!-- ADMIN -->` en `proyecto-agua-tiemblo.html` como
   referencia de dónde añadirlo).
3. Revisas las respuestas en la hoja de cálculo del Form antes de publicar
   nada en la web — así mantienes el principio de "ningún dato se publica
   automáticamente" del brief.

## Pendiente de decidir más adelante

Si en algún momento esto crece (varios administradores, historial de cambios,
exportaciones automáticas, notificaciones push), habrá que pasar de esta web
estática a una aplicación real con backend y base de datos. Para el uso
inmediato de estas dos campañas, esta versión es suficiente y no tiene coste
ni mantenimiento técnico.
