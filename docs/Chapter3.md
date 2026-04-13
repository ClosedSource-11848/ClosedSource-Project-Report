# Capítulo III: Requirements Specification

## 3.1. User Stories

<p>Para la especificación de requisitos de los usuarios, se desarrollaron las historias de usuario que describen cada requisito y funcionalidad que debe estar implementado en el desarrollo del producto final para satisfacer las necesidades del público objetivo. A continuación se presentan las historias de usuario relacionadas con la plataforma QualiTrack. Esta sección reúne historias de usuario centradas en la experiencia de los distintos roles: el visitante de la landing page, el operario de planta y el supervisor o jefe de Aseguramiento de la Calidad. Aquí se definen las necesidades clave para cada uno, desde la navegación inicial, hasta la gestión de lotes, monitoreo IoT y generación de reportes de auditoría.</p>

<table>
  <thead>
    <tr>
      <th>Story ID</th>
      <th>Título</th>
      <th>Descripción</th>
      <th>Criterios de Aceptación (Gherkin)</th>
    </tr>
  </thead>
  <tbody>
    <!-- EP01 -->
    <tr>
      <td>EP01</td>
      <td>Navegación en la Landing Page</td>
      <td>Como visitante quiero tener una experiencia fluida en el sitio web para conocer los servicios de QualiTrack y tomar decisiones informadas.</td>
      <td></td>
    </tr>
    <tr>
      <td>US01</td>
      <td>Menú de navegación</td>
      <td>Como visitante de la Landing Page, quiero poder acceder a un menú de navegación en la parte superior de la página, para explorar fácilmente las secciones como "Inicio", "Características", "Planes" y "Contacto".</td>
      <td>
        <strong>Escenario 1: Navegación exitosa a través del menú</strong><br>
        <strong>Dado que</strong> el visitante está en la landing page<br>
        <strong>Cuando</strong> el menú de navegación está disponible<br>
        <strong>Entonces</strong> el usuario puede ver los enlaces principales y navegar a las secciones correspondientes.<br><br>
        <strong>Escenario 2: Menú no disponible</strong><br>
        <strong>Dado que</strong> el visitante está en la landing page<br>
        <strong>Cuando</strong> el menú no se carga correctamente<br>
        <strong>Entonces</strong> el usuario recibe un mensaje de error y tiene opciones alternativas de navegación.
      </td>
    </tr>
    <tr>
      <td>US02</td>
      <td>Visualización de planes de suscripción</td>
      <td>Como visitante de la Landing Page, quiero ver los planes de suscripción disponibles junto a su precio y características, para poder elegir el que mejor se adapte a las necesidades de mi laboratorio.</td>
      <td>
        <strong>Escenario 1: Visualización de planes disponibles</strong><br>
        <strong>Dado que</strong> el visitante navega a la sección de planes<br>
        <strong>Cuando</strong> los planes están disponibles en el sistema<br>
        <strong>Entonces</strong> el usuario puede ver la lista de planes con sus precios y características para compararlos.<br><br>
        <strong>Escenario 2: Planes no disponibles</strong><br>
        <strong>Dado que</strong> el visitante navega a la sección de planes<br>
        <strong>Cuando</strong> ocurre un error de carga<br>
        <strong>Entonces</strong> el usuario recibe un mensaje informativo sobre la indisponibilidad temporal.
      </td>
    </tr>
    <tr>
      <td>US03</td>
      <td>Visualización del equipo creador</td>
      <td>Como visitante de la Landing Page, quiero ver información sobre el equipo detrás de QualiTrack para generar confianza en el servicio antes de contratar.</td>
      <td>
        <strong>Escenario 1: Acceso a información del equipo</strong><br>
        <strong>Dado que</strong> el visitante navega a la sección "Equipo"<br>
        <strong>Cuando</strong> la información del equipo está disponible<br>
        <strong>Entonces</strong> el usuario puede ver los detalles de los creadores incluyendo nombres, roles y especialidades.<br><br>
        <strong>Escenario 2: Información del equipo no disponible</strong><br>
        <strong>Dado que</strong> el visitante navega a la sección "Equipo"<br>
        <strong>Cuando</strong> la información no está disponible<br>
        <strong>Entonces</strong> el usuario recibe un mensaje informativo sobre la indisponibilidad temporal.
      </td>
    </tr>
    <tr>
      <td>US04</td>
      <td>Formulario de contacto</td>
      <td>Como visitante de la landing page quiero completar un formulario de contacto para enviar consultas específicas y recibir una respuesta personalizada del equipo de QualiTrack.</td>
      <td>
        <strong>Escenario 1: Envío exitoso de consulta</strong><br>
        <strong>Dado que</strong> el visitante completa el formulario de contacto<br>
        <strong>Cuando</strong> todos los campos requeridos están completos y válidos<br>
        <strong>Entonces</strong> la consulta se envía exitosamente y el usuario recibe confirmación por correo.<br><br>
        <strong>Escenario 2: Datos de contacto inválidos</strong><br>
        <strong>Dado que</strong> el visitante completa el formulario de contacto<br>
        <strong>Cuando</strong> existen campos inválidos o incompletos<br>
        <strong>Entonces</strong> el sistema muestra mensajes de validación específicos para los campos problemáticos.
      </td>
    </tr>
    <tr>
      <td>US05</td>
      <td>Cambio de idioma</td>
      <td>Como visitante de la Landing Page quiero un botón para cambiar de idioma entre español e inglés para comprender mejor la propuesta de valor de QualiTrack.</td>
      <td>
        <strong>Escenario 1: Cambio exitoso de idioma</strong><br>
        <strong>Dado que</strong> el visitante selecciona un idioma disponible<br>
        <strong>Cuando</strong> confirma el cambio de idioma<br>
        <strong>Entonces</strong> la interfaz se actualiza al idioma seleccionado y mantiene la preferencia.<br><br>
        <strong>Escenario 2: Idioma no disponible</strong><br>
        <strong>Dado que</strong> el visitante intenta cambiar a un idioma<br>
        <strong>Cuando</strong> el idioma seleccionado no está soportado<br>
        <strong>Entonces</strong> el sistema mantiene el idioma actual y muestra un mensaje informativo.
      </td>
    </tr>
    <!-- EP02 -->
    <tr>
      <td>EP02</td>
      <td>Autenticación y gestión de acceso</td>
      <td>Como usuario de QualiTrack quiero poder registrarme, iniciar sesión y gestionar mi cuenta de forma segura para acceder a las funcionalidades según mi rol.</td>
      <td></td>
    </tr>
    <tr>
      <td>US06</td>
      <td>Registro de laboratorio en la plataforma</td>
      <td>Como jefe de Aseguramiento de Calidad quiero registrar mi laboratorio en QualiTrack para comenzar a gestionar los procesos de control de calidad de forma digital.</td>
      <td>
        <strong>Escenario 1: Registro exitoso</strong><br>
        <strong>Dado que</strong> el jefe de QA completa el formulario de registro con datos válidos del laboratorio<br>
        <strong>Cuando</strong> envía el formulario<br>
        <strong>Entonces</strong> el sistema crea la cuenta institucional, asigna un ID único al laboratorio y envía un correo de confirmación.<br><br>
        <strong>Escenario 2: Datos incompletos o inválidos</strong><br>
        <strong>Dado que</strong> el usuario intenta registrarse con datos faltantes<br>
        <strong>Cuando</strong> envía el formulario<br>
        <strong>Entonces</strong> el sistema muestra mensajes de validación en los campos correspondientes y no crea la cuenta.
      </td>
    </tr>
    <tr>
      <td>US07</td>
      <td>Inicio de sesión seguro</td>
      <td>Como usuario registrado (jefe de QA u operario) quiero iniciar sesión en la plataforma con mis credenciales para acceder a las funcionalidades habilitadas según mi rol.</td>
      <td>
        <strong>Escenario 1: Inicio de sesión exitoso</strong><br>
        <strong>Dado que</strong> el usuario tiene credenciales válidas<br>
        <strong>Cuando</strong> ingresa su usuario y contraseña correctamente<br>
        <strong>Entonces</strong> el sistema autentica al usuario y lo redirige a su dashboard según el rol asignado.<br><br>
        <strong>Escenario 2: Credenciales incorrectas</strong><br>
        <strong>Dado que</strong> el usuario ingresa credenciales inválidas<br>
        <strong>Cuando</strong> intenta iniciar sesión<br>
        <strong>Entonces</strong> el sistema muestra un mensaje de error y no permite el acceso.
      </td>
    </tr>
    <tr>
      <td>US08</td>
      <td>Gestión de roles y permisos de usuarios</td>
      <td>Como jefe de Aseguramiento de Calidad quiero gestionar los roles de mi equipo (supervisor, operario, auditor) para garantizar que cada usuario acceda únicamente a la información y funciones que le corresponden.</td>
      <td>
        <strong>Escenario 1: Asignación de rol exitosa</strong><br>
        <strong>Dado que</strong> el jefe de QA accede a la sección de gestión de usuarios<br>
        <strong>Cuando</strong> asigna un rol específico a un usuario<br>
        <strong>Entonces</strong> el sistema actualiza los permisos del usuario y este solo puede acceder a las funciones habilitadas para su rol.<br><br>
        <strong>Escenario 2: Intento de acceso no autorizado</strong><br>
        <strong>Dado que</strong> un operario intenta acceder a una funcionalidad restringida<br>
        <strong>Cuando</strong> navega a una sección fuera de sus permisos<br>
        <strong>Entonces</strong> el sistema bloquea el acceso y muestra un mensaje de restricción.
      </td>
    </tr>
    <!-- EP03 -->
    <tr>
      <td>EP03</td>
      <td>Dashboard de Telemetría en Tiempo Real</td>
      <td>Como supervisor de calidad quiero visualizar en tiempo real las variables críticas de los equipos de producción para detectar desviaciones de forma inmediata sin depender de registros manuales.</td>
      <td></td>
    </tr>
    <tr>
      <td>US09</td>
      <td>Visualización del dashboard de telemetría</td>
      <td>Como jefe de Aseguramiento de Calidad quiero acceder a un dashboard que muestre en tiempo real las variables críticas (temperatura, presión, pH) de los equipos de producción para supervisar el cumplimiento BPM sin estar físicamente en la planta.</td>
      <td>
        <strong>Escenario 1: Dashboard con datos disponibles</strong><br>
        <strong>Dado que</strong> el jefe de QA está autenticado y tiene equipos IoT vinculados<br>
        <strong>Cuando</strong> accede al dashboard de telemetría<br>
        <strong>Entonces</strong> el sistema muestra gráficos actualizados en tiempo real con los valores de temperatura, presión y pH de cada equipo registrado.<br><br>
        <strong>Escenario 2: Sin equipos vinculados</strong><br>
        <strong>Dado que</strong> el jefe de QA accede al dashboard sin equipos configurados<br>
        <strong>Cuando</strong> carga la vista<br>
        <strong>Entonces</strong> el sistema muestra un mensaje informativo indicando que debe vincular al menos un equipo para comenzar el monitoreo.
      </td>
    </tr>
    <tr>
      <td>US10</td>
      <td>Visualización de historial de telemetría por equipo</td>
      <td>Como jefe de Aseguramiento de Calidad quiero consultar el historial de variables registradas por un equipo específico para analizar el comportamiento del proceso en periodos anteriores.</td>
      <td>
        <strong>Escenario 1: Historial disponible</strong><br>
        <strong>Dado que</strong> el usuario selecciona un equipo y un rango de fechas<br>
        <strong>Cuando</strong> solicita el historial de telemetría<br>
        <strong>Entonces</strong> el sistema muestra un gráfico con la evolución de las variables en el periodo seleccionado.<br><br>
        <strong>Escenario 2: Sin datos en el rango seleccionado</strong><br>
        <strong>Dado que</strong> el usuario selecciona un rango de fechas sin registros<br>
        <strong>Cuando</strong> solicita el historial<br>
        <strong>Entonces</strong> el sistema muestra un mensaje indicando que no hay datos disponibles para el periodo indicado.
      </td>
    </tr>
    <tr>
      <td>US11</td>
      <td>Vinculación de equipos IoT a la plataforma</td>
      <td>Como jefe de Aseguramiento de Calidad quiero registrar y vincular los equipos industriales (autoclaves, medidores de pH) a QualiTrack para que la plataforma reciba automáticamente su telemetría.</td>
      <td>
        <strong>Escenario 1: Vinculación exitosa de equipo</strong><br>
        <strong>Dado que</strong> el jefe de QA registra un nuevo equipo con su identificador único (device_id)<br>
        <strong>Cuando</strong> confirma la vinculación<br>
        <strong>Entonces</strong> el sistema asocia el equipo al laboratorio y comienza a recibir su telemetría en el dashboard.<br><br>
        <strong>Escenario 2: Equipo ya vinculado</strong><br>
        <strong>Dado que</strong> el usuario intenta vincular un equipo con un device_id ya registrado<br>
        <strong>Cuando</strong> envía el formulario de vinculación<br>
        <strong>Entonces</strong> el sistema rechaza la operación e informa que el equipo ya está asociado.
      </td>
    </tr>
    <!-- EP04 -->
    <tr>
      <td>EP04</td>
      <td>Gestión de Lotes (Batch Record)</td>
      <td>Como supervisor de calidad quiero gestionar el ciclo de vida completo de cada lote de producción de forma digital para garantizar la trazabilidad inmutable exigida por DIGEMID.</td>
      <td></td>
    </tr>
    <tr>
      <td>US12</td>
      <td>Registro de nuevo lote de producción</td>
      <td>Como jefe de Aseguramiento de Calidad quiero registrar un nuevo lote de producción en la plataforma para iniciar el seguimiento digital de su ciclo de fabricación.</td>
      <td>
        <strong>Escenario 1: Creación exitosa de lote</strong><br>
        <strong>Dado que</strong> el jefe de QA proporciona los datos del lote (código, producto, fecha de inicio, equipos asignados)<br>
        <strong>Cuando</strong> envía el formulario de registro<br>
        <strong>Entonces</strong> el sistema crea el lote, genera un ID único y lo asocia a los equipos y variables de telemetría correspondientes.<br><br>
        <strong>Escenario 2: Datos requeridos faltantes</strong><br>
        <strong>Dado que</strong> el usuario intenta crear un lote con campos obligatorios vacíos<br>
        <strong>Cuando</strong> envía el formulario<br>
        <strong>Entonces</strong> el sistema muestra mensajes específicos indicando los campos obligatorios sin crear el lote.
      </td>
    </tr>
    <tr>
      <td>US13</td>
      <td>Consulta del historial de un lote</td>
      <td>Como jefe de Aseguramiento de Calidad quiero consultar el historial completo de un lote para verificar que todas las variables del proceso se mantuvieron dentro de los parámetros BPM establecidos.</td>
      <td>
        <strong>Escenario 1: Historial completo disponible</strong><br>
        <strong>Dado que</strong> el usuario selecciona un lote existente<br>
        <strong>Cuando</strong> accede a su historial<br>
        <strong>Entonces</strong> el sistema muestra el registro cronológico e inmutable de todas las variables capturadas durante el proceso de fabricación.<br><br>
        <strong>Escenario 2: Lote sin registros de telemetría</strong><br>
        <strong>Dado que</strong> el usuario consulta un lote recién creado sin datos aún<br>
        <strong>Cuando</strong> accede a su historial<br>
        <strong>Entonces</strong> el sistema muestra un mensaje indicando que aún no se han registrado datos de telemetría para ese lote.
      </td>
    </tr>
    <tr>
      <td>US14</td>
      <td>Liberación digital de lote</td>
      <td>Como jefe de Aseguramiento de Calidad quiero firmar digitalmente la liberación de un lote de producción que haya cumplido todos los parámetros BPM para agilizar la cadena de suministro sin depender de firmas físicas.</td>
      <td>
        <strong>Escenario 1: Liberación exitosa de lote</strong><br>
        <strong>Dado que</strong> el lote ha completado el proceso y todos sus parámetros están dentro del rango<br>
        <strong>Cuando</strong> el jefe de QA aplica su firma digital en la plataforma<br>
        <strong>Entonces</strong> el sistema registra la liberación con fecha, hora y firma del responsable, y el lote queda marcado como "Liberado".<br><br>
        <strong>Escenario 2: Intento de liberar lote bloqueado</strong><br>
        <strong>Dado que</strong> el lote tiene desviaciones de parámetros detectadas y está en estado "Bloqueado"<br>
        <strong>Cuando</strong> el usuario intenta liberar el lote<br>
        <strong>Entonces</strong> el sistema rechaza la acción y muestra las desviaciones registradas que impiden la liberación.
      </td>
    </tr>
    <tr>
      <td>US15</td>
      <td>Rechazo y documentación de lote no conforme</td>
      <td>Como jefe de Aseguramiento de Calidad quiero registrar el rechazo de un lote no conforme con su justificación para mantener un registro documental completo del evento de desviación.</td>
      <td>
        <strong>Escenario 1: Rechazo exitoso con justificación</strong><br>
        <strong>Dado que</strong> el jefe de QA selecciona un lote bloqueado por desviación<br>
        <strong>Cuando</strong> documenta la causa raíz y confirma el rechazo<br>
        <strong>Entonces</strong> el sistema registra el rechazo de forma inmutable con fecha, responsable y justificación, marcando el lote como "Rechazado".<br><br>
        <strong>Escenario 2: Rechazo sin justificación</strong><br>
        <strong>Dado que</strong> el usuario intenta rechazar un lote sin completar la causa raíz<br>
        <strong>Cuando</strong> confirma la acción<br>
        <strong>Entonces</strong> el sistema solicita obligatoriamente la justificación antes de proceder.
      </td>
    </tr>
    <!-- EP05 -->
    <tr>
      <td>EP05</td>
      <td>Motor de Alertas y Bloqueo (Compliance)</td>
      <td>Como operario de planta quiero recibir alertas automáticas cuando una variable crítica salga del rango permitido para actuar de forma inmediata y evitar la liberación de productos defectuosos.</td>
      <td></td>
    </tr>
    <tr>
      <td>US16</td>
      <td>Configuración de parámetros BPM por equipo</td>
      <td>Como jefe de Aseguramiento de Calidad quiero configurar los rangos permitidos de temperatura, presión y pH para cada equipo del laboratorio para que el sistema pueda detectar automáticamente las desviaciones normativas.</td>
      <td>
        <strong>Escenario 1: Configuración exitosa de parámetros</strong><br>
        <strong>Dado que</strong> el jefe de QA accede a la configuración de un equipo registrado<br>
        <strong>Cuando</strong> establece los valores mínimos y máximos permitidos para cada variable<br>
        <strong>Entonces</strong> el sistema guarda los parámetros y los aplica como referencia para la evaluación de telemetría en tiempo real.<br><br>
        <strong>Escenario 2: Valores de rango inválidos</strong><br>
        <strong>Dado que</strong> el usuario ingresa un valor mínimo mayor al máximo<br>
        <strong>Cuando</strong> intenta guardar la configuración<br>
        <strong>Entonces</strong> el sistema muestra un mensaje de error indicando el conflicto de valores.
      </td>
    </tr>
    <tr>
      <td>US17</td>
      <td>Alerta automática ante desviación de parámetros</td>
      <td>Como operario de planta quiero recibir una alerta visual inmediata en la plataforma cuando una variable crítica de un equipo supere o caiga por debajo del rango BPM configurado para poder actuar en menos de 5 segundos.</td>
      <td>
        <strong>Escenario 1: Alerta generada por desviación detectada</strong><br>
        <strong>Dado que</strong> un equipo transmite un valor fuera del rango BPM configurado<br>
        <strong>Cuando</strong> el motor de compliance evalúa la telemetría entrante<br>
        <strong>Entonces</strong> el sistema genera una alerta visual inmediata en el dashboard indicando el equipo, la variable afectada, el valor registrado y la hora del evento.<br><br>
        <strong>Escenario 2: Variable dentro del rango normal</strong><br>
        <strong>Dado que</strong> el equipo transmite valores dentro del rango permitido<br>
        <strong>Cuando</strong> el motor evalúa la telemetría<br>
        <strong>Entonces</strong> el sistema no genera alertas y mantiene el indicador del equipo en estado "Normal".
      </td>
    </tr>
    <tr>
      <td>US18</td>
      <td>Bloqueo automático de lote por desviación</td>
      <td>Como jefe de Aseguramiento de Calidad quiero que el sistema bloquee automáticamente un lote cuando se detecte una desviación crítica en sus parámetros para impedir que avance en la cadena de suministro hasta ser investigado.</td>
      <td>
        <strong>Escenario 1: Bloqueo automático exitoso</strong><br>
        <strong>Dado que</strong> el motor de compliance detecta una desviación crítica en un lote activo<br>
        <strong>Cuando</strong> la variable supera el umbral establecido<br>
        <strong>Entonces</strong> el sistema bloquea el lote automáticamente, lo marca como "En investigación" y notifica al jefe de QA con los detalles de la desviación.<br><br>
        <strong>Escenario 2: Desviación leve sin bloqueo</strong><br>
        <strong>Dado que</strong> el motor detecta una desviación menor configurada como "advertencia"<br>
        <strong>Cuando</strong> evalúa la telemetría<br>
        <strong>Entonces</strong> el sistema genera una advertencia sin bloquear el lote, registrando el evento para auditoría.
      </td>
    </tr>
    <tr>
      <td>US19</td>
      <td>Historial de alertas y eventos de compliance</td>
      <td>Como jefe de Aseguramiento de Calidad quiero consultar el historial completo de alertas y eventos de desviación registrados en la plataforma para analizar patrones de falla y documentar las acciones correctivas tomadas.</td>
      <td>
        <strong>Escenario 1: Historial de alertas disponible</strong><br>
        <strong>Dado que</strong> el usuario accede a la sección de historial de eventos<br>
        <strong>Cuando</strong> aplica filtros por equipo, fecha o tipo de alerta<br>
        <strong>Entonces</strong> el sistema muestra la lista de eventos ordenados cronológicamente con detalles de cada desviación registrada.<br><br>
        <strong>Escenario 2: Sin alertas en el periodo seleccionado</strong><br>
        <strong>Dado que</strong> el usuario filtra por un periodo sin eventos<br>
        <strong>Cuando</strong> consulta el historial<br>
        <strong>Entonces</strong> el sistema muestra un mensaje indicando que no se registraron alertas en ese periodo.
      </td>
    </tr>
    <!-- EP06 -->
    <tr>
      <td>EP06</td>
      <td>Generación de Reportes de Auditoría</td>
      <td>Como jefe de Aseguramiento de Calidad quiero generar reportes digitales e inmutables de los procesos de fabricación para presentarlos como evidencia en inspecciones de DIGEMID sin necesidad de recopilar documentos físicos.</td>
      <td></td>
    </tr>
    <tr>
      <td>US20</td>
      <td>Generación de reporte de trazabilidad de lote</td>
      <td>Como jefe de Aseguramiento de Calidad quiero generar un reporte PDF completo e inmutable del historial de fabricación de un lote específico para presentarlo como evidencia en auditorías regulatorias.</td>
      <td>
        <strong>Escenario 1: Generación exitosa de reporte</strong><br>
        <strong>Dado que</strong> el usuario selecciona un lote con historial completo<br>
        <strong>Cuando</strong> solicita la generación del reporte de trazabilidad<br>
        <strong>Entonces</strong> el sistema genera un PDF no editable con el registro cronológico de variables, alertas, responsables y estado final del lote.<br><br>
        <strong>Escenario 2: Lote sin datos suficientes</strong><br>
        <strong>Dado que</strong> el usuario intenta generar un reporte de un lote sin registros completos<br>
        <strong>Cuando</strong> solicita la generación<br>
        <strong>Entonces</strong> el sistema advierte que el lote no tiene datos suficientes para generar un reporte válido para auditoría.
      </td>
    </tr>
    <tr>
      <td>US21</td>
      <td>Generación de reporte de cumplimiento BPM por periodo</td>
      <td>Como jefe de Aseguramiento de Calidad quiero generar un reporte consolidado de cumplimiento BPM por un periodo de tiempo determinado para identificar tendencias y preparar la documentación antes de una auditoría.</td>
      <td>
        <strong>Escenario 1: Reporte consolidado generado exitosamente</strong><br>
        <strong>Dado que</strong> el usuario selecciona un rango de fechas con datos disponibles<br>
        <strong>Cuando</strong> solicita el reporte de cumplimiento del periodo<br>
        <strong>Entonces</strong> el sistema genera un documento PDF con el resumen de lotes procesados, alertas registradas, desviaciones y porcentaje de cumplimiento BPM.<br><br>
        <strong>Escenario 2: Sin datos en el periodo seleccionado</strong><br>
        <strong>Dado que</strong> el usuario selecciona un periodo sin actividad registrada<br>
        <strong>Cuando</strong> solicita el reporte<br>
        <strong>Entonces</strong> el sistema informa que no existen datos para generar el reporte en ese periodo.
      </td>
    </tr>
    <tr>
      <td>US22</td>
      <td>Exportación de log de eventos inmutable</td>
      <td>Como auditor regulatorio quiero exportar el log completo de eventos de un equipo o lote en formato no editable para verificar la integridad de los datos durante una inspección de DIGEMID.</td>
      <td>
        <strong>Escenario 1: Exportación exitosa del log</strong><br>
        <strong>Dado que</strong> el auditor selecciona un equipo o lote y un rango de fechas<br>
        <strong>Cuando</strong> solicita la exportación del log de eventos<br>
        <strong>Entonces</strong> el sistema descarga un archivo PDF con el registro inmutable de todos los eventos, marcas de tiempo y valores registrados.<br><br>
        <strong>Escenario 2: Intento de exportación sin permisos</strong><br>
        <strong>Dado que</strong> un operario intenta exportar un log de auditoría<br>
        <strong>Cuando</strong> solicita la exportación<br>
        <strong>Entonces</strong> el sistema deniega el acceso y muestra un mensaje de restricción de rol.
      </td>
    </tr>
    <!-- EP07 -->
    <tr>
      <td>EP07</td>
      <td>Ingesta de datos IoT</td>
      <td>Como desarrollador backend quiero implementar los endpoints necesarios para recibir, validar y almacenar la telemetría enviada por los sensores industriales conectados a QualiTrack.</td>
      <td></td>
    </tr>
    <tr>
      <td>TS-IOT01</td>
      <td>Endpoint de ingesta de telemetría</td>
      <td>Como desarrollador backend quiero implementar un endpoint POST para recibir los datos de telemetría enviados por los sensores IoT (temperatura, presión, pH) y persistirlos como registros de medición asociados al equipo y lote correspondiente.</td>
      <td>
        <strong>Escenario 1: Recepción de datos válidos</strong><br>
        - <strong>Dado</strong> que existe un sensor (device_id) vinculado a un equipo en el sistema<br>
        - <strong>Cuando</strong> el sensor envía un POST a <code>/api/v1/telemetry</code> con: deviceId, loteId, temperatura, presion, pH, timestamp<br>
        - <strong>Entonces</strong> la API responde con <code>202 Accepted</code> y persiste el registro con los campos correspondientes.<br><br>
        <strong>Escenario 2: Sensor no reconocido</strong><br>
        - <strong>Dado</strong> que se recibe un POST con un deviceId no registrado<br>
        - <strong>Cuando</strong> la API valida el identificador<br>
        - <strong>Entonces</strong> responde con <code>404 Not Found</code> y registra el intento en los logs de seguridad.
      </td>
    </tr>
    <tr>
      <td>TS-IOT02</td>
      <td>Servicio de evaluación de compliance BPM</td>
      <td>Como desarrollador backend quiero implementar un servicio que evalúe cada medición recibida contra los parámetros BPM configurados para el equipo y clasifique su estado como "Conforme" o "Desviación".</td>
      <td>
        <strong>Escenario 1: Medición dentro de rango</strong><br>
        - <strong>Dado</strong> que se recibe una medición con valores dentro de los parámetros configurados<br>
        - <strong>Cuando</strong> el servicio de compliance evalúa los datos<br>
        - <strong>Entonces</strong> clasifica la medición como "Conforme" y no genera alertas.<br><br>
        <strong>Escenario 2: Medición fuera de rango</strong><br>
        - <strong>Dado</strong> que se recibe una medición con una variable fuera del rango BPM<br>
        - <strong>Cuando</strong> el servicio evalúa los datos<br>
        - <strong>Entonces</strong> clasifica la medición como "Desviación", bloquea el lote asociado y publica un evento de alerta.
      </td>
    </tr>
    <!-- EP08 -->
    <tr>
      <td>EP08</td>
      <td>Gestión de equipos y sensores</td>
      <td>Como jefe de Aseguramiento de Calidad quiero gestionar los equipos industriales y sus sensores asociados para mantener actualizado el inventario de activos conectados a la plataforma.</td>
      <td></td>
    </tr>
    <tr>
      <td>TS-EQ001</td>
      <td>Registrar equipo industrial</td>
      <td>Como desarrollador backend quiero implementar un endpoint POST para registrar nuevos equipos industriales con sus datos y parámetros BPM configurables.</td>
      <td>
        <strong>Escenario 1: Creación exitosa</strong><br>
        - <strong>Dado</strong> que se recibe POST a <code>/api/v1/labs/{labId}/equipment</code> con datos válidos<br>
        - <strong>Cuando</strong> la API valida permisos y persiste el equipo<br>
        - <strong>Entonces</strong> responde con <code>201 Created</code> y retorna el equipo con su ID único, labId, nombre, tipo, device_id y parámetros BPM.<br><br>
        <strong>Escenario 2: Error de validación</strong><br>
        - <strong>Dado</strong> que se recibe una solicitud con datos inválidos<br>
        - <strong>Cuando</strong> la API detecta errores<br>
        - <strong>Entonces</strong> responde con <code>400 Bad Request</code> con detalles de los campos inválidos.
      </td>
    </tr>
    <tr>
      <td>TS-EQ002</td>
      <td>Listar equipos del laboratorio</td>
      <td>Como desarrollador backend quiero implementar un endpoint GET para listar todos los equipos registrados de un laboratorio con su estado de conexión actual.</td>
      <td>
        <strong>Escenario 1: Lista de equipos disponible</strong><br>
        - <strong>Dado</strong> que se recibe GET a <code>/api/v1/labs/{labId}/equipment</code><br>
        - <strong>Cuando</strong> la API busca los equipos del laboratorio<br>
        - <strong>Entonces</strong> responde con <code>200 OK</code> y retorna la lista de equipos con su estado (Conectado/Desconectado) y última telemetría recibida.<br><br>
        <strong>Escenario 2: Sin equipos registrados</strong><br>
        - <strong>Dado</strong> que el laboratorio no tiene equipos registrados<br>
        - <strong>Cuando</strong> la API busca<br>
        - <strong>Entonces</strong> responde con <code>200 OK</code> y retorna una lista vacía.
      </td>
    </tr>
    <!-- EP09 -->
    <tr>
      <td>EP09</td>
      <td>Gestión de lotes (API)</td>
      <td>Como desarrollador backend quiero implementar los endpoints CRUD necesarios para la gestión completa del ciclo de vida de los lotes de producción.</td>
      <td></td>
    </tr>
    <tr>
      <td>TS-LOT001</td>
      <td>Crear lote de producción</td>
      <td>Como desarrollador backend quiero implementar un endpoint POST para crear nuevos lotes de producción con validaciones obligatorias.</td>
      <td>
        <strong>Escenario 1: Creación exitosa</strong><br>
        - <strong>Dado</strong> que se recibe POST a <code>/api/v1/labs/{labId}/batches</code> con datos válidos<br>
        - <strong>Cuando</strong> la API valida permisos y persiste el lote<br>
        - <strong>Entonces</strong> responde con <code>201 Created</code> y retorna el lote con: id, labId, batchCode, productName, startDate, status, equipmentId, createdAt.<br><br>
        <strong>Escenario 2: Código de lote duplicado</strong><br>
        - <strong>Dado</strong> que se intenta crear un lote con un batchCode ya existente<br>
        - <strong>Cuando</strong> la API valida unicidad<br>
        - <strong>Entonces</strong> responde con <code>409 Conflict</code>.
      </td>
    </tr>
    <tr>
      <td>TS-LOT002</td>
      <td>Obtener detalle de lote</td>
      <td>Como desarrollador backend quiero implementar un endpoint GET para obtener el detalle completo de un lote incluyendo su historial de telemetría y alertas asociadas.</td>
      <td>
        <strong>Escenario 1: Lote encontrado</strong><br>
        - <strong>Dado</strong> que se recibe GET a <code>/api/v1/labs/{labId}/batches/{batchId}</code><br>
        - <strong>Cuando</strong> la API encuentra el lote<br>
        - <strong>Entonces</strong> responde con <code>200 OK</code> y retorna el detalle completo del lote.<br><br>
        <strong>Escenario 2: Lote no encontrado</strong><br>
        - <strong>Dado</strong> que el batchId no existe<br>
        - <strong>Cuando</strong> la API busca el lote<br>
        - <strong>Entonces</strong> responde con <code>404 Not Found</code>.
      </td>
    </tr>
    <tr>
      <td>TS-LOT003</td>
      <td>Actualizar estado de lote</td>
      <td>Como desarrollador backend quiero implementar un endpoint PATCH para actualizar el estado de un lote (En proceso, Bloqueado, Liberado, Rechazado) con registro del responsable.</td>
      <td>
        <strong>Escenario 1: Actualización exitosa</strong><br>
        - <strong>Dado</strong> que se recibe PATCH a <code>/api/v1/labs/{labId}/batches/{batchId}/status</code> con el nuevo estado y responsable<br>
        - <strong>Cuando</strong> la API valida la transición de estado y los permisos del usuario<br>
        - <strong>Entonces</strong> responde con <code>200 OK</code> con el lote actualizado y el registro del cambio.<br><br>
        <strong>Escenario 2: Transición de estado no permitida</strong><br>
        - <strong>Dado</strong> que se intenta cambiar un lote "Liberado" a "En proceso"<br>
        - <strong>Cuando</strong> la API valida la transición<br>
        - <strong>Entonces</strong> responde con <code>400 Bad Request</code> indicando que la transición no está permitida.
      </td>
    </tr>
    <!-- EP10 -->
    <tr>
      <td>EP10</td>
      <td>Reportes y auditoría (API)</td>
      <td>Como desarrollador backend quiero implementar los endpoints necesarios para la generación de reportes de trazabilidad y exportación de logs inmutables para auditorías regulatorias.</td>
      <td></td>
    </tr>
    <tr>
      <td>TS-REP001</td>
      <td>Generar reporte PDF de lote</td>
      <td>Como desarrollador backend quiero implementar un endpoint GET que genere y devuelva un reporte PDF inmutable del historial completo de un lote para su presentación en auditorías.</td>
      <td>
        <strong>Escenario 1: Generación exitosa</strong><br>
        - <strong>Dado</strong> que se recibe GET a <code>/api/v1/labs/{labId}/batches/{batchId}/report</code><br>
        - <strong>Cuando</strong> la API valida que el lote tiene datos completos<br>
        - <strong>Entonces</strong> responde con <code>200 OK</code> y retorna el archivo PDF con el historial inmutable del lote.<br><br>
        <strong>Escenario 2: Datos insuficientes para el reporte</strong><br>
        - <strong>Dado</strong> que el lote no tiene registros de telemetría<br>
        - <strong>Cuando</strong> la API intenta generar el reporte<br>
        - <strong>Entonces</strong> responde con <code>422 Unprocessable Entity</code> indicando datos insuficientes.
      </td>
    </tr>
    <tr>
      <td>TS-REP002</td>
      <td>Exportar log de eventos de equipo</td>
      <td>Como desarrollador backend quiero implementar un endpoint GET que exporte el log completo de eventos de un equipo en un rango de fechas en formato PDF no editable.</td>
      <td>
        <strong>Escenario 1: Exportación exitosa</strong><br>
        - <strong>Dado</strong> que se recibe GET a <code>/api/v1/labs/{labId}/equipment/{equipmentId}/logs</code> con parámetros de fecha<br>
        - <strong>Cuando</strong> la API obtiene los registros del periodo<br>
        - <strong>Entonces</strong> responde con <code>200 OK</code> y retorna el PDF con el log cronológico e inmutable.<br><br>
        <strong>Escenario 2: Sin datos en el periodo</strong><br>
        - <strong>Dado</strong> que no hay registros en el rango de fechas solicitado<br>
        - <strong>Cuando</strong> la API busca los datos<br>
        - <strong>Entonces</strong> responde con <code>404 Not Found</code> con mensaje descriptivo.
      </td>
    </tr>

  </tbody>
</table>

<div style="page-break-after: always;"></div>

## 3.2. Impact Mapping

## 3.3. Product Backlog
