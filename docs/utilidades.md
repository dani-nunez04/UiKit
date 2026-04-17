# Utilidades en UIKit

Las utilidades son clases de CSS que facilitan estilos comunes sin necesidad de escribir CSS personalizado.

## Espaciado (Margin & Padding)

### Margin

```html
<!-- Margin en todos los lados -->
<div class="uk-margin">Margin estándar</div>
<div class="uk-margin-small">Margin pequeño</div>
<div class="uk-margin-medium">Margin mediano</div>
<div class="uk-margin-large">Margin grande</div>
<div class="uk-margin-xlarge">Margin extra grande</div>

<!-- Margin en lados específicos -->
<div class="uk-margin-top">Margin superior</div>
<div class="uk-margin-bottom">Margin inferior</div>
<div class="uk-margin-left">Margin izquierdo</div>
<div class="uk-margin-right">Margin derecho</div>

<!-- Quitar margin -->
<div class="uk-margin-remove">Sin margin</div>
```

### Padding

```html
<!-- Padding en todos los lados -->
<div class="uk-padding">Padding estándar</div>
<div class="uk-padding-small">Padding pequeño</div>
<div class="uk-padding-medium">Padding mediano</div>
<div class="uk-padding-large">Padding grande</div>

<!-- Padding en lados específicos -->
<div class="uk-padding-top">Padding superior</div>
<div class="uk-padding-bottom">Padding inferior</div>
```

## Texto

### Alineación

```html
<p class="uk-text-left">Texto alineado a la izquierda</p>
<p class="uk-text-center">Texto centrado</p>
<p class="uk-text-right">Texto alineado a la derecha</p>
<p class="uk-text-justify">Texto justificado</p>
```

### Tamaño

```html
<!-- Tamaños -->
<p class="uk-text-small">Texto pequeño</p>
<p>Texto normal</p>
<p class="uk-text-large">Texto grande</p>

<!-- Responsive -->
<p class="uk-text-small@m">Pequeño en mobile, normal en desktop</p>
```

### Estilo

```html
<p class="uk-text-bold">Texto en negrita</p>
<p class="uk-text-italic">Texto en cursiva</p>
<p class="uk-text-underline">Texto subrayado</p>
<p class="uk-text-line-through">Texto tachado</p>

<!-- Capitalización -->
<p class="uk-text-uppercase">TEXTO EN MAYÚSCULAS</p>
<p class="uk-text-lowercase">texto en minúsculas</p>
<p class="uk-text-capitalize">Texto Con Primera Mayúscula</p>
```

## Colores

### Colores de Texto

```html
<p class="uk-text-primary">Texto Primary</p>
<p class="uk-text-secondary">Texto Secondary</p>
<p class="uk-text-success">Texto Success</p>
<p class="uk-text-warning">Texto Warning</p>
<p class="uk-text-danger">Texto Danger</p>
<p class="uk-text-muted">Texto Muted</p>
```

### Colores de Fondo

```html
<div class="uk-padding uk-background-primary">Fondo Primary</div>
<div class="uk-padding uk-background-secondary">Fondo Secondary</div>

<!-- Alternativa usando divs coloreados -->
<div style="background: #1e87f0; padding: 20px; color: white;">
    Fondo personalizado
</div>
```

## Flexbox

### Display y Alineación

```html
<!-- Flex display -->
<div class="uk-flex">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>

<!-- Alineación horizontal -->
<div class="uk-flex uk-flex-center">Centro horizontal</div>
<div class="uk-flex uk-flex-between">
    <div>Izquierda</div>
    <div>Derecha</div>
</div>
<div class="uk-flex uk-flex-around">Espaciado alrededor</div>

<!-- Alineación vertical -->
<div class="uk-flex uk-flex-middle" style="height: 200px;">
    Centro vertical
</div>

<!-- Dirección -->
<div class="uk-flex-column">Dirección columna</div>
<div class="uk-flex-row">Dirección fila</div>

<!-- Wrap -->
<div class="uk-flex uk-flex-wrap">Items con salto de línea</div>
```

## Visibilidad

