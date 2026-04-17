# Personalización de UIKit

UIKit es muy flexible y se puede personalizar de varias maneras para adaptarse a tu proyecto.

## 1. Variables CSS

La forma más simple de personalizar UIKit es usando variables CSS.

### Colores Principales

```css
:root {
    --uk-primary: #1e87f0;
    --uk-secondary: #222;
    --uk-success: #32d296;
    --uk-warning: #fbc02d;
    --uk-danger: #f0506e;
}
```

### Tamaños

```css
:root {
    --uk-global-font-size: 16px;
    --uk-global-line-height: 1.5;
    --uk-grid-gutter-h: 15px;
    --uk-grid-gutter-v: 15px;
}
```

### Ejemplo Completo

```html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" href="uikit.min.css">
    <style>
        :root {
            --uk-primary: #ff6b6b;
            --uk-secondary: #4ecdc4;
            --uk-text-muted: #95a5a6;
            --uk-global-font-size: 18px;
        }
    </style>
</head>
<body>
    <div class="uk-container">
        <button class="uk-button uk-button-primary">
            Mi botón personalizado
        </button>
    </div>
</body>
</html>
```

## 2. Sobrescribir Estilos

Puedes escribir CSS personalizado que sobrescriba los estilos de UIKit:

```css
/* Personalizar botones */
.uk-button-primary {
    background-color: #e74c3c;
    border-radius: 25px;
    font-weight: bold;
    padding: 12px 30px;
}

.uk-button-primary:hover {
    background-color: #c0392b;
}

/* Personalizar cards */
.uk-card-default {
    border: 2px solid #3498db;
    box-shadow: 0 4px 15px rgba(52, 152, 219, 0.15);
}

/* Personalizar alertas */
.uk-alert-primary {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
}
```

## 3. Clases Personalizadas

Crea tus propias clases para componentes recurrentes:

```css
/* Componente: Hero Section */
.hero-section {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 80px 20px;
    text-align: center;
    border-radius: 12px;
}

.hero-section h1 {
    font-size: 3em;
    font-weight: 700;
    margin-bottom: 20px;
}

.hero-section p {
    font-size: 1.3em;
    opacity: 0.9;
}

/* Componente: Card Mejorada */
.card-premium {
    background: white;
    border-radius: 12px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    overflow: hidden;
    transition: transform 0.3s, box-shadow 0.3s;
}

.card-premium:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 40px rgba(0,0,0,0.15);
}

.card-premium-header {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 20px;
}
```

Uso:

```html
<div class="hero-section">
    <h1>Bienvenido a Mi Sitio</h1>
    <p>Contenido increíble aquí</p>
</div>

<div class="card-premium">
    <div class="card-premium-header">
        <h3>Tarjeta Premium</h3>
    </div>
    <div class="uk-padding">
        <p>Contenido de la tarjeta</p>
    </div>
</div>
```

## 4. Temas Completos

### Tema Oscuro

```css
@media (prefers-color-scheme: dark) {
    :root {
        --uk-background-default: #1a1a1a;
        --uk-text-default: #ffffff;
        --uk-card-background: #2a2a2a;
        --uk-card-border: #444;
    }
    
    body {
        background-color: var(--uk-background-default);
        color: var(--uk-text-default);
    }
    
    .uk-card-default {
        background: var(--uk-card-background);
        border-color: var(--uk-card-border);
    }
}
```

### Tema de Corporativo

```css
:root {
    --uk-primary: #1a237e;
    --uk-secondary: #0097a7;
    --uk-text-default: #37474f;
    --uk-global-font-family: 'Georgia', serif;
    --uk-global-line-height: 1.8;
}

.uk-button-primary {
    border-radius: 2px;
    font-weight: 600;
    letter-spacing: 1px;
}

.uk-card-default {
    border: 1px solid #eceff1;
    box-shadow: 0 1px 3px rgba(0,0,0,0.08);
}
```

## 5. Utilidades Personalizadas

Crea nuevas utilidades para casos de uso específicos:

```css
/* Espaciado extra */
.uk-margin-xl {
    margin: 40px;
}

.uk-padding-xl {
    padding: 40px;
}

/* Colores adicionales */
.uk-background-gradient {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
}

/* Efectos */
.uk-shadow-hover {
    transition: box-shadow 0.3s;
}

.uk-shadow-hover:hover {
    box-shadow: 0 10px 30px rgba(0,0,0,0.2);
}

/* Tipografía */
.uk-text-subtitle {
    font-size: 1.1em;
    font-weight: 500;
    color: var(--uk-text-muted);
    text-transform: uppercase;
    letter-spacing: 1px;
}
```

## 6. Responsive Personalizado

```css
/* Mobile first */
.hero-title {
    font-size: 1.5em;
}

@media (min-width: 640px) {
    .hero-title {
        font-size: 2em;
    }
}

@media (min-width: 960px) {
    .hero-title {
        font-size: 3em;
    }
}
```

## 7. Configuración NPM

Si usas UIKit mediante NPM, puedes personalizar importando solo componentes necesarios:

```javascript
// main.js
import UIkit from 'uikit';
import Icons from 'uikit/dist/js/components/icons';
import Modal from 'uikit/dist/js/components/modal';
import Navbar from 'uikit/dist/js/components/navbar';

UIkit.use(Icons);
UIkit.use(Modal);
UIkit.use(Navbar);
```

Y en tu CSS:

```less
// Importar solo lo que necesitas
@import 'uikit/src/less/components/button';
@import 'uikit/src/less/components/card';
@import 'uikit/src/less/components/grid';

// Personalizar variables
@primary-color: #1e87f0;
@secondary-color: #222;
```

## Mejores Prácticas

1. **Mantén consistencia**: Usa un sistema de colores y espaciado consistente
2. **Usa variables**: Aprovecha las variables CSS para cambios globales fáciles
3. **Organiza tu CSS**: Estructura el CSS personalizado de manera lógica
4. **Documentación**: Documenta tus personalizaciones
5. **Testing**: Prueba en diferentes navegadores y dispositivos
6. **Performance**: No sobrecargues con demasiadas personalizaciones

## Ejemplo Completo: Tema Personalizado

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="uikit.min.css">
    <style>
        :root {
            --uk-primary: #ff6b6b;
            --uk-secondary: #4ecdc4;
            --uk-success: #51cf66;
            --uk-warning: #ffd43b;
            --uk-danger: #ff6b6b;
        }

        * {
            border-radius: 8px;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        .uk-button {
            border-radius: 20px;
            font-weight: 600;
            transition: all 0.3s;
        }

        .uk-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .uk-card {
            border-radius: 12px;
            overflow: hidden;
        }
    </style>
</head>
<body>
    <div class="uk-container uk-margin-large-top">
        <h1 class="uk-text-center">Mi Tema Personalizado</h1>
        <button class="uk-button uk-button-primary">Botón Bonito</button>
    </div>
</body>
</html>
```

---

Para más información sobre personalización, consulta la [documentación oficial](https://getuikit.com/docs/customizing).
