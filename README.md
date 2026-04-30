```markdown
# Infografía Interactiva — Cultivo de Trucha Arco Iris

Infografía web interactiva de tipo estadístico/datos basada en el manual de cultivo de trucha arco iris en jaulas flotantes. Presenta 10 indicadores clave del proceso productivo mediante tarjetas que revelan sus cifras técnicas únicamente cuando el usuario interactúa con ellas (hover o clic), manteniendo un diseño inicial limpio y de lectura inmediata.

---

## Vista previa

El diseño consta de una cuadrícula de 10 tarjetas sobre un fondo oscuro atmosférico con elementos flotantes sutiles. En su estado reposo cada tarjeta muestra únicamente un emoji temático y su título; al interactuar se desvela el valor numérico exacto y su descripción acompañados de una animación de revelado progresivo.

---

## Tecnologías utilizadas

| Tecnología | Uso en el proyecto |
|---|---|
| **HTML5** | Estructura semántica (`<header>`, `<main>`, `<section>`, `<article>`, `<footer>`) con atributos de accesibilidad (`aria-label`, `role`, `tabindex`). |
| **CSS3 (Vanilla)** | Diseño completo sin frameworks: Custom Properties para tokens de color, CSS Grid responsivo, animaciones `@keyframes`, transiciones con `ease-in-out`, `box-shadow` inset para el efecto de revelado, y media queries para el enfoque Mobile First. |
| **JavaScript (Vanilla)** | Lógica de interacción por clic/toque como complemento del hover, soporte de teclado (Enter, Espacio, Escape) y cierre de tarjetas al hacer clic fuera. |
| **Google Fonts** | Tipografía [Poppins](https://fonts.google.com/specimen/Poppins) en pesos 300, 400, 600, 700 y 900. |

> No se utilizaron frameworks CSS (Bootstrap, Tailwind) ni librerías JavaScript externas.

---

## Estructura del proyecto

```
trucha-infografia/
│
├── index.html        ← Archivo único con HTML, CSS y JS integrados
└── README.md         ← Este documento
```

El proyecto se entrega en un solo archivo `index.html` que contiene las tres capas de desarrollo embebidas:

- `<style>` — Toda la hoja de estilos (variables, reset, grid, tarjetas, animaciones, responsive).
- Markup HTML — Estructura semántica con las 10 tarjetas de datos.
- `<script>` — Lógica de interacción (toggle por clic, teclado y cierre global).

---

## Paleta de colores

| Token | Valor | Aplicación |
|---|---|---|
| Principal | `#c8e3ea` | Títulos de tarjetas y encabezado |
| Secundario | `#306182` | Fondo de las tarjetas |
| Acento | `#5e7750` | Valores revelados, línea decorativa, créditos |
| Fondo | `#0b1a27` | Fondo general del documento |

---

## Los 10 datos de la infografía

| # | Indicador | Dato |
|---|---|---|
| 01 | Alimentación | 8% – 9% de la biomasa para alevines |
| 02 | Temperatura | 11°C – 15°C rango óptimo |
| 03 | Densidad | 13 kg/m³ carga final máxima |
| 04 | Conversión | 1:1 – 1:1.2 factor de conversión |
| 05 | Vida | 99% supervivencia inicial |
| 06 | Oxígeno | 7 – 9 ppm disueltos |
| 07 | Inversión | 50% – 60% del costo es alimento |
| 08 | Acidez | pH 7 – 9 ideal |
| 09 | Respiración | 0 – 2 ppm de CO₂ |
| 10 | Ubicación | 10 – 20 m de profundidad |

---

## Cómo visualizar localmente

### Opción 1 — Doble clic (la más sencilla)

1. Descarga o copia el archivo `index.html` en cualquier carpeta de tu equipo.
2. Haz doble clic sobre el archivo.
3. Se abrirá en tu navegador predeterminado.

### Opción 2 — Arrastrar al navegador

1. Abre Chrome, Firefox, Edge o Safari.
2. Arrastra el archivo `index.html` desde tu explorador de archivos hacia la ventana del navegador.

### Opción 3 — Servidor local (recomendado para desarrollo)

Si deseas editar el proyecto y necesitar recarga en caliente o evitar restricciones de CORS:

```bash
# Con Python 3
python -m http.server 8000

# Con Node.js (npx, sin instalación)
npx serve .

# Con PHP
php -S localhost:8000
```

Luego abre `http://localhost:8000` en el navegador.

---

## Comportamiento interactivo

- **Escritorio:** Pasa el cursor sobre cualquier tarjeta para revelar el dato. Retira el cursor para ocultarlo.
- **Móvil / táctil:** Toca una tarjeta para fijar el dato visible. Toca otra tarjeta o cualquier zona vacía para cerrarla.
- **Teclado:** Usa `Tab` para navegar entre tarjetas, `Enter` o `Espacio` para revelar, y `Escape` para cerrar.
- **Reducir movimiento:** Si el sistema operativo tiene activada la opción de reducir movimiento, todas las animaciones se desactivan automáticamente.

---

## Compatibilidad

El proyecto es compatible con versiones recientes de:

- Google Chrome
- Mozilla Firefox
- Microsoft Edge
- Safari

No requiere conexión a internet una vez cargada la fuente Google Fonts (el navegador la almacena en caché). Si no hay conexión en la primera carga, se aplicará la fuente serif del sistema como respaldo.

---

## Fuentes bibliográficas

- Cornejo Dávila, Dariana. 2006. *Trucha Arco Iris en Jaulas Flotantes*. Revista.
- Mendoza, R. & Palomino, A. (2004). *Manual de cultivo de trucha arco iris en jaulas flotantes*. FONDEPES.

---

## Autora

**Dariana Cornejo Dávila**

---

## Licencia

Este proyecto es de uso educativo y académico. Se permite su reproducción con fines no comerciales citando a la autora.
```