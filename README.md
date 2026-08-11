# Padel Argentina

Sitio web estático dedicado a la venta de paletas y artículos de pádel.
Proyecto del curso de Desarrollo Web de Coderhouse (Módulos 1 al 5).

## Sitio desplegado

🔗 **[Ver sitio en vivo](https://mateoimpini.github.io/PadelArgentina9/)**

## Tecnologías

- HTML5 semántico
- **Sass (SCSS)**: arquitectura de partials con `@use`, variables, mixins,
  nesting y el operador `&`
- CSS3 (Flexbox y CSS Grid), compilado desde SCSS
- [Bootstrap 5.3](https://getbootstrap.com/) (navbar, carousel y modales)
- Google Fonts (Roboto)

## Estructura del proyecto

```
padel-argentina/
├── index.html                  # Página de inicio
├── pages/
│   ├── ofertas.html            # Promociones y descuentos
│   ├── productos.html          # Catálogo de paletas y accesorios
│   ├── sobrenosotros.html      # Información sobre la empresa
│   └── contactos.html          # Datos de contacto
├── scss/                       # Código fuente de estilos (Sass)
│   ├── main.scss               # Único punto de entrada (@use)
│   ├── utilities/
│   │   ├── _variables.scss     # Paleta, tokens y breakpoints ($)
│   │   └── _mixins.scss        # Mixins (flex-columna, responsive)
│   ├── base/
│   │   ├── _base.scss          # Reset y estilos globales a etiquetas
│   │   └── _tipografia.scss    # Jerarquía de títulos y textos
│   ├── layout/
│   │   ├── _header.scss        # Navbar y marca
│   │   ├── _nav.scss           # Enlaces de navegación y foco
│   │   ├── _grid.scss          # Grillas (home, catálogo, nosotros, contacto)
│   │   ├── _footer.scss        # Pie de página
│   │   └── _responsive.scss    # Escalera responsiva (media queries)
│   └── components/
│       ├── _hero.scss          # Portada de la home
│       ├── _cards.scss         # Tarjetas de producto
│       ├── _buttons.scss       # Botón de detalle y badge de descuento
│       ├── _carousel.scss      # Carousel de Bootstrap
│       ├── _modal.scss         # Modal de detalle
│       └── _forms.scss         # Formulario y datos de contacto
├── styles/
│   └── style.css               # CSS COMPILADO (generado por Sass, no editar)
├── assets/                     # Recursos multimedia (imágenes, íconos)
└── README.md
```

## Estilos: arquitectura SCSS

Todo el diseño nace de archivos `.scss` bajo `scss/`. El archivo
`styles/style.css` es **solo el resultado de la compilación** (no se edita a
mano). El punto de entrada es `scss/main.scss`, que orquesta los partials con
`@use`. Los valores repetidos (colores, medidas, breakpoints) se definen una
sola vez en `scss/utilities/_variables.scss` y se reutilizan en todo el proyecto.

### Compilar los estilos

Requiere [Sass](https://sass-lang.com/install). Con la CLI de Dart Sass
(no necesita Node) o con el paquete npm:

```bash
# Compilación única
sass scss/main.scss styles/style.css

# Modo watch (recompila al guardar)
sass --watch scss/main.scss styles/style.css
```

Si tenés Node instalado, también podés usar los scripts del `package.json`:

```bash
npm install
npm run build:css      # compila una vez
npm run watch:css      # modo watch
```

## Responsividad

El sitio está maquetado mobile-first y es 100% responsivo en las cinco páginas,
adaptado a mobile, tablet y desktop mediante media queries, sin scroll horizontal
ni compresión de elementos.

## Cómo verlo localmente

Clonar el repositorio y abrir `index.html` en el navegador:

```bash
git clone https://github.com/MateoImpini/PadelArgentina9.git
cd PadelArgentina9
```
