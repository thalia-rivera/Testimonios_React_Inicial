# Práctica inicial de React

## Integrantes 

- **Gutierrez Calero Sugey**
- **Rivera López Thalia Yazmin**

## Versiones 

- **Node.js:** v24.21.0
- **npm:** 11.19.0

## Instalación

### Requisitos

- Node.js (versión LTS compatible con Vite): `<resultado de node -v>`
- npm: `<resultado de npm -v>`
- Git y un editor como VS Code

### Pasos

1. Clonar el repositorio:

```bash
git clone https://github.com/thalia-rivera/Testimonios_React_Inicial.git
cd Testimonios_React_Inicial
```

2. Cambiar a la rama de desarrollo:

```bash
git checkout develop
git pull
```

3. Instalar las dependencias:

```bash
npm install
```

`node_modules` no se incluye en el repositorio, por eso este paso se repite en cada clon.

## Ejecución

| Comando | Resultado |
|---|---|
| `npm run dev` | Inicia el servidor de desarrollo. Abrir la dirección **Local** que muestre la terminal (normalmente `http://localhost:5173/`). |
| `npm run build` | Genera la versión de producción en `dist`. |
| `npm run preview` | Permite revisar localmente la compilación. No publica el sitio. |


## Estructura

```
Testimonios_React_Inicial/
├── docs/
│   └── reflexion-reutilizacion.md   Reflexión individual de la práctica
├── public/
│   ├── favicon.svg                  Icono de la pestaña
│   └── icons.svg                    Iconos de la plantilla de Vite
├── src/
│   ├── assets/                      Recursos de la plantilla (hero.png, react.svg, vite.svg)
│   ├── components/
│   │   ├── Testimonial.jsx          Tarjeta que presenta un testimonio
│   │   └── Controls.jsx             Botones Anterior, Siguiente y Aleatorio
│   ├── App.jsx                      Estado, navegación y reproducción automática
│   ├── main.jsx                     Monta React en #root e importa styles.css
│   ├── data.js                      Arreglo con los testimonios
│   └── styles.css                   Estilos de la aplicación
├── .gitignore                       Archivos que Git ignora (node_modules, dist)
├── eslint.config.js                 Configuración del análisis de código
├── index.html                       Contiene el elemento con id "root"
├── package.json                     Dependencias y comandos
├── package-lock.json                Versiones exactas de las dependencias
├── vite.config.js                   Configuración de Vite
└── README.md                        Documentación del proyecto
```


## Desiciones principales
Usamos fotos locales en public/fotos porque las URLs aleatorias mostraban fotos que no coincidían con el género del nombre mas a parte que dependían de internet. Solo que este cambio lo decidimos al final. 

Elegimos usar main, develop y ramas feature/... con Pull Requests hacia develop, y que main solo reciba la versión final como una buena practica de trabajo con Git.

Alternamos conductor y observador por punto de la actividad o por etapas, ambas estuvimos al pendiente siempre del trabajo de la otra. 

Los cinco testimonios adicionales. La guía pedía añadirlos, pero los nombres, cargos y comentarios los inventaron y desidimos nosotros.

Organizamos en un tablero las tareas pendientes y nos asignamos ambas a cada tarjeta por que si una llevaba a cabo la tarea, la otra la revisaba.

Para las pruebas, al llegar a la etapa 10 ya teniamos agregados los 8 registros. Pa identificar bien el orden de las pruebas mejor lo probamos en las que correspondia con 3 y en las que ya debian hacerse coon los 8, solo estuvimos comentando los registros en data.js y nos funciono bien.

## Pruebas 
### 10 Casos de prueba de la etapa básica

