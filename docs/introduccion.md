# Introducción a UIKit

## ¿Qué es UIKit?

UIKit es un framework CSS y JavaScript moderno desarrollado por YooTheme que proporciona componentes, patrones y utilidades para construir interfaces web rápidamente. Es ligero, flexible y fácil de integrar en cualquier proyecto.

## Características Principales

UIKit ofrece múltiples ventajas para desarrollo web:

- Ligero: Solo ~60KB comprimido
- Modular: Importa solo lo que necesitas
- Responsivo: Funciona perfectamente en móviles, tablets y escritorio
- Componentes Listos: Grid, botones, formularios, modales, navegación, etc
- Customizable: Fácil de personalizar con variables LESS/CSS
- JavaScript Interactivo: Componentes interactivos sin dependencias externas
- Soporte Navegadores: IE 11+ y navegadores modernos

## Comparación con Otros Frameworks

### UIKit vs Bootstrap
| Aspecto | UIKit | Bootstrap |
|--------|-------|-----------|
| Tamaño | ~60KB | ~200KB |
| Curva Aprendizaje | Media | Media |
| Comunidad | Pequeña | Grande |
| Customización | Excelente | Buena |
| Componentes | Suficientes | Muchos |

### UIKit vs Tailwind CSS
| Aspecto | UIKit | Tailwind |
|--------|-------|----------|
| Enfoque | Componentes | Utility-first |
| Aprendizaje | Clases semanticas | Muchas clases |
| Tamaño Final | Pequeño | Variable |
| Customización | LESS/CSS | Config file |

## Instalación Rápida

### Opción 1: CDN (Recomendado para empezar)

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/uikit@3/dist/css/uikit.min.css">
<script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit-icons.min.js"></script>
```

### Opción 2: NPM (Para proyectos profesionales)

```bash
npm install uikit
```

Luego en tu archivo JavaScript:

```javascript
import UIkit from 'uikit';
import Icons from 'uikit/dist/js/components/icons';

UIkit.use(Icons);
```

## Estructura Básica

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="uikit.min.css">
    <script src="uikit.min.js"></script>
    <script src="uikit-icons.min.js"></script>
</head>
<body>
    <!-- Tu contenido aquí -->
    <div class="uk-container">
        <h1>Hola UIKit!</h1>
    </div>
</body>
</html>
```

## Conceptos Clave

### 1. Container
El contenedor principal que centra el contenido y lo limita a un ancho máximo:

```html
<div class="uk-container">
    <!-- Contenido centrado -->
</div>
```

### 2. Grid
Sistema flexible para distribuir contenido en columnas:

```html
<div class="uk-grid">
    <div class="uk-width-1-3">Columna 1</div>
    <div class="uk-width-1-3">Columna 2</div>
    <div class="uk-width-1-3">Columna 3</div>
</div>
```

### 3. Componentes
Elementos predefinidos como botones, tarjetas, formularios, etc.:

```html
<button class="uk-button uk-button-primary">Enviar</button>
<div class="uk-card uk-card-default">Contenido</div>
```

### 4. Utilidades
Clases de ayuda para espaciado, alineación, texto, etc.:

```html
<div class="uk-margin uk-padding uk-text-center">
    Contenido con espaciado y centrado
</div>
```

## Ventajas de Usar UIKit

- Rápido de aprender e implementar
- Código HTML semántico y legible
- Componentes pulidos y profesionales
- Excelente para prototipado rápido
- Perfectamente responsive desde el inicio
- Sin dependencias externas
- Fácil de personalizar
- Comunidad activa

## Próximos Pasos

1. Lee la documentación de [Grid](grid.md)
2. Explora los [Componentes](componentes.md)
3. Aprende sobre [Utilidades](utilidades.md)
4. Revisa [Personalización](personalizacion.md)
5. Mira los [Ejemplos Prácticos](../ejemplos/)

---

**Nota**: Aunque UIKit es potente y fácil de usar, siempre es importante entender HTML y CSS base para aprovecharlo al máximo.
