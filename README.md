# Mini-portafolio · Sebastián Ulloa

Portafolio web personal con estética **Windows 3.1 (File Manager)**, creado como parte de la Evaluación 2 de ICINF1107 en la Universidad Católica de Temuco (UCT).

## Descripción

Sitio de una sola página que presenta a su autor, estudiante de Ingeniería Civil en Informática, y sus trabajos del semestre. Está pensado para que un **reclutador o docente** encuentre rápido quién es el autor, qué ha hecho y cómo contactarlo.

El sitio tiene tres secciones, en este orden:

1. **Presentación personal:** quién soy y qué estudio.
2. **Contacto:** enlaces a GitHub y correo.
3. **Prácticas:** tabla con los trabajos del semestre, su descripción y el enlace al código.

## Tecnologías

- **HTML5** con estructura semántica (`header`, `nav`, `main`, `section`, `footer`).
- **CSS3** en un archivo externo, con variables, Flexbox y *media queries*.
- Sin frameworks ni librerías externas.

## Estructura del proyecto

```
mini-portafolio/
├── index.html
├── css/
│   └── styles.css
├── img/
│   └── icon.png
└── README.md
```

## Capturas

> Reemplaza estas rutas por tus capturas reales (guárdalas en `img/`).

| Móvil | Tablet | Escritorio |
|-------|--------|------------|
| ![Vista móvil](img/captura-movil.png) | ![Vista tablet](img/captura-tablet.png) | ![Vista escritorio](img/captura-escritorio.png) |

## Cómo abrirlo

**Opción 1: local**

1. Clona el repositorio:
   ```bash
   git clone https://github.com/TU-USUARIO/NOMBRE-DEL-REPO.git
   ```
2. Abre la carpeta del proyecto.
3. Haz doble clic en `index.html` para verlo en tu navegador.

**Opción 2: GitHub Pages**

Si el sitio está publicado, puedes verlo en: `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`

## Decisiones de diseño

### Audiencia
El portafolio está dirigido a reclutadores y docentes, que suelen revisar muchos perfiles en poco tiempo. Por eso la información está en tres bloques cortos y el menú permite saltar directamente a cada uno.

### Estructura y semántica
- Cada parte de la página usa la etiqueta que le corresponde: `header` para el título y la navegación, `main` para el contenido, `section` para cada bloque y `footer` para el cierre.
- Los encabezados siguen una jerarquía ordenada: un `h1` (UCT) y un `h2` por sección.
- El orden del HTML (Presentación → Contacto → Prácticas) coincide con el orden visual y con el del menú, para que el recorrido con teclado o lector de pantalla sea coherente.
- Las prácticas se presentan en una `table` con `caption` y `th scope="col"`, porque son datos con las mismas columnas (nombre, descripción y enlace).

### Jerarquía visual
- Las barras de título azules (`#000080`) con texto blanco marcan el inicio de cada ventana y guían la lectura.
- Una sola columna y espaciado generoso evitan que los elementos compitan por la atención.
- Los datos clave (nombre y carrera) están en negrita y color azul dentro del texto.

### Diseño responsivo
Se usó un enfoque *mobile-first* con tres puntos de quiebre:

| Punto de quiebre | Ancho | Cambios principales |
|------------------|-------|---------------------|
| Móvil | menos de 600px | Imagen centrada sobre el texto; título y carrera apilados en la barra. |
| Tablet | desde 600px | Imagen a la izquierda con el texto a su lado; carrera a la derecha del título. |
| Escritorio | desde 1024px | Tipografía y espaciados más grandes; imagen de mayor tamaño. |

La tabla de prácticas está dentro de un contenedor con `overflow-x: auto`, de modo que en pantallas pequeñas se desplaza horizontalmente sin romper el diseño.

### Accesibilidad
- Contraste alto: texto blanco sobre azul `#000080` y negro sobre blanco o gris.
- Foco visible al navegar con teclado: los enlaces se resaltan con fondo amarillo y contorno negro.
- Imagen con texto alternativo (`alt`).
- Idioma de la página declarado (`lang="es"`).
- Los elementos decorativos (el cuadrito del menú de sistema) se generan con CSS y no se leen en lectores de pantalla.

### Estética
La referencia visual es el File Manager de Windows 3.1: gris `#c0c0c0` como fondo, biseles claros y oscuros, barras de título azules y una barra de estado como pie de página. El menú de navegación hace el papel de la barra de menú (*File, Disk, Tree...*) y cada sección es una ventana.

## Dificultades y aprendizajes

- Adaptar una tabla a pantallas pequeñas obligó a usar un contenedor con desplazamiento horizontal.
- Mantener el orden del HTML igual al orden visual, en lugar de reordenar solo con CSS, mejora la accesibilidad.
- Elegir colores con contraste suficiente respetando el estilo retro.

## Mejoras futuras

- Cambio de tema claro/oscuro con un botón.
- Formulario de contacto con etiquetas (`label`) en lugar de enlaces directos.
- Más prácticas en la tabla, con capturas de cada proyecto.

## Autor

**Sebastián Henry Ulloa Barrientos**
Estudiante de Ingeniería Civil en Informática, UCT, Temuco.
