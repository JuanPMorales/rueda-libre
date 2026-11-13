# Rueda Libre

Sitio web estático para **Rueda Libre**, un servicio de alquiler de bicicletas en Medellín. El proyecto presenta la flota disponible, las tarifas, los recorridos guiados, los productos para ciclismo y un formulario para solicitar reservas.

## Vista previa

El sitio publicado está disponible en:

<https://juanpmorales.github.io/rueda-libre/index.html>

## Funcionalidades

- Página de inicio con promociones, servicios y bicicletas disponibles.
- Catálogo de bicicletas urbanas, de montaña, eléctricas, infantiles y tándem.
- Página de tarifas por tipo de bicicleta y duración del alquiler.
- Información de recorridos guiados:
  - Río y Parques.
  - Sabores de Barrio.
  - Reto Las Palmas.
- Formulario de reserva con validaciones para datos personales, fecha, bicicleta, plan y cantidad.
- Políticas de alquiler y canales de contacto por correo y WhatsApp.
- Diseño responsive con Bootstrap y estilos personalizados.
- Prototipo independiente de la experiencia nocturna **Rueda Nocturna** con Tailwind CSS.

## Tecnologías

- HTML5.
- CSS3.
- JavaScript.
- Bootstrap 5.3 y Bootstrap Icons mediante CDN.
- Google Fonts: Montserrat y Open Sans.
- Tailwind CSS 4 para el prototipo `nocturna/`.

## Estructura del proyecto

```text
.
├── index.html                 # Página principal
├── css/
│   └── styles.css              # Estilos generales
├── img/                        # Logos, fotografías e ilustraciones
├── paginas/
│   ├── tarifas.html            # Tarifas y recorridos guiados
│   ├── reservas.html           # Formulario de reservas
│   └── reservas.js             # Validación del formulario
├── nocturna/
│   ├── index.html              # Prototipo Rueda Nocturna
│   ├── prototipo.html          # Prototipo con Tailwind vía CDN
│   ├── package.json            # Dependencias de Tailwind
│   └── src/
│       ├── input.css           # Entrada de Tailwind
│       └── output.css          # CSS generado
├── pruebas/
│   └── catalogo-bootstrap.html # Página de pruebas
└── bitacoras.txt               # Registro de avances y decisiones
```

## Ejecución local

El sitio principal no requiere instalación de dependencias. Puede abrirse directamente desde `index.html`, aunque se recomienda usar un servidor local para que todas las rutas funcionen correctamente.

Con Python:

```bash
python3 -m http.server 5500
```

Después, visita <http://localhost:5500>.

También puedes usar la extensión **Live Server** de Visual Studio Code.

## Desarrollo de `nocturna/`

El subproyecto utiliza Tailwind CSS para generar los estilos de `nocturna/src/output.css`.

```bash
cd nocturna
npm install
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```

Con el proceso activo, abre `nocturna/index.html` mediante el servidor local.

## Navegación principal

| Página | Archivo |
|---|---|
| Inicio | `index.html` |
| Tarifas y rutas | `paginas/tarifas.html` |
| Reservas | `paginas/reservas.html` |
| Rueda Nocturna | `nocturna/index.html` |

## Reserva

El formulario valida los campos en el navegador y muestra los mensajes de validación antes de permitir el envío. Actualmente funciona como una interfaz frontend: no incluye un backend para guardar reservas ni enviar los datos a un servicio externo.

## Licencia

Este proyecto es de carácter educativo y demostrativo.
