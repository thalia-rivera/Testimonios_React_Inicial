# Práctica inicial de React

## Integrantes 

- **Gutierrez Calero Sugey**
- **Rivera López Thalia Yazmin**

## Versiones 

- **Node.js:** v24.21.0
- **npm:** 11.19.0

## Instalación

## Ejecución

## Estructura


## Desiciones principales

### Pruebas 
### 10 Casos de prueba de la etapa básica

|Prueba | Acción y resultado esperado | Resultado Obtenido | Estado | Correcciones |
|P01 Inicio | Se muestra Ana y la posición 1 de 3. | Se muestra el primer testimonio registrado en el archivo data.js con el nombre de Ana Perez | Aprobado | No hicimos correcciones porque la prueba fue exitosa |
|P02 Siguiente |  Desde Ana, Siguiente muestra Luis y 2 de 3. | Se muestra el siguiente testimonio con el nombre de Luis García y Testimonio 2 de 3  de forma correcta | Aprobado | No hicimos correciones porque el resultado de la prueba fue aceptable |
|P03 Límite superior | Desde María, Siguiente muestra Ana. | Si es correcto, despues de Maria López el siguiente testimonio es de Ana Perez | Aprobado | No hicimos correciones |
|P04 Límite inferior | Desde Ana, Anterior muestra María. | El resultado es el mismo que el esperado, de Ana Perez, uno anterior es Maria López | Aprobada | No se hicieron correciones porque fue aceptada la prueba |
|P05 Aleatorio | Desde cualquier posición, cambia a otra válida. Repetir 10 veces inspeccionar también la lógica, porque el muestreo no demuestra por sí solo la propiedad. | Si, con el botón de aleatorio los testimonios cambian de forma correcta. | Aprobada | No hubo correciones |
|P06 Un registro | Dejar temporalmente un solo objeto: todos los controles mantienen el registro y no hay errores. |  Si, el codigo no se rompe y el unico registro que existia en ninguna accion de los botones desaparecio | Aprobada | No hubo correcciones |
|P07 Sin registros | Usar temporalmente []: aparece el mensaje y no se muestran controles. | Aparece un titulo "Experiencias de nuestros usuarios" y el mensaje no hay testimonios disponibles porque el arreglo esta vacio y los botones tampoco aparecen | Aprobada | No tuvimos que hacer correcciones |
|P08 Ampliación de datos | Restaurar y añadir cinco objetos: navegación completa y contador de ocho. | Cuando restaure el arreglo para anadir los otros 5 testimonios, ahora el contador era 8 y toods los botones funcionaban correctamente recorriendo los 8 restimonios | Aprobada | No hubo correcciones |
|P09 Presentación | Probar tres anchos, textos largos y navegación por teclado. | La pagina es completamente responsiva en los anchos probados, lo probamos desde las herramiengtas de desarrollador. Los elementos se adaptan a las dimensiones | Aprobada | No hubo correciones |
P10 Compilación | Ejecutar npm run build y revisar ausencia de errores de aplicación en consola. | npm run build ha compilado y optimizado exitosamente el proyecto de React y no hay errores en la consola | Aprobada | No hubo correciones | 















# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.
