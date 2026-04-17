# Sistema de Grid en UIKit

El grid de UIKit es un sistema flexible basado en Flexbox que permite crear layouts responsivos de manera sencilla.

## Grid Básico

### Estructura

El grid es un sistema de layout basado en filas y columnas. La clase `uk-grid` activa el comportamiento responsivo.
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>
```

El atributo `uk-grid` es importante para que UIKit aplique el comportamiento responsivo correcto.

## Anchos de Columnas

UIKit proporciona clases para establecer el ancho de las columnas usando fracciones.

### Fracciones

```html
<!-- 1 columna al 50% -->
<div class="uk-width-1-2">50%</div>

<!-- 1 columna al 33.33% -->
<div class="uk-width-1-3">33%</div>

<!-- 1 columna al 25% -->
<div class="uk-width-1-4">25%</div>

<!-- 1 columna al 20% -->
<div class="uk-width-1-5">20%</div>
```

### Ejemplo: 3 Columnas Iguales

```html
<div class="uk-grid" uk-grid>
    <div class="uk-width-1-3">
        <div class="uk-card uk-card-default">
            <div class="uk-card-body">Columna 1</div>
        </div>
    </div>
    <div class="uk-width-1-3">
        <div class="uk-card uk-card-default">
            <div class="uk-card-body">Columna 2</div>
        </div>
    </div>
    <div class="uk-width-1-3">
        <div class="uk-card uk-card-default">
            <div class="uk-card-body">Columna 3</div>
        </div>
    </div>
</div>
```

## Responsive Breakpoints

UIKit permite cambiar el layout según el tamaño de pantalla usando sufijos de breakpoints.

- `@s` - Small (≥640px)
- `@m` - Medium (≥960px)
- `@l` - Large (≥1200px)
- `@xl` - Extra Large (≥1600px)

### Ejemplo: Adaptativo

```html
<div class="uk-grid" uk-grid>
    <!-- Mobile: full width, Medium+: 50%, Large+: 33% -->
    <div class="uk-width-1-2@m uk-width-1-3@l">
        Contenido adaptativo
    </div>
</div>
```

En este ejemplo:
- En móviles: ocupa 100% del ancho
- En tablets (≥960px): ocupa 50% del ancho
- En escritorio (≥1200px): ocupa 33.33% del ancho

## Espaciado Entre Items

Usa el atributo `uk-grid` con modificadores para controlar el espaciado:

```html
<!-- Grid pequeño -->
<div class="uk-grid" uk-grid="gutter: small">

<!-- Grid mediano (por defecto) -->
<div class="uk-grid" uk-grid="gutter: medium">

<!-- Grid grande -->
<div class="uk-grid" uk-grid="gutter: large">
```

O usa clases:

```html
<div class="uk-grid uk-grid-small" uk-grid>
    <!-- Espaciado pequeño -->
</div>

<div class="uk-grid uk-grid-large" uk-grid>
    <!-- Espaciado grande -->
</div>
```

## Alineación

### Alineación Vertical

```html
<!-- Centro vertical -->
<div class="uk-grid uk-grid-match" uk-grid="match: height">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>
```

### Alineación Horizontal

```html
<!-- Centrado horizontalmente -->
<div class="uk-flex uk-flex-center">
    <div>Contenido centrado</div>
</div>

<!-- Espaciado entre items -->
<div class="uk-flex uk-flex-between">
    <div>Izquierda</div>
    <div>Derecha</div>
</div>
```

## Grid Anidado

Puedes anidar grids dentro de grids:

```html
<div class="uk-grid" uk-grid>
    <div class="uk-width-1-2">
        <div class="uk-grid" uk-grid>
            <div class="uk-width-1-2">Anidado 1</div>
            <div class="uk-width-1-2">Anidado 2</div>
        </div>
    </div>
    <div class="uk-width-1-2">Lado Derecho</div>
</div>
```

## Ejemplos Prácticos

### Layout 2 Columnas

```html
<div class="uk-grid" uk-grid>
    <!-- Contenido principal (66.6%) -->
    <div class="uk-width-2-3@m">
        <h2>Artículo Principal</h2>
        <p>Contenido importante...</p>
    </div>
    
    <!-- Sidebar (33.3%) -->
    <div class="uk-width-1-3@m">
        <div class="uk-card uk-card-default">
            <div class="uk-card-body">
                <h4>Categorías</h4>
                <ul class="uk-list">
                    <li><a href="#">Categoría 1</a></li>
                    <li><a href="#">Categoría 2</a></li>
                </ul>
            </div>
        </div>
    </div>
</div>
```

### Blog Grid (3 Columnas)

```html
<div class="uk-grid uk-grid-large" uk-grid>
    <!-- Repetir para cada artículo -->
    <div class="uk-width-1-3@m">
        <div class="uk-card uk-card-hover">
            <div class="uk-card-media-top">
                <img src="image.jpg" alt="">
            </div>
            <div class="uk-card-body">
                <h3 class="uk-card-title">Título</h3>
                <p>Descripción del artículo...</p>
            </div>
            <div class="uk-card-footer">
                <a href="#" class="uk-button uk-button-text">Leer más</a>
            </div>
        </div>
    </div>
</div>
```

## Tips Importantes

1. **Siempre usa `uk-grid`**: Asegúrate de incluir el atributo `uk-grid` para comportamiento responsive correcto
2. **Usa breakpoints**: Aprovecha `@m`, `@l` etc. para diseños truly responsive
3. **Combina con otros componentes**: El grid funciona perfectamente con tarjetas, botones, etc.
4. **Considera el mobile-first**: Diseña primero para móvil, luego agrega cambios para pantallas más grandes

---

Para más información, consulta la [documentación oficial de Grid](https://getuikit.com/docs/grid).