```html
<!-- Hidden en todos los tamaños -->
<div class="uk-hidden">Siempre oculto</div>

<!-- Hidden en tamaños específicos -->
<div class="uk-hidden@m">Oculto en mobile</div>
<div class="uk-visible@m">Visible solo en mobile</div>

<!-- Mostrar solo en print -->
<div class="uk-print-inline">Solo en impresión</div>
```

## Display

```html
<!-- Block, Inline, Inline-block -->
<div class="uk-display-block">Block</div>
<div class="uk-display-inline">Inline</div>
<div class="uk-display-inline-block">Inline-block</div>

<!-- Tabla -->
<div class="uk-display-table">Display table</div>
```

## Bordes y Sombras

```html
<!-- Bordes -->
<div class="uk-border-rounded">Bordes redondeados</div>
<div class="uk-border-circle" style="width: 100px; height: 100px;">
    Círculo
</div>

<!-- Sombra -->
<div class="uk-box-shadow-small">Sombra pequeña</div>
<div class="uk-box-shadow-medium">Sombra mediana</div>
<div class="uk-box-shadow-large">Sombra grande</div>
<div class="uk-box-shadow-xlarge">Sombra extra grande</div>

<!-- Hover shadow -->
<div class="uk-box-shadow-hover-small">Sombra al pasar</div>
```

## Ancho y Alto

```html
<!-- Ancho -->
<div class="uk-width-1-1">100%</div>
<div class="uk-width-1-2">50%</div>
<div class="uk-width-1-3">33.33%</div>
<div class="uk-width-1-4">25%</div>

<!-- Responsive -->
<div class="uk-width-1-1 uk-width-1-2@m uk-width-1-4@l">
    Responsive width
</div>

<!-- Auto -->
<div class="uk-width-auto">Ancho automático</div>
```

## Overflow

```html
<!-- Scroll si se desborda -->
<div class="uk-overflow-auto" style="width: 200px;">
    Contenido que puede desbordarse
</div>

<!-- Ocultar overflow -->
<div class="uk-overflow-hidden">
    Contenido oculto si desborda
</div>
```

## Posición

```html
<!-- Position absolute -->
<div style="position: relative;">
    <div class="uk-position-absolute">Absoluto</div>
</div>

<!-- Esquinas específicas -->
<div class="uk-position-top-right">Top Right</div>
<div class="uk-position-bottom-left">Bottom Left</div>

<!-- Centro -->
<div class="uk-position-center">Centrado</div>
```

## Ejemplos Prácticos

### Card Mejorada con Utilidades

```html
<div class="uk-card uk-card-default uk-border-rounded uk-box-shadow-medium uk-margin">
    <div class="uk-card-media-top">
        <img src="image.jpg" alt="">
    </div>
    <div class="uk-card-body uk-padding-large">
        <h3 class="uk-card-title uk-text-bold">Título Importante</h3>
        <p class="uk-text-secondary uk-margin-small-top">
            Descripción del contenido...
        </p>
    </div>
    <div class="uk-card-footer uk-padding uk-background-secondary">
        <button class="uk-button uk-button-primary uk-width-1-1">
            Acción Principal
        </button>
    </div>
</div>
```

### Layout con Sidebar

```html
<div class="uk-grid" uk-grid>
    <!-- Contenido principal -->
    <div class="uk-width-2-3@m">
        <div class="uk-padding uk-background-primary uk-text-white uk-border-rounded">
            <h2>Contenido Principal</h2>
            <p>Lorem ipsum dolor sit amet...</p>
        </div>
    </div>
    
    <!-- Sidebar -->
    <div class="uk-width-1-3@m">
        <div class="uk-padding uk-background-secondary uk-border-rounded">
            <h3 class="uk-text-bold">Widget</h3>
            <ul class="uk-list">
                <li><a href="#">Opción 1</a></li>
                <li><a href="#">Opción 2</a></li>
            </ul>
        </div>
    </div>
</div>
```

---

Para más utilidades, consulta la [documentación oficial de Utilidades](https://getuikit.com/docs/utility).