| Prueba | Acción y resultado esperado | Resultado Obtenido | Estado | Correcciones |
|---|---|---|---|---|
| P01 Inicio | Se muestra Ana y la posición 1 de 3. | Se muestra el primer testimonio registrado en el archivo data.js con el nombre de Ana Perez | Aprobado | No hicimos correcciones porque la prueba fue exitosa |
| P02 Siguiente | Desde Ana, Siguiente muestra Luis y 2 de 3. | Se muestra el siguiente testimonio con el nombre de Luis García y Testimonio 2 de 3  de forma correcta | Aprobado | No hicimos correciones porque el resultado de la prueba fue aceptable |
| P03 Límite superior | Desde María, Siguiente muestra Ana. | Si es correcto, despues de Maria López el siguiente testimonio es de Ana Perez | Aprobado | No hicimos correciones |
| P04 Límite inferior | Desde Ana, Anterior muestra María. | El resultado es el mismo que el esperado, de Ana Perez, uno anterior es Maria López | Aprobada | No se hicieron correciones porque fue aceptada la prueba |
| P05 Aleatorio | Desde cualquier posición, cambia a otra válida. Repetir 10 veces inspeccionar también la lógica, porque el muestreo no demuestra por sí solo la propiedad. | Si, con el botón de aleatorio los testimonios cambian de forma correcta. | Aprobada | No hubo correciones |
| P06 Un registro | Dejar temporalmente un solo objeto: todos los controles mantienen el registro y no hay errores. | Si, el codigo no se rompe y el unico registro que existia en ninguna accion de los botones desaparecio | Aprobada | No hubo correcciones |
| P07 Sin registros | Usar temporalmente []: aparece el mensaje y no se muestran controles. | Aparece un titulo "Experiencias de nuestros usuarios" y el mensaje no hay testimonios disponibles porque el arreglo esta vacio y los botones tampoco aparecen | Aprobada | No tuvimos que hacer correcciones |
| P08 Ampliación de datos | Restaurar y añadir cinco objetos: navegación completa y contador de ocho. | Cuando restaure el arreglo para anadir los otros 5 testimonios, ahora el contador era 8 y toods los botones funcionaban correctamente recorriendo los 8 restimonios | Aprobada | No hubo correcciones |
| P09 Presentación | Probar tres anchos, textos largos y navegación por teclado. | La pagina es completamente responsiva en los anchos probados, lo probamos desde las herramiengtas de desarrollador. Los elementos se adaptan a las dimensiones | Aprobada | No hubo correciones |
| P10 Compilación | Ejecutar npm run build y revisar ausencia de errores de aplicación en consola. | npm run build ha compilado y optimizado exitosamente el proyecto de React y no hay errores en la consola | Aprobada | No hubo correciones |


### 7 Casos de prueba de la etapa avanzada 

| Prueba | Acción y resultado esperado | Resultado Obtenido | Estado | Correcciones |
|---|---|---|---|---|
| A01 Activación | Reanudar inicia avances separados aproximadamente cinco segundos. | Si, aproximadamente cada 5 segundos hace el cambio entre testimonios | Aprobado | No se realizo correciones |
| A02 Pausa | Pausar mantiene el testimonio al esperar más de cinco segundos. | Si se queda pausado el testimonio, no cambia | Aprobada | No se realizacon correciiones | 
| A03 Acción manual | Anterior, Siguiente o Aleatorio cambian la tarjeta y dejan pausada la reproducción. | Si, con estos 3 botones la tarjeta se queda pausada y cumplen correctamente con su función | Aprobado | No se realizaron correciones | 
| A04 Reanudación | Reanudar permite nuevos avances; repetir varias veces sin aceleración. | Si ejecuto la accion de reanudar y pausar varias veces sigue funcionando igual, el tiempo sigue estando en aprox 5 segundos en el intervalo | Aprobada | Sin coorreciones |
| A05 Límites | Durante autoplay, el último vuelve al primero. | Despues del testimonio 8 de 8, regresa al 1 de 8 correctamente | Aprobada | Sin correciones |
| A06 Pocos datos | Con cero o un registro no se crea un intervalo. |
| A07 Limpieza | Revisar el return del efecto y comprobar que no aparecen intervalos acumulados al alternar pausa y reproducción. | Ejecutamos las acciones d elos botones repetidamente y confirmamos que el intervalo de tiempo seguia siendo 5 segundos entre cada testimonio | Aprobado | Sin correcciones |


