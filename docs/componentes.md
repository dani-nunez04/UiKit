# Componentes de UIKit

UIKit proporciona una variedad de componentes preconstructidos para acelerar el desarrollo.

## Botones

### Tipos de Botón

```html
<!-- Default -->
<button class="uk-button uk-button-default">Default</button>

<!-- Primary -->
<button class="uk-button uk-button-primary">Primary</button>

<!-- Secondary -->
<button class="uk-button uk-button-secondary">Secondary</button>

<!-- Danger -->
<button class="uk-button uk-button-danger">Danger</button>

<!-- Text (Enlace como botón) -->
<button class="uk-button uk-button-text">Text</button>
```

### Tamaños de Botón

```html
<!-- Pequeño -->
<button class="uk-button uk-button-small">Small</button>

<!-- Default (normal) -->
<button class="uk-button">Normal</button>

<!-- Grande -->
<button class="uk-button uk-button-large">Large</button>
```

### Botones Especiales

```html
<!-- Botón deshabilitado -->
<button class="uk-button uk-button-primary" disabled>Disabled</button>

<!-- Botón con ícono -->
<button class="uk-button uk-button-primary">
    <span uk-icon="icon: download"></span>
    Descargar
</button>

<!-- Grupo de botones -->
<div class="uk-button-group">
    <button class="uk-button uk-button-default">Izquierda</button>
    <button class="uk-button uk-button-default">Centro</button>
    <button class="uk-button uk-button-default">Derecha</button>
</div>
```

## Cards (Tarjetas)

### Card Básica

```html
<div class="uk-card uk-card-default">
    <div class="uk-card-body">
        <h3 class="uk-card-title">Título de la Tarjeta</h3>
        <p>Contenido de la tarjeta...</p>
    </div>
</div>
```

### Card con Imagen

```html
<div class="uk-card uk-card-default">
    <div class="uk-card-media-top">
        <img src="image.jpg" alt="Imagen">
    </div>
    <div class="uk-card-body">
        <h3 class="uk-card-title">Título</h3>
        <p>Descripción...</p>
    </div>
    <div class="uk-card-footer">
        <button class="uk-button uk-button-text">Acción</button>
    </div>
</div>
```

### Variantes de Card

```html
<!-- Card Primary -->
<div class="uk-card uk-card-primary">
    <div class="uk-card-body">...</div>
</div>

<!-- Card Secondary -->
<div class="uk-card uk-card-secondary">
    <div class="uk-card-body">...</div>
</div>

<!-- Card Hover (efecto al pasar mouse) -->
<div class="uk-card uk-card-hover">
    <div class="uk-card-body">...</div>
</div>
```

## Formularios

### Input Básico

```html
<div class="uk-margin">
    <label class="uk-form-label">Email</label>
    <input class="uk-input" type="email" placeholder="ejemplo@email.com">
</div>
```

### Textarea

```html
<div class="uk-margin">
    <label class="uk-form-label">Mensaje</label>
    <textarea class="uk-textarea" rows="5"></textarea>
</div>
```

### Select

```html
<div class="uk-margin">
    <label class="uk-form-label">Opción</label>
    <select class="uk-select">
        <option>Opción 1</option>
        <option>Opción 2</option>
        <option>Opción 3</option>
    </select>
</div>
```

### Checkbox y Radio

```html
<!-- Checkbox -->
<div class="uk-margin">
    <label>
        <input class="uk-checkbox" type="checkbox">
        Aceptar términos
    </label>
</div>

<!-- Radio -->
<div class="uk-margin">
    <label>
        <input class="uk-radio" type="radio" name="grupo">
        Opción A
    </label>
    <label>
        <input class="uk-radio" type="radio" name="grupo">
        Opción B
    </label>
</div>
```

## Alertas

```html
<!-- Alert Primary -->
<div class="uk-alert-primary" uk-alert>
    <a class="uk-alert-close" uk-close></a>
    <p>Este es un mensaje informativo.</p>
</div>

<!-- Alert Success -->
<div class="uk-alert-success" uk-alert>
    <p>¡La operación fue exitosa!</p>
</div>

<!-- Alert Warning -->
<div class="uk-alert-warning" uk-alert>
    <p>Advertencia: revisa esto antes de continuar.</p>
</div>

<!-- Alert Danger -->
<div class="uk-alert-danger" uk-alert>
    <p>Error: algo salió mal.</p>
</div>
```

## Navegación

### Navbar Básica

```html
<nav class="uk-navbar-container" uk-navbar>
    <div class="uk-navbar-left">
        <div class="uk-navbar-item">
            <h3>Logo</h3>
        </div>
    </div>
    <div class="uk-navbar-right">
        <ul class="uk-navbar-nav">
            <li class="uk-active"><a href="#">Inicio</a></li>
            <li><a href="#">Acerca de</a></li>
            <li><a href="#">Contacto</a></li>
        </ul>
    </div>
</nav>
```

### Lista de Navegación

```html
<ul class="uk-nav uk-nav-default">
    <li class="uk-active"><a href="#">Activo</a></li>
    <li><a href="#">Enlace</a></li>
    <li><a href="#">Enlace</a></li>
</ul>
```

## Modales

```html
<!-- Botón que abre el modal -->
<button class="uk-button uk-button-primary" uk-toggle="target: #modal-ejemplo">
    Abrir Modal
</button>

<!-- Modal -->
<div id="modal-ejemplo" class="uk-modal" uk-modal>
    <div class="uk-modal-dialog">
        <button class="uk-modal-close-default" type="button" uk-close></button>
        <div class="uk-modal-header">
            <h2 class="uk-modal-title">Título del Modal</h2>
        </div>
        <div class="uk-modal-body">
            <p>Contenido del modal...</p>
        </div>
        <div class="uk-modal-footer uk-text-right">
            <button class="uk-button uk-button-default uk-modal-close">
                Cancelar
            </button>
            <button class="uk-button uk-button-primary">Aceptar</button>
        </div>
    </div>
</div>
```

## Breadcrumbs

```html
<ul class="uk-breadcrumb">
    <li><a href="#">Inicio</a></li>
    <li><a href="#">Categoría</a></li>
    <li><span>Página Actual</span></li>
</ul>
```

## Paginación

```html
<ul class="uk-pagination">
    <li><a href="#">Anterior</a></li>
    <li class="uk-active"><span>1</span></li>
    <li><a href="#">2</a></li>
    <li><a href="#">3</a></li>
    <li><a href="#">Siguiente</a></li>
</ul>
```

## Badges

```html
<!-- Badge Primary -->
<span class="uk-badge">Primary</span>

<!-- Badge Rojo -->
<span class="uk-badge" style="background: #f0506e;">Danger</span>

<!-- En un botón -->
<button class="uk-button uk-button-default">
    Notificaciones
    <span class="uk-badge">5</span>
</button>
```

## Badges y Labels

```html
<!-- Label -->
<span class="uk-label">Label</span>

<!-- Label Warning -->
<span class="uk-label" style="background: #fbc02d;">Warning</span>
```

---

Para más componentes y variantes, consulta la [documentación oficial de Componentes](https://getuikit.com/docs/components).
