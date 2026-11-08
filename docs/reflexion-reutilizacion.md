# Reflexión individual: experimento de reutilización (Tarea 12)

**Nombre:** Sugey
**Equipo:** Sugey y Thalia Rivera

## 1. ¿Qué reutilicé y qué duplicación evité?
Reutilicé el componente `Testimonial` en tres lugares: dos tarjetas de ejemplo
(Ana Pérez y Luis García) y la tarjeta de navegación. Cada una recibe un objeto
distinto por la prop `item`, pero todas usan el mismo código. Sin el componente
habría tenido que copiar tres veces el bloque de `article`, `img`, `h2`, `p` y
`blockquote`. Para comprobarlo agregué una sola línea de borde en
`.testimonial-card` y las tres tarjetas cambiaron al mismo tiempo.

## 2. Comparación con actualizar el DOM manualmente
Sin React tendría que buscar cada elemento del DOM (por ejemplo con
`document.querySelector`) y cambiar su texto, su imagen y sus atributos cada vez
que se presione un botón, además de cuidar que todo quede sincronizado. Con
React solo cambio el estado `index` con `setIndex`; React vuelve a ejecutar
`App`, calcula qué objeto se pasa a `Testimonial` y actualiza en el DOM solo lo
necesario.

## 3. ¿Qué organización depende de mi diseño y qué mecanismo aporta React?
Depende de nuestro diseño separar los datos en `data.js`, la presentación en
`Testimonial.jsx`, las acciones en `Controls.jsx` y el estado en `App.jsx`;
también decidimos qué archivo cambiar para cada tipo de modificación. React
aporta los mecanismos: componentes, JSX, props, el estado con `useState` y el
renderizado que actualiza la pantalla cuando el estado cambia.

## 4. Dificultad o costo de usar React en una aplicación pequeña
Para una aplicación tan pequeña hay que aprender JSX, props y Hooks, y además
instalar y configurar Node.js, npm y Vite. También hay más archivos y pasos
(compilación, dependencias). Una página con una sola tarjeta podría hacerse con
HTML, CSS y JavaScript sin necesitar nada de eso.

## 5. Parte que todavía no comprendo y pregunta concreta
Todavía no me queda claro cuándo conviene usar `useRef` en lugar de guardar el
identificador del intervalo dentro del `useEffect`. Mi pregunta es: ¿en qué
casos reales una variable local del efecto ya no basta y se necesita `useRef`?