# Referencia Rápida de UIKit

Una guía de consulta rápida para los componentes y utilidades más usados.

## CDN - Copia y Pega

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/uikit@3/dist/css/uikit.min.css">
<script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit-icons.min.js"></script>
```

## Componentes Más Usados

### Botón
```html
<button class="uk-button uk-button-primary">Primary</button>
<button class="uk-button uk-button-default">Default</button>
<button class="uk-button uk-button-danger">Danger</button>
```

### Card
```html
<div class="uk-card uk-card-default">
    <div class="uk-card-body">Contenido</div>
</div>
```

### Grid (3 Columnas)
```html
<div class="uk-grid" uk-grid>
    <div class="uk-width-1-3">Col 1</div>
    <div class="uk-width-1-3">Col 2</div>
    <div class="uk-width-1-3">Col 3</div>
</div>
```

### Modal
```html
<button uk-toggle="target: #modal">Abrir</button>
<div id="modal" uk-modal>
    <div class="uk-modal-dialog">
        <!-- Contenido -->
    </div>
</div>
```

### Alertas
```html
<div class="uk-alert-success" uk-alert>Success</div>
<div class="uk-alert-warning" uk-alert>Warning</div>
<div class="uk-alert-danger" uk-alert>Danger</div>
```

### Formulario Completo

Estructura básica de un formulario con validación:

```html
<form>
    <div class="uk-margin">
        <label class="uk-form-label">Nombre</label>
        <input class="uk-input" type="text" required>
    </div>
    
    <div class="uk-margin">
        <label class="uk-form-label">Email</label>
        <input class="uk-input" type="email" required>
    </div>
    
    <div class="uk-margin">
        <label class="uk-form-label">Mensaje</label>
        <textarea class="uk-textarea" rows="4" required></textarea>
    </div>
    
    <div class="uk-margin">
        <label>
            <input class="uk-checkbox" type="checkbox" required>
            Acepto términos
        </label>
    </div>
    
    <button class="uk-button uk-button-primary">Enviar</button>
</form>
```

### Formulario
```html
<form>
    <input class="uk-input" type="text">
    <textarea class="uk-textarea"></textarea>
    <select class="uk-select">
        <option>Option</option>
    </select>
    <button class="uk-button uk-button-primary">Submit</button>
</form>
```

## Utilidades Esenciales

### Espaciado
```html
<div class="uk-margin">Margin</div>
<div class="uk-padding">Padding</div>
<div class="uk-margin-large">Margin grande</div>
```

### Texto
```html
<p class="uk-text-center">Centrado</p>
<p class="uk-text-bold">Negrita</p>
<p class="uk-text-primary">Color primary</p>
<p class="uk-text-small">Pequeño</p>
```

### Flexbox
```html
<div class="uk-flex uk-flex-center">Centrado horizontalmente</div>
<div class="uk-flex uk-flex-middle">Centrado verticalmente</div>
<div class="uk-flex uk-flex-between">Espacio entre items</div>
```

### Ancho
```html
<div class="uk-width-1-2">50%</div>
<div class="uk-width-1-3">33.33%</div>
<div class="uk-width-1-4">25%</div>
<div class="uk-width-auto">Auto</div>
```

## Breakpoints Responsive

Añade a tus clases para hacer responsive:

```html
<!-- Mostrar solo en mobile -->
<div class="uk-hidden@m">Mobile</div>

<!-- Grid responsivo -->
<div class="uk-width-1-1 uk-width-1-2@m uk-width-1-4@l">
    Responsivo: 100% mobile, 50% tablet, 25% desktop
</div>
```

Breakpoints:
- `@s` - Small (≥640px)
- `@m` - Medium (≥960px)  
- `@l` - Large (≥1200px)
- `@xl` - Extra Large (≥1600px)

## Patrones Comunes

### Navbar Básica
```html
<nav class="uk-navbar-container" uk-navbar>
    <div class="uk-navbar-left">
        <div class="uk-navbar-item"><h3>Logo</h3></div>
    </div>
    <div class="uk-navbar-right">
        <ul class="uk-navbar-nav">
            <li class="uk-active"><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
        </ul>
    </div>
</nav>
```

### Hero Section
```html
<div style="background: linear-gradient(135deg, #667eea, #764ba2); color: white; padding: 100px 20px; text-align: center;">
    <h1>Bienvenido</h1>
    <p>Descripción corta</p>
    <button class="uk-button uk-button-default">CTA</button>
</div>
```

### Card con Imagen
```html
<div class="uk-card uk-card-default">
    <div class="uk-card-media-top">
        <img src="image.jpg" alt="">
    </div>
    <div class="uk-card-body">
        <h3 class="uk-card-title">Título</h3>
        <p>Descripción</p>
    </div>
</div>
```

### Layout con Sidebar
```html
<div class="uk-grid" uk-grid>
    <div class="uk-width-2-3@m">
        <!-- Contenido principal -->
    </div>
    <div class="uk-width-1-3@m">
        <!-- Sidebar -->
    </div>
</div>
```

## Atributos Especiales

```html
<!-- Toggle para modales, dropdowns -->
uk-toggle="target: #id"

<!-- Grid automático -->
uk-grid

<!-- Alertas cerrable -->
uk-alert

<!-- Navbar -->
uk-navbar

<!-- Modal -->
uk-modal
```

## Variables CSS Personalizables

```css
:root {
    --uk-primary: #1e87f0;
    --uk-secondary: #222;
    --uk-success: #32d296;
    --uk-warning: #fbc02d;
    --uk-danger: #f0506e;
    --uk-global-font-size: 16px;
}
```

## Recursos Útiles

- Sitio Oficial: https://getuikit.com
- Documentación: https://getuikit.com/docs
- Componentes: https://getuikit.com/docs/components
- Utilidades: https://getuikit.com/docs/utility
- GitHub: https://github.com/uikit/uikit

## Tips Rápidos

1. Siempre usa `uk-container` para centrar contenido
2. El atributo `uk-grid` es obligatorio en grids
3. Usa `uk-width-*@breakpoint` para responsive
4. Combina utilidades para layouts complejos
5. Los modales necesitan un ID único
6. Las alertas cerrable necesitan `uk-alert`
7. Los dropdowns necesitan `uk-dropdown`

## Template Inicial

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/uikit@3/dist/css/uikit.min.css">
    <title>Mi Página</title>
</head>
<body>
    <div class="uk-container uk-padding">
        <h1>Hola UIKit!</h1>
        <p>Comienza a crear aquí</p>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit-icons.min.js"></script>
</body>
</html>
```

---

**Última actualización**: April 17, 2024
**Versión UIKit**: 3.x