###  useEffect y su limpieza

useEffect sirve para realizar acciones que no forman parte directamente de lo que se muestra en pantalla. En nuestra aplicación lo utilizamos para controlar un temporizador que, cuando se presiona Reanudar y hay al menos dos testimonios, cambia automáticamente al siguiente cada cinco segundos.

La limpieza es una función que se encarga de detener ese temporizador mediante clearInterval. React la ejecuta antes de volver a iniciar el efecto o cuando el componente deja de mostrarse. Esto es importante porque, si no se hiciera, se podrían quedar varios temporizadores funcionando al mismo tiempo y provocar que los testimonios cambiaran más rápido de lo normal, pero con las pruebas comprobamos que si se limpiaban correctamente.


## Reflexiones finales de la practica 

### Guitierrez Calero Sugey

Con esta práctica entendí cómo funciona React en la práctica. Antes pensaba en una página como HTML que se cambia a mano, pero aquí los datos viven en `data.js`, `Testimonial` los muestra y `App` decide cuál se ve. Si cambia el índice, la pantalla se actualiza sola.

Lo que más me costó fue entender las props y el estado. Ya con el código propio vi que `Controls` solo avisa con un callback y que `App` es quien cambia el estado con `setIndex`. También entendí por qué hay que cuidar los límites: con el `%` la navegación da la vuelta, y con cero o un registro hay que evitar leer `testimonios[index]`.

En la parte del autoplay aprendí para qué sirve `useEffect`. El temporizador es algo externo al JSX, y por eso hay que limpiarlo con `clearInterval`. Si no, los intervalos se acumulan y el avance se acelera.

Trabajar en pareja con Git también me enseñó mucho: commits pequeños, coautoría, ramas, pull requests a `develop` y revisar `git status` antes de subir algo. Tuve errores, como un import de `index.css` que ya no existía, el servidor detenido y las fotos que no coincidían con los nombres, y los resolvimos leyendo la consola y usando fotos locales.

Reconozco que para una página tan pequeña React puede ser demasiado, pero separar datos, tarjeta y lógica hace más fácil encontrar dónde cambiar cada cosa.

### Rivera López Thalia Yazmin

Esta práctica me pareció muy enriquecedora, ya que anteriormente había escuchado hablar de React, pero realmente no sabía para qué servía ni qué lo hacía una herramienta tan útil.

Me pareció interesante trabajar con esta herramienta porque pude entender cómo una página se puede dividir en componentes más pequeños, donde cada uno cumple una función. Por ejemplo, la tarjeta de los testimonios se crea una sola vez y se puede reutilizar para mostrar los demás. Si se necesita cambiar algo de su diseño, basta con modificar ese componente y el cambio se refleja en todos. También aprendí que no es necesario estar modificando el HTML manualmente cada vez que cambia algo en pantalla, ya que React se encarga de actualizar la interfaz cuando cambia el estado.

Una de las partes que más me costó entender fue cómo funciona el estado y cómo los botones indican a App que debe cambiar el índice para mostrar otro testimonio. Sin embargo, al hacer las pruebas y seguir paso a paso lo que sucede cuando se presiona un botón, pude comprenderlo mejor.

También fue de ayuda trabajar en pareja, porque mientras uno escribía el código, el otro podía revisar y detectar errores. Esto nos permitió corregir algunos problemas antes de continuar, como cuando la carpeta components se había creado incorrectamente. 

En general, esta práctica me ayudó a tener una mejor idea de qué es React, cómo funciona y por qué es una herramienta tan utilizada actualmente.




