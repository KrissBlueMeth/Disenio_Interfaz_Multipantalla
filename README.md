# Diseño de Interfaz Multipantalla: Configurador de Entorno de Trabajo

Este repositorio contiene el código fuente de la actividad práctica realizada para la asignatura de **Desarrollo de Interfaces**. El proyecto consiste en una aplicación web que simula un configurador de preferencias de usuario, enfocándose en la usabilidad (UX), la accesibilidad y la persistencia de datos entre pantallas.

## 📋 Descripción de la Actividad

El objetivo principal es desarrollar una interfaz multipantalla que gestione el flujo de información y ofrezca retroalimentación (feedback) al usuario, aplicando estándares de diseño modernos.

La aplicación permite al usuario:
1.  Introducir sus datos personales y preferencias de visualización (Tema Claro/Oscuro y Tamaño de Fuente).
2.  Guardar dicha configuración simulando una carga de datos.
3.  Visualizar una pantalla de bienvenida personalizada que aplica los estilos seleccionados automáticamente.

## 🛠️ Tecnologías Utilizadas

* **HTML5:** Estructura semántica del contenido.
* **CSS3 & Bootstrap 5.3:** Diseño responsivo y estilizado de componentes.
* **JavaScript (ES6):** Lógica de negocio, manipulación del DOM y gestión de eventos.
* **Web Storage API:**
    * `localStorage`: Para la persistencia de preferencias (Tema y Nombre) a largo plazo.
    * `sessionStorage`: Para la gestión de estados temporales (Feedback de carga).

## 🚀 Funcionalidades Clave y Diseño UX/UI

Este proyecto ha sido desarrollado siguiendo principios estrictos de diseño de interfaces:

### 1. Principios de Usabilidad
* **Ley de Fitts:** Los botones de acción principal ("Guardar", "Ayuda") cuentan con un área de clic ampliada y ubicación estratégica para facilitar la interacción.
* **Visibilidad del Sistema:** Se implementa un *loader* (barra de progreso) durante la transición entre pantallas para informar al usuario de que su solicitud se está procesando.

### 2. Accesibilidad (WCAG)
* **Contraste:** El "Modo Oscuro" ha sido diseñado cumpliendo los ratios de contraste AA para evitar fatiga visual.
* **Navegación por Teclado:** Todo el formulario y los botones son accesibles mediante la tecla `Tab`, siguiendo un orden lógico.
* **Etiquetado:** Uso correcto de etiquetas `<label>` vinculadas a los inputs para soporte de lectores de pantalla.

### 3. Persistencia de Datos
La aplicación recuerda al usuario. Si cierras el navegador y vuelves a entrar, tu nombre y tu tema preferido (oscuro/claro) se mantienen activos gracias a la implementación de `localStorage`.

## 📂 Estructura del Proyecto

```text
├── index.html          # Pantalla de Inicio (Formulario de configuración)
├── bienvenida.html     # Pantalla de Destino (Resultado personalizado con Modal de Ayuda)
├── css/                # (Estilos integrados en HTML)
└── Manual_Usuario.pdf  # Documentación funcional para el usuario final
