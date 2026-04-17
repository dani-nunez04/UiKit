# Guía de Instalación y Uso

Una guía completa para instalar y usar UIKit en tus proyectos.

## Tabla de Contenidos

1. [Instalación Rápida (CDN)](#instalación-rápida-cdn)
2. [Instalación con NPM](#instalación-con-npm)
3. [Primeros Pasos](#primeros-pasos)
4. [Estructura de Proyecto](#estructura-de-proyecto)
5. [Troubleshooting](#troubleshooting)

---

## Instalación Rápida (CDN)

La forma más fácil de comenzar. RECOMENDADO PARA EMPEZAR

### 1. Copia el Template Base

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Página con UIKit</title>
    
    <!-- UIKit CSS -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/uikit@3/dist/css/uikit.min.css">
</head>
<body>
    <!-- Tu contenido aquí -->
    <div class="uk-container uk-padding">
        <h1>Hola UIKit!</h1>
        <button class="uk-button uk-button-primary">Mi Primer Botón</button>
    </div>

    <!-- UIKit JavaScript -->
    <script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit.min.js"></script>
    
    <!-- UIKit Icons -->
    <script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit-icons.min.js"></script>
</body>
</html>
```

### 2. Guarda como `.html` y Abre en tu Navegador

Eso es todo! Ya tienes UIKit funcionando.

### 3. Comienza a Añadir Componentes

```html
<!-- Botón -->
<button class="uk-button uk-button-primary">Enviar</button>

<!-- Card -->
<div class="uk-card uk-card-default">
    <div class="uk-card-body">Mi Card</div>
</div>

<!-- Grid -->
<div class="uk-grid" uk-grid>
    <div class="uk-width-1-3">Columna 1</div>
    <div class="uk-width-1-3">Columna 2</div>
    <div class="uk-width-1-3">Columna 3</div>
</div>
```

---

## Instalación con NPM

Para proyectos más complejos o si usas bundlers como Webpack, Vite, etc.

### 1. Instala UIKit

```bash
npm install uikit
# o si usas yarn
yarn add uikit
# o si usas pnpm
pnpm add uikit
```

### 2. En tu Archivo JavaScript

```javascript
// main.js
import UIkit from 'uikit';
import Icons from 'uikit/dist/js/components/icons';

// Cargar componentes específicos
UIkit.use(Icons);

// Ahora UIkit está disponible globalmente
console.log(UIkit);
```

### 3. Importa CSS

```javascript
// main.js (continuación)
import 'uikit/dist/css/uikit.min.css';
```

O en tu CSS/LESS:

```css
/* main.css */
@import 'uikit/dist/css/uikit.min.css';
```

### 4. Usar en tu HTML

```html
<!-- Tus componentes funcionan igual -->
<button class="uk-button uk-button-primary">Enviar</button>
```

---

## Primeros Pasos

### Crear tu Primer Proyecto

```bash
# 1. Crea una carpeta
mkdir mi-sitio-uikit
cd mi-sitio-uikit

# 2. Crea un archivo index.html
# (Copia el template de CDN de arriba)

# 3. Abre en tu navegador
# Simplemente haz doble-click en index.html
```

### Estructura Recomendada

```
mi-proyecto/
├── index.html
├── css/
│   └── estilos.css       (tus estilos personalizados)
├── js/
│   └── main.js           (tu JavaScript)
├── imagenes/
│   └── ...
└── README.md
```

### Archivo HTML Completo

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Proyecto</title>
    
    <!-- UIKit CSS -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/uikit@3/dist/css/uikit.min.css">
    
    <!-- Tus estilos -->
    <link rel="stylesheet" href="css/estilos.css">
</head>
<body>
    <!-- Navbar -->
    <nav class="uk-navbar-container" uk-navbar>
        <div class="uk-navbar-left">
            <div class="uk-navbar-item">
                <h2>Mi Sitio</h2>
            </div>
        </div>
    </nav>

    <!-- Contenido Principal -->
    <main class="uk-container uk-padding">
        <h1>Bienvenido</h1>
        <p>Tu contenido aquí</p>
    </main>

    <!-- Footer -->
    <footer class="uk-padding uk-background-secondary uk-text-white">
        <div class="uk-container uk-text-center">
            <p>&copy; 2024 Mi Proyecto</p>
        </div>
    </footer>

    <!-- UIKit JS -->
    <script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit-icons.min.js"></script>
    
    <!-- Tu JavaScript -->
    <script src="js/main.js"></script>
</body>
</html>
```

### Archivo CSS Personalizado

```css
/* css/estilos.css */

/* Variables personalizadas */
:root {
    --mi-color-primario: #667eea;
    --mi-color-secundario: #764ba2;
}

/* Sobrescribir estilos de UIKit */
.uk-button-primary {
    background: var(--mi-color-primario);
}

/* Tus clases personalizadas */
.hero {
    background: linear-gradient(135deg, var(--mi-color-primario), var(--mi-color-secundario));
    color: white;
    padding: 100px 20px;
    text-align: center;
}

.feature-box {
    padding: 30px;
    border-radius: 10px;
    background: white;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}
```

### Archivo JavaScript

```javascript
// js/main.js

// Esperar a que DOM esté listo
document.addEventListener('DOMContentLoaded', function() {
    console.log('¡Página cargada!');
    
    // Tu código aquí
    const btn = document.querySelector('.uk-button');
    if (btn) {
        btn.addEventListener('click', function() {
            alert('¡Botón clickeado!');
        });
    }
});
```

---

## Estructura de Proyecto

### Proyecto Simple

```
mi-proyecto/
├── index.html         (página principal)
└── README.md
```

### Proyecto Mediano

```
mi-proyecto/
├── index.html
├── about.html
├── contacto.html
├── css/
│   └── estilos.css
├── js/
│   └── main.js
├── imagenes/
│   ├── logo.png
│   └── hero.jpg
└── README.md
```

### Proyecto Grande (NPM)

```
mi-proyecto/
├── src/
│   ├── index.html
│   ├── js/
│   │   └── main.js
│   └── css/
│       └── estilos.css
├── dist/              (compilado)
├── package.json
├── webpack.config.js
└── README.md
```

---

## Troubleshooting

PROBLEMA: Los estilos no aparecen

**Problema**: UIKit no se carga.

**Solución**:
```html
<!-- Verifica que tiene este orden -->
1. Meta charset
2. Meta viewport
3. UIKit CSS  ← Primero
4. Tus CSS
```

PROBLEMA: Los componentes no funcionan

**Problema**: Modales, dropdowns no abren.

**Solución**:
```html
<!-- Asegúrate de cargar el JavaScript de UIKit -->
<script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit-icons.min.js"></script>
```

PROBLEMA: Los iconos no aparecen

**Problema**: Ver cuadrados en lugar de iconos.

**Solución**:
```html
<!-- Cargar DESPUÉS de uikit.min.js -->
<script src="https://cdn.jsdelivr.net/npm/uikit@3/dist/js/uikit-icons.min.js"></script>
```

PROBLEMA: El grid no es responsivo

**Problema**: Las columnas no se adaptan.

**Solución**:
```html
<!-- Usa el atributo uk-grid -->
<div class="uk-grid" uk-grid>
    <div class="uk-width-1-2@m">Responsive</div>
</div>

<!-- Añade breakpoint -->
uk-width-1-2@m  ← Media query
```

PROBLEMA: Estilos personalizados no funcionan

**Problema**: CSS personalizado se sobrescribe.

**Solución**:
```css
/* Mayor especificidad */
.uk-button.mi-boton {
    background: #ff6b6b;
}

/* O usa !important (último recurso) */
.uk-button-custom {
    background: #ff6b6b !important;
}
```

---

## Checklist de Configuración

- [ ] CDN o NPM instalado
- [ ] Meta tags configurados
- [ ] UIKit CSS cargado
- [ ] UIKit JS cargado
- [ ] Iconos cargados (si los usas)
- [ ] Tu CSS personalizado agregado
- [ ] Tu JavaScript agregado
- [ ] Probado en navegador
- [ ] Probado en mobile
- [ ] Probado en diferentes navegadores

---

## Siguientes Pasos

1. Instalación completada
2. Lee la [Introducción](introduccion.md)
3. Aprende el [Grid](grid.md)
4. Explora [Componentes](componentes.md)
5. Mira los [Ejemplos](../ejemplos/)

---

## Tips Finales

- Siempre personaliza los colores
- Prueba en mobile desde el inicio
- Usa F12 para debuguear
- Lee la [documentación oficial](https://getuikit.com/docs)
- Mantente actualizado con UIKit

---

¡Ahora estás listo para comenzar! 🎉
