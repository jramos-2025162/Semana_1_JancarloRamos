# Documentación del Proyecto - Actividad 1 Angular


El proyecto fue creado utilizando la CLI de Angular mediante el comando:
`ng new mi_primer_proyecto_angular`

El proyecto está organizado bajo una estructura modular y escalable dentro de la carpeta `src/app/`:

* `src/app/components/`: Almacena los componentes visuales de la aplicación.
  * **Existentes:** `header`, `body`, `footer`.
  * **Nuevos componentes:** `inicio`, `productos`, `contacto`, `acerca-de`.
* `src/app/core/`: Destinado a elementos globales como servicios, modelos e interceptores para la lógica de negocio.
  * `core/services/api.service.ts`: Servicio base configurado para realizar peticiones HTTP al servidor.
* `src/environments/`: Contiene la configuración de variables de entorno (URL base de la API).
* `AppModule` (`app.module.ts`): Módulo principal donde se declaran e integran todos los componentes y servicios necesarios.
* `AppComponent` (`app.component.ts`): Componente raíz que orquesta la visualización general.

## 3. Planificación de Conexión con Backend (Node.js / TypeScript)
La comunicación con el backend se realizará mediante el protocolo HTTP consumiendo una API RESTful desarrollada en Node.js/Express:

1. **Configuración:** La URL base (`http://localhost:3000/api`) se define en `environment.ts`.
2. **Consumo:** Los componentes inyectarán el servicio de API para recibir y mostrar la información procesada por el servidor.