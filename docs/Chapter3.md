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
      <td>Como visitante, quiero tener una experiencia fluida en el sitio web, para conocer los servicios de QualiTrack y tomar decisiones informadas.</td>
      <td></td>
    </tr>
    <tr>
      <td>US01</td>
      <td>Menú de navegación</td>
      <td>Como visitante, quiero explorar las secciones principales del sitio, para informarme sobre las características, planes y contacto de QualiTrack.</td>
      <td>
        <strong>Escenario 1: Navegación exitosa</strong><br>
        <strong>Dado que</strong> el visitante se encuentra en la landing page<br>
        <strong>Cuando</strong> la navegación principal es desplegada<br>
        <strong>Entonces</strong> el sistema desplaza al usuario a la sección correspondiente en menos de 2 segundos.<br><br>
        <strong>Escenario 2: Navegación no disponible</strong><br>
        <strong>Dado que</strong> el servicio web presenta una falla temporal<br>
        <strong>Cuando</strong> el visitante accede a la navegación<br>
        <strong>Entonces</strong> el sistema indica la indisponibilidad y sugiere alternativas de acceso.
      </td>
    </tr>
    <tr>
      <td>US02</td>
      <td>Visualización de planes de suscripción</td>
      <td>Como visitante del segmento QA Manager, quiero comparar los planes disponibles junto a su precio y características, para elegir el que mejor se adapte a las necesidades de mi organización.</td>
      <td>
        <strong>Escenario 1: Visualización de planes disponibles</strong><br>
        <strong>Dado que</strong> el visitante navega a la sección de planes<br>
        <strong>Cuando</strong> el sistema carga la información de suscripciones<br>
        <strong>Entonces</strong>el visitante visualiza cada plan con nombre, precio mensual, límite de usuarios y funcionalidades incluidas.<br><br>
        <strong>Escenario 2: Planes no disponibles</strong><br>
        <strong>Dado que</strong> ocurre un error de carga en la sección de planes<br>
        <strong>Cuando</strong> el visitante accede al contenido<br>
        <strong>Entonces</strong> el sistema muestra un mensaje indicando que los planes no están disponibles temporalmente.
      </td>
    </tr>
    <tr>
      <td>US03</td>
      <td>Visualización del equipo creador</td>
      <td>Como visitante, quiero conocer al equipo detrás de QualiTrack, para generar confianza en el servicio antes de contratar.</td>
      <td>
        <strong>Escenario 1: Acceso a información del equipo</strong><br>
        <strong>Dado que</strong> el visitante navega a la sección del equipo<br>
        <strong>Cuando</strong> el sistema carga la información correctamente<br>
        <strong>Entonces</strong> el visitante visualiza el nombre, rol y especialidad de cada integrante del equipo.<br><br>
        <strong>Escenario 2: Información del equipo no disponible</strong><br>
        <strong>Dado que</strong> que ocurre un error de carga en la sección del equipo<br>
        <strong>Cuando</strong> el visitante accede a la información<br>
        <strong>Entonces</strong> el sistema muestra un mensaje indicando que la información no está disponible temporalmente.
      </td>
    </tr>
    <tr>
      <td>US04</td>
      <td>Formulario de contacto</td>
      <td>Como visitante, quiero enviar consultas al equipo de QualiTrack, para obtener información adicional sobre el servicio.</td>
      <td>
        <strong>Escenario 1: Envío exitoso de consulta</strong><br>
        <strong>Dado que</strong> el visitante completa todos los campos requeridos<br>
        <strong>Cuando</strong> el visitante envía la consulta<br>
        <strong>Entonces</strong> el sistema registra la consulta y confirma su recepción.<br><br>
        <strong>Escenario 2: Validación de campos incompletos</strong><br>
        <strong>Dado que</strong> el visitante envía el formulario con campos incompletos<br>
        <strong>Cuando</strong> el sistema valida la información<br>
        <strong>Entonces</strong> el sistema indica qué campos requieren completarse.<br><br>
        <strong>Escenario 3: Error en el envío</strong><br>
        <strong>Dado que</strong> ocurre un error en el servicio de envío<br>
        <strong>Cuando</strong> el visitante envía la consulta<br>
        <strong>Entonces</strong> el sistema muestra un mensaje de error y permite reenviar el formulario.
      </td>
    </tr>
    <tr>
      <td>US05</td>
      <td>Cambio de idioma</td>
      <td>Como visitante, quiero cambiar el idioma del sitio entre español e inglés, para comprender mejor la propuesta de valor en mi idioma preferido.</td>
      <td>
        <strong>Escenario 1: Cambio exitoso de idioma</strong><br>
        <strong>Dado que</strong> el visitante selecciona un idioma diferente<br>
        <strong>Cuando</strong> el sistema procesa la selección<br>
        <strong>Entonces</strong> todo el contenido visible del sitio se actualiza al idioma seleccionado en menos de 3 segundos.<br><br>
        <strong>Escenario 2: Persistencia de preferencia</strong><br>
        <strong>Dado que</strong> el visitante ha seleccionado un idioma específico<br>
        <strong>Cuando</strong> el visitante navega entre secciones del sitio<br>
        <strong>Entonces</strong> el sistema mantiene el idioma seleccionado durante toda la sesión activa.
      </td>
    </tr>
    <tr>
      <td>US40</td>
      <td>Términos y condiciones de uso</td>
      <td>Como visitante, quiero acceder a los términos y condiciones de QualiTrack, para conocer las políticas antes de contratar el servicio.</td>
      <td>
        <strong>Escenario 1: Acceso a términos y condiciones</strong><br>
        <strong>Dado que</strong> el visitante navega a la sección de términos<br>
        <strong>Cuando</strong> el documento de términos está disponible<br>
        <strong>Entonces</strong> el visitante visualiza el contenido completo de las políticas y condiciones de uso.
      </td>
    </tr>
    <!-- EP02 -->
    <tr>
      <td>EP02</td>
      <td>Gestión de acceso y autenticación</td>
      <td>Como usuario de la plataforma, quiero gestionar mi acceso de manera segura, para proteger la información de mi laboratorio y mantener la trazabilidad de acciones.</td>
      <td></td>
    </tr>
    <tr>
      <td>US06</td>
      <td>Registro de laboratorio en la plataforma</td>
      <td>Como QA Manager, quiero registrar mi laboratorio en QualiTrack, para comenzar a gestionar los procesos de calidad digitalmente.</td>
      <td>
        <strong>Escenario 1: Registro exitoso de laboratorio</strong><br>
        <strong>Dado que</strong> el QA Manager completa todos los datos institucionales requeridos<br>
        <strong>Cuando</strong> el QA Manager envía el formulario de registro<br>
        <strong>Entonces</strong> el sistema crea la cuenta del laboratorio y confirma el registro exitoso.<br><br>
        <strong>Escenario 2: Validación de datos incompletos</strong><br>
        <strong>Dado que</strong> el QA Manager envía el formulario con datos incompletos<br>
        <strong>Cuando</strong> el sistema valida la información<br>
        <strong>Entonces</strong> el sistema indica qué campos son obligatorios y requieren completarse.<br><br>
        <strong>Escenario 3: Laboratorio ya registrado</strong><br>
        <strong>Dado que</strong> el QA Manager registra un laboratorio que ya existe en el sistema<br>
        <strong>Cuando</strong> el sistema valida la información<br>
        <strong>Entonces</strong> el sistema indica que el laboratorio ya está registrado.
      </td>
    </tr>
    <tr>
      <td>US07</td>
      <td>Inicio de sesión seguro</td>
      <td>Como usuario registrado, quiero iniciar sesión con mis credenciales, para acceder a las funcionalidades según mi rol asignado.</td>
      <td>
        <strong>Escenario 1: Inicio de sesión exitoso</strong><br>
        <strong>Dado que</strong> el usuario ingresa credenciales válidas<br>
        <strong>Cuando</strong> el usuario solicita iniciar sesión<br>
        <strong>Entonces</strong> el sistema autentica al usuario y le otorga acceso a las funcionalidades de su rol.<br><br>
        <strong>Escenario 2: Credenciales inválidas</strong><br>
        <strong>Dado que</strong> el usuario ingresa credenciales incorrectas<br>
        <strong>Cuando</strong> el usuario solicita iniciar sesión<br>
        <strong>Entonces</strong> el sistema deniega el acceso e indica que las credenciales son incorrectas.<br><br>
        <strong>Escenario 3: Cuenta desactivada</strong><br>
        <strong>Dado que</strong> el usuario solicita iniciar sesión con una cuenta desactivada<br>
        <strong>Cuando</strong> el sistema valida las credenciales<br>
        <strong>Entonces</strong> el sistema deniega el acceso e indica que la cuenta está desactivada.
      </td>
    </tr>
    <tr>
      <td>US08</td>
      <td>Recuperación de contraseña</td>
      <td>Como usuario registrado, quiero recuperar mi contraseña olvidada, para no perder acceso a la plataforma.</td>
      <td>
        <strong>Escenario 1: Solicitud exitosa de recuperación</strong><br>
        <strong>Dado que</strong> el usuario ingresa un correo registrado<br>
        <strong>Cuando</strong> solicita recuperar su contraseña<br>
        <strong>Entonces</strong> el sistema envía un enlace de recuperación válido por 15 minutos al correo electrónico registrado.<br><br>
        <strong>Escenario 2: Correo no registrado</strong><br>
        <strong>Dado que</strong> el usuario solicita recuperar la contraseña con un correo no registrado<br>
        <strong>Cuando</strong> el sistema valida el correo electrónico<br>
        <strong>Entonces</strong> el sistema indica que el correo no está asociado a ninguna cuenta.<br><br>
        <strong>Escenario 3: Restablecimiento exitoso</strong><br>
        <strong>Dado que</strong> el usuario accede al enlace de recuperación válido<br>
        <strong>Cuando</strong> ingresa y confirma una nueva contraseña que cumple las políticas de seguridad<br>
        <strong>Entonces</strong> el sistema actualiza la contraseña y permite iniciar sesión con la nueva credencial.
      </td>
    </tr>
    <tr>
      <td>US09</td>
      <td>Gestión de roles y permisos</td>
      <td>Como QA Manager, quiero gestionar los roles de mi equipo, para garantizar accesos según responsabilidades de cada miembro.</td>
      <td>
        <strong>Escenario 1: Asignación exitosa de rol</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona un rol específico para un usuario<br>
        <strong>Cuando</strong> el QA Manager confirma la asignación<br>
        <strong>Entonces</strong> el sistema actualiza los permisos del usuario según el rol asignado.<br><br>
        <strong>Escenario 2: Modificación de rol existente</strong><br>
        <strong>Dado que</strong> el QA Manager modifica el rol de un usuario activo<br>
        <strong>Cuando</strong> el sistema procesa el cambio<br>
        <strong>Entonces</strong> el sistema ajusta los permisos del usuario y registra la modificación en el log de auditoría.<br><br>
        <strong>Escenario 3: Revocación de permisos</strong><br>
        <strong>Dado que</strong> el QA Manager revoca permisos a un usuario<br>
        <strong>Cuando</strong> el sistema procesa la revocación<br>
        <strong>Entonces</strong> el usuario pierde acceso a las funcionalidades correspondientes de forma inmediata.
      </td>
    </tr>
    <tr>
      <td>US28</td>
      <td>Registro de operario o supervisor</td>
      <td>Como QA Manager, quiero registrar a los miembros del equipo técnico, para que puedan acceder a la plataforma según sus responsabilidades.</td>
      <td>
        <strong>Escenario 1: Registro exitoso de personal</strong><br>
        <strong>Dado que</strong> el QA Manager completa los datos del nuevo miembro<br>
        <strong>Cuando</strong> el QA Manager confirma el registro<br>
        <strong>Entonces</strong> el sistema crea la cuenta del usuario y envía las credenciales de acceso.<br><br>
        <strong>Escenario 2: Usuario ya registrado</strong><br>
        <strong>Dado que</strong> el QA Manager registra un usuario con credenciales existentes<br>
        <strong>Cuando</strong> el sistema valida la información<br>
        <strong>Entonces</strong> el sistema indica que el usuario ya está registrado en el laboratorio.
      </td>
    </tr>
    <tr>
      <td>US29</td>
      <td>Baja de personal del laboratorio</td>
      <td>Como QA Manager, quiero desactivar el acceso de personal que ya no forma parte del laboratorio, para mantener la seguridad de la información.</td>
      <td>
        <strong>Escenario 1: Desactivación exitosa</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona un usuario activo para dar de baja<br>
        <strong>Cuando</strong> el QA Manager confirma la desactivación<br>
        <strong>Entonces</strong> el sistema desactiva la cuenta y revoca todos los permisos del usuario de forma inmediata.<br><br>
        <strong>Escenario 2: Preservación del historial</strong><br>
        <strong>Dado que</strong> el QA Manager desactiva un usuario con acciones registradas<br>
        <strong>Cuando</strong> el sistema procesa la desactivación<br>
        <strong>Entonces</strong> el sistema mantiene el historial de acciones del usuario para fines de auditoría.
      </td>
    </tr>
    <tr>
      <td>US30</td>
      <td>Consulta de actividad de personal por turno</td>
      <td>Como QA Manager, quiero consultar el registro de actividad de cada operario por turno, para verificar responsabilidades y acciones realizadas.</td>
      <td>
        <strong>Escenario 1: Consulta exitosa de actividad</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona un operario y un periodo específico<br>
        <strong>Cuando</strong> el sistema recupera la información<br>
        <strong>Entonces</strong> el QA Manager visualiza el registro completo de acciones del operario en el periodo seleccionado.<br><br>
        <strong>Escenario 2: Sin actividad registrada</strong><br>
        <strong>Dado que</strong> el QA Manager consulta un periodo sin actividad del operario<br>
        <strong>Cuando</strong> el sistema busca registros<br>
        <strong>Entonces</strong> el sistema indica que no hay actividad registrada en el periodo seleccionado.
      </td>
    </tr>
    <!-- EP03 -->
    <tr>
      <td>EP03</td>
      <td>Gestión de equipos industriales e IoT</td>
      <td>Como QA Manager, quiero gestionar los equipos industriales y su telemetría IoT, para monitorear el cumplimiento de parámetros BPM en tiempo real.</td>
      <td></td>
    </tr>
    <tr>
      <td>US12</td>
      <td>Vinculación de equipos IoT</td>
      <td>Como QA Manager, quiero registrar y vincular los equipos industriales, para que la plataforma reciba su telemetría automáticamente.</td>
      <td>
        <strong>Escenario 1: Vinculación exitosa de equipo</strong><br>
        <strong>Dado que</strong> el QA Manager ingresa los datos de identificación del equipo<br>
        <strong>Cuando</strong> el sistema valida la conexión<br>
        <strong>Entonces</strong> el equipo queda vinculado y comienza a enviar telemetría a la plataforma.<br><br>
        <strong>Escenario 2: Error de conexión con equipo</strong><br>
        <strong>Dado que</strong> el QA Manager vincula un equipo sin conectividad<br>
        <strong>Cuando</strong> el sistema valida la conexión<br>
        <strong>Entonces</strong> el sistema indica que no se puede establecer comunicación con el equipo.<br><br>
        <strong>Escenario 3: Equipo ya vinculado</strong><br>
        <strong>Dado que</strong> el QA Manager vincula un equipo ya registrado<br>
        <strong>Cuando</strong> el sistema valida la información<br>
        <strong>Entonces</strong> el sistema indica que el equipo ya está vinculado al laboratorio.
      </td>
    </tr>
    <tr>
      <td>US19</td>
      <td>Configuración de parámetros BPM por equipo</td>
      <td>Como QA Manager, quiero configurar los rangos permitidos de variables por equipo, para que el sistema detecte desviaciones automáticamente.</td>
      <td>
        <strong>Escenario 1: Configuración exitosa de parámetros</strong><br>
        <strong>Dado que</strong> el QA Manager define los rangos mínimos y máximos para cada variable<br>
        <strong>Cuando</strong> el QA Manager guarda la configuración<br>
        <strong>Entonces</strong> el sistema almacena los parámetros BPM y los aplica en la evaluación de telemetría.<br><br>
        <strong>Escenario 2: Validación de rangos inconsistentes</strong><br>
        <strong>Dado que</strong> el QA Manager guarda parámetros con valores mínimos mayores a los máximos<br>
        <strong>Cuando</strong> el sistema valida la configuración<br>
        <strong>Entonces</strong> el sistema indica que los rangos son inconsistentes y requieren corrección.
      </td>
    </tr>
    <tr>
      <td>US10</td>
      <td>Visualización del dashboard de telemetría</td>
      <td>Como QA Manager, quiero un dashboard en tiempo real de las variables críticas, para supervisar el cumplimiento BPM de manera continua.</td>
      <td>
        <strong>Escenario 1: Dashboard con telemetría activa</strong><br>
        <strong>Dado que</strong> los equipos están enviando telemetría<br>
        <strong>Cuando</strong> el QA Manager accede al dashboard<br>
        <strong>Entonces</strong> el sistema muestra las variables críticas actualizadas con una frecuencia máxima de 5 segundos.<br><br>
        <strong>Escenario 2: Indicación de desviaciones</strong><br>
        <strong>Dado que</strong> una variable supera el rango BPM configurado<br>
        <strong>Cuando</strong> el sistema procesa la telemetría<br>
        <strong>Entonces</strong> el dashboard resalta la variable en color rojo y muestra una alerta visible para el usuario.<br><br>
        <strong>Escenario 3: Sin telemetría disponible</strong><br>
        <strong>Dado que</strong> no existen equipos enviando telemetría<br>
        <strong>Cuando</strong> el QA Manager accede al dashboard<br>
        <strong>Entonces</strong> el sistema muestra el mensaje “No hay datos disponibles en tiempo real”.
      </td>
    </tr>
    <tr>
      <td>US11</td>
      <td>Visualización del historial de telemetría</td>
      <td>Como QA Manager, quiero consultar el historial de variables de un equipo, para analizar el comportamiento del proceso en un periodo específico.</td>
      <td>
        <strong>Escenario 1: Consulta exitosa de historial</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona un equipo y un rango de fechas<br>
        <strong>Cuando</strong> el sistema recupera los datos históricos<br>
        <strong>Entonces</strong> el QA Manager visualiza la evolución de las variables en el periodo seleccionado.<br><br>
        <strong>Escenario 2: Periodo sin datos</strong><br>
        <strong>Dado que</strong> el QA Manager consulta un periodo sin telemetría registrada<br>
        <strong>Cuando</strong> el sistema busca los datos<br>
        <strong>Entonces</strong> el sistema indica que no hay registros disponibles en el periodo seleccionado.
      </td>
    </tr>
    <tr>
      <td>US13</td>
      <td>Consulta del estado de equipos en tiempo real</td>
      <td>Como Lab Operator, quiero verificar el estado de conexión de los equipos, para confirmar que están operativos antes de iniciar un proceso de producción.</td>
      <td>
        <strong>Escenario 1: Equipos conectados y operativos</strong><br>
        <strong>Dado que</strong> el Lab Operator consulta el estado de los equipos<br>
        <strong>Cuando</strong> todos los equipos están enviando telemetría<br>
        <strong>Entonces</strong> el Lab Operator visualiza que los equipos están conectados y operativos.<br><br>
        <strong>Escenario 2: Equipo desconectado</strong><br>
        <strong>Dado que</strong> el Lab Operator consulta el estado de los equipos<br>
        <strong>Cuando</strong> un equipo no está enviando telemetría<br>
        <strong>Entonces</strong> el sistema indica que el equipo está desconectado o sin comunicación.
      </td>
    </tr>
    <tr>
      <td>US43</td>
      <td>Registro de mantenimiento de equipo</td>
      <td>Como QA Manager, quiero registrar las actividades de mantenimiento de los equipos, para garantizar la trazabilidad de su estado operativo.</td>
      <td>
        <strong>Escenario 1: Registro exitoso de mantenimiento</strong><br>
        <strong>Dado que</strong> el QA Manager completa los datos del mantenimiento realizado<br>
        <strong>Cuando</strong> el QA Manager guarda el registro<br>
        <strong>Entonces</strong> el sistema almacena la información y la vincula al historial del equipo.<br><br>
        <strong>Escenario 2: Actualización de fecha de calibración</strong><br>
        <strong>Dado que</strong> el QA Manager registra una calibración del equipo<br>
        <strong>Cuando</strong> el sistema procesa el registro<br>
        <strong>Entonces</strong> el sistema actualiza la fecha de próxima calibración según la periodicidad configurada.
      </td>
    </tr>
    <tr>
      <td>US44</td>
      <td>Historial de mantenimiento de equipo</td>
      <td>Como QA Manager, quiero consultar el historial de mantenimientos de un equipo, para verificar su estado de calibración y conformidad.</td>
      <td>
        <strong>Escenario 1: Consulta exitosa de historial</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona un equipo<br>
        <strong>Cuando</strong> el sistema recupera el historial<br>
        <strong>Entonces</strong> el QA Manager visualiza todos los mantenimientos registrados con sus fechas y detalles.<br><br>
        <strong>Escenario 2: Sin mantenimientos registrados</strong><br>
        <strong>Dado que</strong> el QA Manager consulta el historial de un equipo sin mantenimientos<br>
        <strong>Cuando</strong> el sistema busca los registros<br>
        <strong>Entonces</strong> el sistema indica que no hay mantenimientos registrados para el equipo.
      </td>
    </tr>
    <tr>
      <td>US45</td>
      <td>Alerta de calibración próxima a vencer</td>
      <td>Como QA Manager, quiero recibir alertas de calibración próxima a vencer, para programar el mantenimiento con anticipación y evitar desviaciones.</td>
      <td>
        <strong>Escenario 1: Alerta de calibración próxima</strong><br>
        <strong>Dado que</strong> la fecha de calibración de un equipo está próxima a vencer<br>
        <strong>Cuando</strong> el sistema evalúa el calendario de mantenimientos<br>
        <strong>Entonces</strong> el QA Manager recibe una alerta indicando el equipo y la fecha de vencimiento.<br><br>
        <strong>Escenario 2: Alerta de calibración vencida</strong><br>
        <strong>Dado que</strong> la fecha de calibración de un equipo ha vencido<br>
        <strong>Cuando</strong> el sistema valida el estado de calibración<br>
        <strong>Entonces</strong> el sistema marca el equipo como no conforme y notifica al QA Manager.
      </td>
    </tr>
    <!-- EP04 -->
    <tr>
      <td>EP04</td>
      <td>Sistema de alertas y monitoreo de compliance BPM</td>
      <td>Como Lab Operator o QA Manager, quiero recibir alertas automáticas ante desviaciones de parámetros, para reaccionar de inmediato y garantizar el cumplimiento BPM.</td>
      <td></td>
    </tr>
    <tr>
      <td>US20</td>
      <td>Alerta automática ante desviación de parámetros</td>
      <td>Como Lab Operator, quiero recibir alertas inmediatas cuando una variable salga del rango BPM, para tomar acciones correctivas de inmediato.</td>
      <td>
        <strong>Escenario 1: Alerta de desviación no crítica</strong><br>
        <strong>Dado que</strong> una variable excede el rango BPM configurado en menos del 10%<br>
        <strong>Cuando</strong> el sistema detecta la desviación<br>
        <strong>Entonces</strong> el Lab Operator recibe una alerta visual en menos de 5 segundos indicando la variable afectada y el valor registrado.<br><br>
        <strong>Escenario 2: Alerta de desviación crítica</strong><br>
        <strong>Dado que</strong> una variable excede el rango BPM configurado en más del 10%<br>
        <strong>Cuando</strong> el sistema detecta la desviación<br>
        <strong>Entonces</strong> el sistema genera una alerta de prioridad alta y notifica al Lab Operator en menos de 5 segundos.
      </td>
    </tr>
    <tr>
      <td>US21</td>
      <td>Bloqueo automático de lote por desviación</td>
      <td>Como QA Manager, quiero que el sistema bloquee automáticamente un lote ante una desviación crítica, para evitar que productos no conformes avancen en la cadena de suministro.</td>
      <td>
        <strong>Escenario 1: Bloqueo automático por desviación crítica</strong><br>
        <strong>Dado que</strong> una variable crítica excede el límite BPM permitido en más del 10%<br>
        <strong>Cuando</strong> el sistema evalúa la telemetría del lote<br>
        <strong>Entonces</strong> el sistema cambia automáticamente el estado del lote a “Bloqueado” y registra la causa del bloqueo.br><br>
        <strong>Escenario 2: Notificación de bloqueo</strong><br>
        <strong>Dado que</strong> el sistema bloquea un lote automáticamente<br>
        <strong>Cuando</strong> el bloqueo es ejecutado<br>
        <strong>Entonces</strong> el QA Manager y el Lab Operator reciben una notificación con el identificador del lote, variable afectada y fecha del evento.
      </td>
    </tr>
    <tr>
      <td>US22</td>
      <td>Historial de alertas y eventos de compliance</td>
      <td>Como QA Manager, quiero consultar el historial completo de alertas, para analizar patrones de falla y tomar acciones preventivas.</td>
      <td>
        <strong>Escenario 1: Consulta de historial de alertas</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona un rango de fechas<br>
        <strong>Cuando</strong> el sistema recupera las alertas<br>
        <strong>Entonces</strong> el QA Manager visualiza todas las alertas registradas con su tipo, fecha y equipo asociado.<br><br>
        <strong>Escenario 2: Filtrado de alertas por criticidad</strong><br>
        <strong>Dado que</strong> el QA Manager aplica filtros de criticidad<br>
        <strong>Cuando</strong> el sistema procesa los filtros<br>
        <strong>Entonces</strong> el QA Manager visualiza únicamente las alertas del nivel de criticidad seleccionado.
      </td>
    </tr>
    <tr>
      <td>US23</td>
      <td>Notificación push de alerta crítica</td>
      <td>Como QA Manager, quiero recibir notificaciones push ante alertas críticas, para reaccionar de inmediato aunque no esté utilizando activamente la plataforma.</td>
      <td>
        <strong>Escenario 1: Notificación push enviada</strong><br>
        <strong>Dado que</strong> ocurre una alerta crítica en el sistema<br>
        <strong>Cuando</strong> el QA Manager tiene configuradas notificaciones push<br>
        <strong>Entonces</strong> el QA Manager recibe la notificación en su dispositivo con los detalles de la alerta.<br><br>
        <strong>Escenario 2: Múltiples canales activos</strong><br>
        <strong>Dado que</strong> el QA Manager tiene configurados múltiples canales de notificación<br>
        <strong>Cuando</strong> ocurre una alerta crítica<br>
        <strong>Entonces</strong> el sistema envía la notificación por todos los canales configurados simultáneamente.
      </td>
    </tr>
    <tr>
      <td>US24</td>
      <td>Configuración de canales de notificación</td>
      <td>Como QA Manager, quiero configurar los canales por los que deseo recibir alertas, para adaptar las notificaciones a mis preferencias y disponibilidad.</td>
      <td>
        <strong>Escenario 1: Configuración de canales activos</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona sus canales preferidos de notificación<br>
        <strong>Cuando</strong> el QA Manager guarda la configuración<br>
        <strong>Entonces</strong> el sistema almacena las preferencias y envía alertas solo por los canales activos.<br><br>
        <strong>Escenario 2: Modificación de preferencias</strong><br>
        <strong>Dado que</strong> el QA Manager modifica sus canales de notificación<br>
        <strong>Cuando</strong> el sistema actualiza la configuración<br>
        <strong>Entonces</strong> las nuevas alertas se envían según las preferencias actualizadas de forma inmediata.
      </td>
    </tr>
    <!-- EP05 -->
    <tr>
      <td>EP05</td>
      <td>Gestión y trazabilidad de lotes de producción</td>
      <td>Como QA Manager, quiero gestionar el ciclo completo de los lotes de producción, para garantizar la trazabilidad y el cumplimiento normativo en cada etapa.</td>
      <td></td>
    </tr>
    <tr>
      <td>US14</td>
      <td>Registro de nuevo lote de producción</td>
      <td>Como QA Manager, quiero registrar un nuevo lote de producción, para iniciar su seguimiento digital desde el inicio del proceso.</td>
      <td>
        <strong>Escenario 1: Registro exitoso de lote</strong><br>
        <strong>Dado que</strong> el QA Manager completa todos los datos obligatorios del lote<br>
        <strong>Cuando</strong> el QA Manager confirma el registro<br>
        <strong>Entonces</strong> el sistema crea el lote con estado inicial y genera su identificador único.<br><br>
        <strong>Escenario 2: Validación de datos incompletos</strong><br>
        <strong>Dado que</strong> el QA Manager registra un lote con datos faltantes<br>
        <strong>Cuando</strong> el sistema valida la información<br>
        <strong>Entonces</strong> el sistema indica qué campos obligatorios requieren completarse.<br><br>
        <strong>Escenario 3: Vinculación automática con equipo</strong><br>
        <strong>Dado que</strong> el QA Manager registra un lote asociado a un equipo específico<br>
        <strong>Cuando</strong> el sistema crea el lote<br>
        <strong>Entonces</strong> el sistema vincula automáticamente la telemetría del equipo con el lote.
      </td>
    </tr>
    <tr>
      <td>US15</td>
      <td>Consulta del historial completo de un lote</td>
      <td>Como QA Manager, quiero consultar el historial de un lote, para verificar el cumplimiento BPM del proceso completo.</td>
      <td>
        <strong>Escenario 1: Consulta exitosa de historial</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona un lote registrado<br>
        <strong>Cuando</strong> el sistema recupera la información<br>
        <strong>Entonces</strong> el sistema muestra el estado del lote, fechas de producción, variables registradas, alertas generadas y acciones realizadas por los usuarios.<br><br>
        <strong>Escenario 2: Trazabilidad de materias primas</strong><br>
        <strong>Dado que</strong> el QA Manager consulta el historial de un lote<br>
        <strong>Cuando</strong> el sistema presenta la información<br>
        <strong>Entonces</strong> el sistema muestra las materias primas utilizadas, proveedor asociado y lote de origen de cada insumo.
      </td>
    </tr>
    <tr>
      <td>US18</td>
      <td>Búsqueda y filtrado de lotes</td>
      <td>Como QA Manager, quiero buscar y filtrar lotes por estado, producto o fecha, para localizar rápidamente información específica.</td>
      <td>
        <strong>Escenario 1: Filtrado por estado de lote</strong><br>
        <strong>Dado que</strong> el QA Manager aplica filtros por estado<br>
        <strong>Cuando</strong> el sistema procesa la consulta<br>
        <strong>Entonces</strong> el QA Manager visualiza únicamente los lotes que coinciden con el estado seleccionado.<br><br>
        <strong>Escenario 2: Búsqueda por identificador</strong><br>
        <strong>Dado que</strong> el QA Manager ingresa un identificador de lote<br>
        <strong>Cuando</strong> el sistema busca el lote<br>
        <strong>Entonces</strong> el sistema presenta directamente el lote correspondiente.<br><br>
        <strong>Escenario 3: Combinación de filtros</strong><br>
        <strong>Dado que</strong> el QA Manager aplica múltiples filtros simultáneamente<br>
        <strong>Cuando</strong> el sistema procesa la búsqueda<br>
        <strong>Entonces</strong> el sistema presenta únicamente los lotes que cumplen todos los criterios seleccionados.
      </td>
    </tr>
    <tr>
      <td>US16</td>
      <td>Liberación digital de lote conforme</td>
      <td>Como QA Manager, quiero firmar digitalmente la liberación de un lote conforme, para agilizar la cadena de suministro manteniendo la trazabilidad regulatoria.</td>
      <td>
        <strong>Escenario 1: Liberación exitosa de lote</strong><br>
        <strong>Dado que</strong> el QA Manager verifica que el lote cumple todos los criterios BPM<br>
        <strong>Cuando</strong> el QA Manager firma digitalmente la liberación<br>
        <strong>Entonces</strong> el sistema actualiza el estado del lote a liberado y registra la firma digital con fecha y hora.<br><br>
        <strong>Escenario 2: Impedimento de liberación por desviación pendiente</strong><br>
        <strong>Dado que</strong> el QA Manager libera un lote con desviaciones sin resolver<br>
        <strong>Cuando</strong> el sistema valida el estado del lote<br>
        <strong>Entonces</strong> el sistema impide la liberación e indica las desviaciones pendientes de resolución.
      </td>
    </tr>
    <tr>
      <td>US17</td>
      <td>Rechazo y documentación de lote no conforme</td>
      <td>Como QA Manager, quiero registrar el rechazo de un lote no conforme con justificación, para mantener el registro documental requerido por auditorías.</td>
      <td>
        <strong>Escenario 1: Rechazo exitoso de lote</strong><br>
        <strong>Dado que</strong> el QA Manager identifica que un lote no cumple los criterios BPM<br>
        <strong>Cuando</strong> el QA Manager registra el rechazo con su justificación<br>
        <strong>Entonces</strong> el sistema actualiza el estado del lote a rechazado y almacena la justificación en el historial.<br><br>
        <strong>Escenario 2: Rechazo con registro de acciones correctivas</strong><br>
        <strong>Dado que</strong> el QA Manager rechaza un lote e identifica acciones correctivas<br>
        <strong>Cuando</strong> el QA Manager documenta las acciones<br>
        <strong>Entonces</strong> el sistema vincula las acciones correctivas al registro de rechazo del lote.
      </td>
    </tr>
    <!-- EP06 -->
    <tr>
      <td>EP06</td>
      <td>Gestión de productos y materias primas</td>
      <td>Como QA Manager, quiero gestionar el catálogo de productos y materias primas, para garantizar la trazabilidad completa de los insumos utilizados en producción.</td>
      <td></td>
    </tr>
    <tr>
      <td>US31</td>
      <td>Registro de producto farmacéutico</td>
      <td>Como QA Manager, quiero registrar los productos farmacéuticos con sus especificaciones, para vincularlos a lotes de producción y garantizar su trazabilidad.</td>
      <td>
        <strong>Escenario 1: Registro exitoso de producto</strong><br>
        <strong>Dado que</strong> el QA Manager completa todos los datos del producto<br>
        <strong>Cuando</strong> el QA Manager confirma el registro<br>
        <strong>Entonces</strong> el sistema almacena el producto con sus especificaciones en el catálogo.<br><br>
        <strong>Escenario 2: Producto duplicado</strong><br>
        <strong>Dado que</strong> el QA Manager registra un producto con código existente<br>
        <strong>Cuando</strong> el sistema valida la información<br>
        <strong>Entonces</strong> el sistema indica que el producto ya está registrado en el catálogo.
      </td>
    </tr>
    <tr>
      <td>US32</td>
      <td>Consulta del catálogo de productos</td>
      <td>Como QA Manager, quiero consultar el catálogo de productos registrados, para revisar sus especificaciones y vincularlos a nuevos lotes.</td>
      <td>
        <strong>Escenario 1: Consulta exitosa del catálogo</strong><br>
        <strong>Dado que</strong> el QA Manager accede al catálogo de productos<br>
        <strong>Cuando</strong> el sistema presenta la información<br>
        <strong>Entonces</strong> el QA Manager visualiza todos los productos con sus especificaciones principales.<br><br>
        <strong>Escenario 2: Búsqueda de producto específico</strong><br>
        <strong>Dado que</strong> el QA Manager busca un producto por nombre o código<br>
        <strong>Cuando</strong> el sistema procesa la búsqueda<br>
        <strong>Entonces</strong> el sistema presenta los productos que coinciden con los criterios de búsqueda.
      </td>
    </tr>
    <tr>
      <td>US33</td>
      <td>Registro de materia prima</td>
      <td>Como QA Manager, quiero registrar las materias primas con proveedor y fecha de vencimiento, para garantizar su trazabilidad en los lotes de producción.</td>
      <td>
        <strong>Escenario 1: Registro exitoso de materia prima</strong><br>
        <strong>Dado que</strong> el QA Manager completa los datos obligatorios de la materia prima<br>
        <strong>Cuando</strong> el QA Manager confirma el registro<br>
        <strong>Entonces</strong> el sistema almacena la materia prima con proveedor, lote de origen y fecha de vencimiento.<br><br>
        <strong>Escenario 2: Alerta de vencimiento próximo</strong><br>
        <strong>Dado que</strong> el QA Manager registra una materia prima con fecha de vencimiento cercana<br>
        <strong>Cuando</strong> el sistema valida la fecha<br>
        <strong>Entonces</strong> el sistema genera una alerta indicando el vencimiento próximo.
      </td>
    </tr>
    <tr>
      <td>US34</td>
      <td>Trazabilidad de materia prima en lote</td>
      <td>Como QA Manager, quiero consultar qué materias primas se utilizaron en un lote, para garantizar la trazabilidad completa desde el origen.</td>
      <td>
        <strong>Escenario 1: Consulta exitosa de trazabilidad</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona un lote específico<br>
        <strong>Cuando</strong> el sistema recupera la información de trazabilidad<br>
        <strong>Entonces</strong> el QA Manager visualiza todas las materias primas utilizadas con sus proveedores y lotes de origen.<br><br>
        <strong>Escenario 2: Identificación de lotes afectados por materia prima</strong><br>
        <strong>Dado que</strong> el QA Manager consulta una materia prima específica<br>
        <strong>Cuando</strong> el sistema busca su uso<br>
        <strong>Entonces</strong> el QA Manager visualiza todos los lotes que utilizaron esa materia prima.
      </td>
    </tr>
    <tr>
      <td>US35</td>
      <td>Alerta de stock mínimo de materia prima</td>
      <td>Como QA Manager, quiero recibir alertas de stock mínimo, para gestionar el reabastecimiento a tiempo y evitar interrupciones en producción.</td>
      <td>
        <strong>Escenario 1: Alerta de stock mínimo</strong><br>
        <strong>Dado que</strong> el stock de una materia prima alcanza el nivel mínimo configurado<br>
        <strong>Cuando</strong> el sistema evalúa el inventario<br>
        <strong>Entonces</strong> el QA Manager recibe una alerta indicando la materia prima y el nivel actual de stock.<br><br>
        <strong>Escenario 2: Alerta de stock crítico</strong><br>
        <strong>Dado que</strong> el stock de una materia prima alcanza nivel crítico<br>
        <strong>Cuando</strong> el sistema evalúa el inventario<br>
        <strong>Entonces</strong> el QA Manager recibe una alerta de alta prioridad indicando la urgencia del reabastecimiento.
      </td>
    </tr>
    <!-- EP07 -->
    <tr>
      <td>EP07</td>
      <td>Reportes y auditoría de compliance</td>
      <td>Como QA Manager o auditor, quiero generar reportes inmutables de cumplimiento, para preparar documentación de auditorías regulatorias y verificar la integridad de datos.</td>
      <td></td>
    </tr>
    <tr>
      <td>US25</td>
      <td>Generación de reporte de trazabilidad de lote</td>
      <td>Como QA Manager, quiero generar un reporte PDF inmutable del historial de un lote, para presentarlo en auditorías regulatorias.</td>
      <td>
        <strong>Escenario 1: Generación exitosa de reporte</strong><br>
        <strong>Dado que</strong> el QA Manager solicita el reporte de un lote existente<br>
        <strong>Cuando</strong> el sistema genera el documento<br>
        <strong>Entonces</strong> el sistema descarga un archivo PDF que contiene historial del lote, alertas, variables registradas y responsables asociados.<br><br>
        <strong>Escenario 2: Reporte con firma digital</strong><br>
        <strong>Dado que</strong> el QA Manager solicita el reporte de trazabilidad<br>
        <strong>Cuando</strong> el sistema genera el PDF<br>
        <strong>Entonces</strong> eel documento incluye firma digital y marca de tiempo para validar su integridad.
      </td>
    </tr>
    <tr>
      <td>US26</td>
      <td>Generación de reporte consolidado de cumplimiento BPM</td>
      <td>Como QA Manager, quiero un reporte consolidado de cumplimiento BPM por periodo, para preparar documentación de auditoría con indicadores agregados.</td>
      <td>
        <strong>Escenario 1: Generación de reporte periódico</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona un rango de fechas<br>
        <strong>Cuando</strong> el sistema genera el reporte<br>
        <strong>Entonces</strong> el QA Manager descarga el reporte consolidado con todos los lotes, alertas y desviaciones del periodo.<br><br>
        <strong>Escenario 2: Desglose por producto</strong><br>
        <strong>Dado que</strong> el QA Manager solicita un reporte consolidado<br>
        <strong>Cuando</strong> el sistema presenta los datos<br>
        <strong>Entonces</strong> el reporte incluye desglose de cumplimiento por cada producto farmacéutico.
      </td>
    </tr>
    <tr>
      <td>US27</td>
      <td>Exportación de log de eventos inmutable</td>
      <td>Como auditor, quiero exportar el log de eventos en formato no editable, para verificar la integridad de datos durante auditorías externas.</td>
      <td>
        <strong>Escenario 1: Exportación exitosa de log</strong><br>
        <strong>Dado que</strong> el auditor solicita el log de eventos de un periodo<br>
        <strong>Cuando</strong> el sistema genera la exportación<br>
        <strong>Entonces</strong> el auditor descarga el log completo en formato PDF con firma digital.<br><br>
        <strong>Escenario 2: Log con hash de verificación</strong><br>
        <strong>Dado que</strong> el auditor exporta el log de eventos<br>
        <strong>Cuando</strong> el sistema crea el documento<br>
        <strong>Entonces</strong> el documento incluye hash criptográfico para verificar su integridad.
      </td>
    </tr>
    <!-- EP08 -->
    <tr>
      <td>EP08</td>
      <td>Analytics y KPIs de calidad</td>
      <td>Como QA Manager, quiero analizar indicadores clave de calidad, para evaluar el desempeño del área basado en datos y priorizar acciones de mejora.</td>
      <td></td>
    </tr>
    <tr>
      <td>US36</td>
      <td>Dashboard de indicadores de calidad (KPIs)</td>
      <td>Como QA Manager, quiero un panel de KPIs, para evaluar el desempeño del área de calidad basado en datos objetivos.</td>
      <td>
        <strong>Escenario 1: Visualización de KPIs principales</strong><br>
        <strong>Dado que</strong> el QA Manager accede al dashboard de KPIs<br>
        <strong>Cuando</strong> el sistema presenta los indicadores<br>
        <strong>Entonces</strong> el QA Manager visualiza métricas como tasa de conformidad, tiempo promedio de liberación y cantidad de desviaciones.<br><br>
        <strong>Escenario 2: Comparación con periodos anteriores</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona un periodo de comparación<br>
        <strong>Cuando</strong> el sistema procesa los datos<br>
        <strong>Entonces</strong> el QA Manager visualiza la evolución de los KPIs respecto a periodos anteriores.
      </td>
    </tr>
    <tr>
      <td>US37</td>
      <td>Reporte de tendencias de desviaciones</td>
      <td>Como QA Manager, quiero visualizar tendencias de desviaciones por equipo y variable, para priorizar acciones correctivas basadas en patrones identificados.</td>
      <td>
        <strong>Escenario 1: Análisis de tendencias por equipo</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona un equipo específico<br>
        <strong>Cuando</strong> el sistema analiza el historial de desviaciones<br>
        <strong>Entonces</strong> el QA Manager visualiza las tendencias de desviación por variable.<br><br>
        <strong>Escenario 2: Identificación de variables críticas</strong><br>
        <strong>Dado que</strong> el QA Manager analiza las tendencias de desviaciones<br>
        <strong>Cuando</strong> el sistema procesa los datos<br>
        <strong>Entonces</strong> el sistema resalta las variables con mayor frecuencia de desviación para priorizar acciones.
      </td>
    </tr>
    <!-- EP09 -->
    <tr>
      <td>EP09</td>
      <td>Configuración y seguridad institucional</td>
      <td>Como QA Manager, quiero gestionar la configuración institucional y las políticas de seguridad, para mantener la información actualizada y protegida.</td>
      <td></td>
    </tr>
    <tr>
      <td>US38</td>
      <td>Gestión de información del laboratorio</td>
      <td>Como QA Manager, quiero actualizar los datos institucionales de mi laboratorio, para mantener la información vigente en la plataforma.</td>
      <td>
        <strong>Escenario 1: Actualización exitosa de información</strong><br>
        <strong>Dado que</strong> el QA Manager modifica los datos institucionales<br>
        <strong>Cuando</strong> el QA Manager guarda los cambios<br>
        <strong>Entonces</strong> el sistema actualiza la información y registra la modificación en el log de auditoría.<br><br>
        <strong>Escenario 2: Validación de campos obligatorios</strong><br>
        <strong>Dado que</strong> el QA Manager guarda cambios con campos obligatorios vacíos<br>
        <strong>Cuando</strong> el sistema valida la información<br>
        <strong>Entonces</strong> el sistema indica qué campos requieren completarse antes de guardar.
      </td>
    </tr>
    <tr>
      <td>US39</td>
      <td>Configuración de normativas aplicables</td>
      <td>Como QA Manager, quiero configurar las normativas regulatorias bajo las cuales opera mi laboratorio, para que el sistema valide el cumplimiento según los estándares correspondientes.</td>
      <td>
        <strong>Escenario 1: Configuración de normativas</strong><br>
        <strong>Dado que</strong> el QA Manager selecciona las normativas aplicables<br>
        <strong>Cuando</strong> el QA Manager guarda la configuración<br>
        <strong>Entonces</strong> el sistema aplica los requisitos de las normativas seleccionadas en las validaciones.<br><br>
        <strong>Escenario 2: Actualización de normativas</strong><br>
        <strong>Dado que</strong> el QA Manager modifica las normativas configuradas<br>
        <strong>Cuando</strong> el sistema procesa el cambio<br>
        <strong>Entonces</strong> el sistema ajusta los criterios de validación según las nuevas normativas de forma inmediata.
      </td>
    </tr>
    <tr>
      <td>US41</td>
      <td>Cifrado de datos sensibles</td>
      <td>Como QA Manager, quiero que la información sensible esté cifrada en almacenamiento y tránsito, para protegerla de accesos no autorizados.</td>
      <td>
        <strong>Regla de negocio: Cifrado de almacenamiento</strong><br>
        Toda información sensible almacenada en la plataforma debe utilizar cifrado AES-256.<br><br>
        <strong>Regla de negocio: Cifrado en tránsito</strong><br>
       Toda transmisión de datos entre cliente y servidor debe realizarse mediante protocolo HTTPS con TLS 1.2 o superior.<br><br>
        <strong>Regla de negocio: Clasificación de datos</strong><br>
      El sistema debe clasificar automáticamente la información sensible y aplicar el nivel de cifrado correspondiente según el tipo de dato.
      </td>
    </tr>
    <tr>
      <td>US42</td>
      <td>Log de auditoría de accesos y acciones</td>
      <td>Como QA Manager, quiero que la plataforma registre un log de todos los accesos e interacciones, para garantizar la trazabilidad de acciones realizadas en el sistema.</td>
      <td>
        <strong>Regla de negocio: Registro de acciones</strong><br>
       El sistema debe registrar cada acceso, modificación y eliminación de información indicando fecha, hora, usuario y acción realizada.<br><br>
        <strong>Regla de negocio: Inmutabilidad de logs</strong><br>
      Los registros de auditoría no pueden ser modificados ni eliminados por usuarios del sistema.<br><br>
        <strong>Regla de negocio: Retención de logs</strong><br>
      Los logs de auditoría deben conservarse por un periodo mínimo de 5 años.
      </td>
    </tr>
    <!-- Technical Stories -->
    <tr>
      <td>EP10</td>
      <td>Technical Stories - Backend API</td>
      <td>Como Developer, quiero contar con los endpoints del RESTful API, para que la aplicación web y móvil consuman los servicios de QualiTrack de manera eficiente y segura.</td>
      <td></td>
    </tr>
    <tr>
      <td>TS-IOT01</td>
      <td>Ingesta de telemetría desde sensores IoT</td>
      <td>Como Developer, quiero gestionar la recepción y almacenamiento de telemetría desde sensores IoT, para que el sistema procese las mediciones en tiempo real.</td>
      <td>
        <strong>Escenario 1: Ingesta exitosa de telemetría</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición POST con datos de telemetría válidos<br>
        <strong>Cuando</strong> el endpoint procesa la solicitud<br>
        <strong>Entonces</strong> el sistema responde con código 201 y almacena las mediciones con timestamp.<br><br>
        <strong>Escenario 2: Validación de formato de telemetría</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición POST con datos de telemetría en formato inválido<br>
        <strong>Cuando</strong> el endpoint valida la estructura<br>
        <strong>Entonces</strong> el sistema responde con código 400 indicando los campos con formato incorrecto.<br><br>
        <strong>Escenario 3: Autenticación de sensor</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición POST sin token de autenticación válido<br>
        <strong>Cuando</strong> el endpoint valida las credenciales<br>
        <strong>Entonces</strong> el sistema responde con código 401 rechazando la ingesta de telemetría.
      </td>
    </tr>
    <tr>
      <td>TS-IOT02</td>
      <td>Evaluación de compliance BPM en tiempo real</td>
      <td>Como Developer, quiero la evaluación automática de mediciones contra parámetros BPM, para que el sistema detecte desviaciones de forma inmediata.</td>
      <td>
        <strong>Escenario 1: Evaluación de medición conforme</strong><br>
        <strong>Dado que</strong> el sistema procesa una medición dentro de los rangos BPM<br>
        <strong>Cuando</strong> el servicio evalúa los valores<br>
        <strong>Entonces</strong> el sistema registra la medición como conforme sin generar alertas.<br><br>
        <strong>Escenario 2: Detección de desviación no crítica</strong><br>
        <strong>Dado que</strong> el sistema procesa una medición fuera de rangos BPM pero dentro de límites aceptables<br>
        <strong>Cuando</strong> el servicio evalúa los valores<br>
        <strong>Entonces</strong> el sistema registra la desviación y genera una alerta de nivel medio.<br><br>
        <strong>Escenario 3: Detección de desviación crítica</strong><br>
        <strong>Dado que</strong> el sistema procesa una medición que excede límites críticos BPM<br>
        <strong>Cuando</strong> el servicio evalúa los valores<br>
        <strong>Entonces</strong> el sistema registra la desviación crítica, genera alerta de alta prioridad y activa el bloqueo automático del lote.
      </td>
    </tr>
    <tr>
      <td>TS-EQ001</td>
      <td>Registro de equipos industriales</td>
      <td>Como Developer, quiero el registro de equipos industriales con sus parámetros BPM, para que el sistema valide la telemetría de cada equipo.</td>
      <td>
        <strong>Escenario 1: Registro exitoso de equipo</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición POST con datos completos del equipo y parámetros BPM<br>
        <strong>Cuando</strong> el endpoint procesa la solicitud<br>
        <strong>Entonces</strong> el sistema responde con código 201 y retorna el identificador único del equipo registrado.<br><br>
        <strong>Escenario 2: Validación de campos obligatorios</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición POST con datos incompletos del equipo<br>
        <strong>Cuando</strong> el endpoint valida la información<br>
        <strong>Entonces</strong> el sistema responde con código 400 indicando los campos obligatorios faltantes.<br><br>
        <strong>Escenario 3: Equipo duplicado</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición POST con un identificador de equipo ya registrado<br>
        <strong>Cuando</strong> el endpoint valida la unicidad<br>
        <strong>Entonces</strong> el sistema responde con código 409 indicando que el equipo ya existe.
      </td>
    </tr>
    <tr>
      <td>TS-EQ002</td>
      <td>Listado de equipos del laboratorio</td>
      <td>Como Developer, quiero la consulta de equipos con su estado de conexión, para que la aplicación muestre el estado operativo de cada equipo.</td>
      <td>
        <strong>Escenario 1: Listado exitoso de equipos</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición GET para listar equipos de un laboratorio<br>
        <strong>Cuando</strong> el endpoint procesa la solicitud<br>
        <strong>Entonces</strong> el sistema responde con código 200 y retorna la lista de equipos con su estado de conexión y última telemetría.<br><br>
        <strong>Escenario 2: Filtrado por estado de conexión</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición GET con parámetro de filtro por estado<br>
        <strong>Cuando</strong> el endpoint aplica el filtro<br>
        <strong>Entonces</strong> el sistema responde con código 200 y retorna únicamente los equipos que coinciden con el estado solicitado.
      </td>
    </tr>
    <tr>
      <td>TS-LOT001</td>
      <td>Creación de lotes de producción</td>
      <td>Como Developer, quiero la creación de lotes con validaciones obligatorias, para que cada lote tenga la información mínima requerida para trazabilidad.</td>
      <td>
        <strong>Escenario 1: Creación exitosa de lote</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición POST con todos los datos obligatorios del lote<br>
        <strong>Cuando</strong> el endpoint procesa la solicitud<br>
        <strong>Entonces</strong> el sistema responde con código 201 y retorna el identificador único del lote creado.<br><br>
        <strong>Escenario 2: Validación de producto asociado</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición POST con un identificador de producto inexistente<br>
        <strong>Cuando</strong> el endpoint valida las relaciones<br>
        <strong>Entonces</strong> el sistema responde con código 400 indicando que el producto especificado no existe.<br><br>
        <strong>Escenario 3: Vinculación automática con equipo</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición POST con identificador de equipo válido<br>
        <strong>Cuando</strong> el endpoint crea el lote<br>
        <strong>Entonces</strong> el sistema establece la vinculación entre el lote y el equipo para recepción automática de telemetría.
      </td>
    </tr>
    <tr>
      <td>TS-LOT002</td>
      <td>Obtención de detalle de lote</td>
      <td>Como Developer, quiero la consulta del detalle completo de un lote con su historial, para que la aplicación presente toda la información de trazabilidad.</td>
      <td>
        <strong>Escenario 1: Consulta exitosa de lote</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición GET con un identificador de lote válido<br>
        <strong>Cuando</strong> el endpoint recupera la información<br>
        <strong>Entonces</strong> el sistema responde con código 200 y retorna el lote con todas sus etapas, telemetría, alertas y materias primas utilizadas.<br><br>
        <strong>Escenario 2: Lote inexistente</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición GET con un identificador de lote que no existe<br>
        <strong>Cuando</strong> el endpoint busca el lote<br>
        <strong>Entonces</strong> el sistema responde con código 404 indicando que el lote no fue encontrado.
      </td>
    </tr>
    <tr>
      <td>TS-LOT003</td>
      <td>Actualización de estado de lote</td>
      <td>Como Developer, quiero la actualización de estado de lotes con registro del responsable, para que cada cambio de estado quede trazado en el historial.</td>
      <td>
        <strong>Escenario 1: Actualización exitosa de estado</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición PATCH con nuevo estado y responsable<br>
        <strong>Cuando</strong> el endpoint procesa la actualización<br>
        <strong>Entonces</strong> el sistema responde con código 200, actualiza el estado del lote y registra el cambio con timestamp y usuario responsable.<br><br>
        <strong>Escenario 2: Transición de estado inválida</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición PATCH con una transición de estado no permitida<br>
        <strong>Cuando</strong> el endpoint valida la transición<br>
        <strong>Entonces</strong> el sistema responde con código 400 indicando que la transición no está permitida según las reglas de negocio.<br><br>
        <strong>Escenario 3: Liberación con desviaciones pendientes</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición PATCH para liberar un lote con desviaciones sin resolver<br>
        <strong>Cuando</strong> el endpoint valida las condiciones<br>
        <strong>Entonces</strong> el sistema responde con código 400 indicando las desviaciones que impiden la liberación.
      </td>
    </tr>
    <tr>
      <td>TS-REP001</td>
      <td>Generación de reporte PDF de lote</td>
      <td>Como Developer, quiero la generación de reportes PDF inmutables con historial de lotes, para que la aplicación provea documentación para auditorías.</td>
      <td>
        <strong>Escenario 1: Generación exitosa de reporte</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición GET para generar reporte de un lote específico<br>
        <strong>Cuando</strong> el endpoint procesa la solicitud<br>
        <strong>Entonces</strong> el sistema responde con código 200 y retorna el documento PDF con toda la trazabilidad del lote incluyendo firma digital.<br><br>
        <strong>Escenario 2: Lote sin datos suficientes</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición GET para un lote sin información completa<br>
        <strong>Cuando</strong> el endpoint valida los datos disponibles<br>
        <strong>Entonces</strong> el sistema responde con código 400 indicando que el lote no tiene información suficiente para generar el reporte.
      </td>
    </tr>
    <tr>
      <td>TS-REP002</td>
      <td>Exportación de log de eventos de equipo</td>
      <td>Como Developer, quiero la exportación de logs de eventos en formato PDF, para que auditores puedan verificar la integridad de datos.</td>
      <td>
        <strong>Escenario 1: Exportación exitosa de log</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición GET con rango de fechas y equipo específico<br>
        <strong>Cuando</strong> el endpoint procesa la exportación<br>
        <strong>Entonces</strong> el sistema responde con código 200 y retorna el documento PDF con el log completo incluyendo hash de verificación.<br><br>
        <strong>Escenario 2: Rango de fechas inválido</strong><br>
        <strong>Dado que</strong> el sistema recibe una petición GET con fecha inicial posterior a fecha final<br>
        <strong>Cuando</strong> el endpoint valida los parámetros<br>
        <strong>Entonces</strong> el sistema responde con código 400 indicando que el rango de fechas es inválido.
      </td>
    </tr>
  </tbody>
</table>


<div style="page-break-after: always;"></div>

## 3.2. Impact Mapping

<p>
En el Impact Mapping de QualiTrack, el equipo elaboró el mapa partiendo de un Business Goal principal que cumple los criterios SMART: "Reducir en un 80% el tiempo de preparación para auditorías regulatorias de DIGEMID y disminuir en un 15% la pérdida de lotes por desviaciones no detectadas, logrando la suscripción de al menos 2 laboratorios piloto en los primeros 8 meses de operación".
</p>

<p>
A partir de esta meta se incorporaron como Actors/Personas a los User Personas previamente definidos: el Jefe de Aseguramiento de la Calidad (QA) y el Operario de planta. Para cada uno se identificaron los Impacts esperados: en el caso del Jefe de QA, la reducción del tiempo dedicado a preparar documentación para auditorías, la liberación de lotes de forma digital en menos de 10 minutos y la detección anticipada de desviaciones normativas; en el caso del Operario, la eliminación de las bitácoras físicas y la recepción de alertas de desviación en menos de 5 segundos.
</p>

<p>
A partir de estos impactos se definieron los Deliverables que QualiTrack debe ofrecer: el dashboard de telemetría en tiempo real con indicadores de cumplimiento BPM, el módulo de gestión de lotes con historial inmutable, el motor de alertas automáticas y bloqueo de lotes no conformes, la generación de reportes PDF de trazabilidad listos para inspección, y la integración IoT para la captura automática de variables críticas. Finalmente, en la columna de User Stories se detallaron historias que permiten trazar la ruta desde los objetivos de negocio hasta los features concretos del producto, asegurando la alineación entre Business Goals, Impacts, Deliverables y desarrollo de la solución.
</p>

<img src="../assets/img/Impact-Map.png" alt="Impact Map QualiTrack" style="width: 90%; height: auto;">

<div style="page-break-after: always;"></div>

## 3.3. Product Backlog

En esta sección se presenta el Product Backlog priorizado con las Historias de Usuario y Technical Stories estimadas en Story Points. El orden ha sido determinado por el valor que aportan al negocio, priorizando las funcionalidades core de compliance y trazabilidad que son el diferenciador clave de QualiTrack.

<table>
  <tr>
    <td><strong>#</strong></td>
    <td><strong>Story ID</strong></td>
    <td><strong>Título</strong></td>
    <td><strong>Descripción</strong></td>
    <td><strong>Story Points (1/2/3)</strong></td>
  </tr>
  <tr><td>1</td><td>US01</td><td>Menú de navegación</td><td>Como visitante, quiero explorar las secciones principales del sitio, para informarme sobre las características, planes y contacto de QualiTrack.</td><td>1</td></tr>
  <tr><td>2</td><td>US02</td><td>Visualización de planes de suscripción</td><td>Como visitante del segmento QA Manager, quiero comparar los planes disponibles, para elegir el que mejor se adapte a mi organización.</td><td>2</td></tr>
  <tr><td>3</td><td>US03</td><td>Visualización del equipo creador</td><td>Como visitante, quiero conocer al equipo detrás de QualiTrack, para generar confianza antes de contratar.</td><td>1</td></tr>
  <tr><td>4</td><td>US04</td><td>Formulario de contacto</td><td>Como visitante, quiero enviar consultas al equipo de QualiTrack, para obtener información adicional sobre el servicio.</td><td>2</td></tr>
  <tr><td>5</td><td>US05</td><td>Cambio de idioma</td><td>Como visitante, quiero cambiar el idioma del sitio entre español e inglés, para comprender mejor la propuesta de valor.</td><td>2</td></tr>
  <tr><td>6</td><td>US06</td><td>Registro de laboratorio en la plataforma</td><td>Como QA Manager, quiero registrar mi laboratorio en QualiTrack, para comenzar a gestionar los procesos de calidad digitalmente.</td><td>3</td></tr>
  <tr><td>7</td><td>US07</td><td>Inicio de sesión seguro</td><td>Como usuario registrado, quiero iniciar sesión con mis credenciales, para acceder a las funcionalidades según mi rol asignado.</td><td>2</td></tr>
  <tr><td>8</td><td>US08</td><td>Recuperación de contraseña</td><td>Como usuario registrado, quiero recuperar mi contraseña olvidada, para no perder acceso a la plataforma.</td><td>2</td></tr>
  <tr><td>9</td><td>US09</td><td>Gestión de roles y permisos</td><td>Como QA Manager, quiero gestionar los roles de mi equipo, para garantizar accesos según responsabilidades.</td><td>3</td></tr>
  <tr><td>10</td><td>US12</td><td>Vinculación de equipos IoT</td><td>Como QA Manager, quiero registrar y vincular los equipos industriales, para que la plataforma reciba su telemetría automáticamente.</td><td>3</td></tr>
  <tr><td>11</td><td>US19</td><td>Configuración de parámetros BPM por equipo</td><td>Como QA Manager, quiero configurar los rangos permitidos de variables, para que el sistema detecte desviaciones automáticamente.</td><td>3</td></tr>
  <tr><td>12</td><td>US10</td><td>Visualización del dashboard de telemetría</td><td>Como QA Manager, quiero un dashboard en tiempo real de las variables críticas, para supervisar el cumplimiento BPM.</td><td>3</td></tr>
  <tr><td>13</td><td>US11</td><td>Visualización del historial de telemetría</td><td>Como QA Manager, quiero consultar el historial de variables de un equipo, para analizar el comportamiento del proceso.</td><td>3</td></tr>
  <tr><td>14</td><td>US13</td><td>Consulta del estado de equipos en tiempo real</td><td>Como Lab Operator, quiero verificar el estado de conexión de los equipos, para confirmar que están operativos antes de producción.</td><td>2</td></tr>
  <tr><td>15</td><td>US20</td><td>Alerta automática ante desviación de parámetros</td><td>Como Lab Operator, quiero recibir alertas inmediatas cuando una variable salga del rango BPM, para tomar acciones correctivas.</td><td>3</td></tr>
  <tr><td>16</td><td>US21</td><td>Bloqueo automático de lote por desviación</td><td>Como QA Manager, quiero que el sistema bloquee automáticamente un lote ante una desviación crítica.</td><td>3</td></tr>
  <tr><td>17</td><td>US22</td><td>Historial de alertas y eventos de compliance</td><td>Como QA Manager, quiero consultar el historial completo de alertas, para analizar patrones de falla.</td><td>3</td></tr>
  <tr><td>18</td><td>US23</td><td>Notificación push de alerta crítica</td><td>Como QA Manager, quiero recibir notificaciones push ante alertas críticas, para reaccionar aunque no esté en la plataforma.</td><td>3</td></tr>
  <tr><td>19</td><td>US24</td><td>Configuración de canales de notificación</td><td>Como QA Manager, quiero configurar los canales por los que deseo recibir alertas, para adaptar las notificaciones a mis preferencias.</td><td>2</td></tr>
  <tr><td>20</td><td>US14</td><td>Registro de nuevo lote de producción</td><td>Como QA Manager, quiero registrar un nuevo lote de producción, para iniciar su seguimiento digital.</td><td>3</td></tr>
  <tr><td>21</td><td>US15</td><td>Consulta del historial completo de un lote</td><td>Como QA Manager, quiero consultar el historial de un lote, para verificar el cumplimiento BPM del proceso.</td><td>3</td></tr>
  <tr><td>22</td><td>US18</td><td>Búsqueda y filtrado de lotes</td><td>Como QA Manager, quiero buscar y filtrar lotes por estado, producto o fecha, para localizar rápidamente información específica.</td><td>2</td></tr>
  <tr><td>23</td><td>US16</td><td>Liberación digital de lote conforme</td><td>Como QA Manager, quiero firmar digitalmente la liberación de un lote conforme, para agilizar la cadena de suministro.</td><td>3</td></tr>
  <tr><td>24</td><td>US17</td><td>Rechazo y documentación de lote no conforme</td><td>Como QA Manager, quiero registrar el rechazo de un lote no conforme con justificación, para mantener el registro documental.</td><td>3</td></tr>
  <tr><td>25</td><td>US25</td><td>Generación de reporte de trazabilidad de lote</td><td>Como QA Manager, quiero generar un reporte PDF inmutable del historial de un lote, para auditorías regulatorias.</td><td>3</td></tr>
  <tr><td>26</td><td>US26</td><td>Generación de reporte consolidado de cumplimiento BPM</td><td>Como QA Manager, quiero un reporte consolidado de cumplimiento BPM por periodo, para preparar documentación de auditoría.</td><td>3</td></tr>
  <tr><td>27</td><td>US27</td><td>Exportación de log de eventos inmutable</td><td>Como auditor, quiero exportar el log de eventos en formato no editable, para verificar la integridad de datos.</td><td>3</td></tr>
  <tr><td>28</td><td>US28</td><td>Registro de operario o supervisor</td><td>Como QA Manager, quiero registrar a los miembros del equipo técnico, para que puedan acceder a la plataforma.</td><td>3</td></tr>
  <tr><td>29</td><td>US29</td><td>Baja de personal del laboratorio</td><td>Como QA Manager, quiero desactivar el acceso de personal que ya no forma parte del laboratorio.</td><td>3</td></tr>
  <tr><td>30</td><td>US30</td><td>Consulta de actividad de personal por turno</td><td>Como QA Manager, quiero consultar el registro de actividad de cada operario por turno, para verificar responsabilidades.</td><td>2</td></tr>
  <tr><td>31</td><td>US31</td><td>Registro de producto farmacéutico</td><td>Como QA Manager, quiero registrar los productos farmacéuticos con sus especificaciones, para vincularlos a lotes de producción.</td><td>3</td></tr>
  <tr><td>32</td><td>US32</td><td>Consulta del catálogo de productos</td><td>Como QA Manager, quiero consultar el catálogo de productos registrados, para revisar sus especificaciones.</td><td>2</td></tr>
  <tr><td>33</td><td>US33</td><td>Registro de materia prima</td><td>Como QA Manager, quiero registrar las materias primas con proveedor y fecha de vencimiento, para garantizar su trazabilidad.</td><td>3</td></tr>
  <tr><td>34</td><td>US34</td><td>Trazabilidad de materia prima en lote</td><td>Como QA Manager, quiero consultar qué materias primas se utilizaron en un lote, para garantizar la trazabilidad completa.</td><td>3</td></tr>
  <tr><td>35</td><td>US35</td><td>Alerta de stock mínimo de materia prima</td><td>Como QA Manager, quiero recibir alertas de stock mínimo, para gestionar el reabastecimiento a tiempo.</td><td>3</td></tr>
  <tr><td>36</td><td>US36</td><td>Dashboard de indicadores de calidad (KPIs)</td><td>Como QA Manager, quiero un panel de KPIs, para evaluar el desempeño del área de calidad basado en datos.</td><td>3</td></tr>
  <tr><td>37</td><td>US37</td><td>Reporte de tendencias de desviaciones</td><td>Como QA Manager, quiero visualizar tendencias de desviaciones por equipo y variable, para priorizar acciones correctivas.</td><td>3</td></tr>
  <tr><td>38</td><td>US38</td><td>Gestión de información del laboratorio</td><td>Como QA Manager, quiero actualizar los datos institucionales de mi laboratorio, para mantener la información vigente.</td><td>2</td></tr>
  <tr><td>39</td><td>US39</td><td>Configuración de normativas aplicables</td><td>Como QA Manager, quiero configurar las normativas regulatorias bajo las cuales opera mi laboratorio.</td><td>2</td></tr>
  <tr><td>40</td><td>US40</td><td>Términos y condiciones de uso</td><td>Como visitante, quiero acceder a los términos y condiciones de QualiTrack, para conocer las políticas antes de contratar.</td><td>1</td></tr>
  <tr><td>41</td><td>US41</td><td>Cifrado de datos sensibles</td><td>Como QA Manager, quiero que la información sensible esté cifrada, para protegerla de accesos no autorizados.</td><td>3</td></tr>
  <tr><td>42</td><td>US42</td><td>Log de auditoría de accesos y acciones</td><td>Como QA Manager, quiero que la plataforma registre un log de todos los accesos, para garantizar la trazabilidad de acciones.</td><td>3</td></tr>
  <tr><td>43</td><td>US43</td><td>Registro de mantenimiento de equipo</td><td>Como QA Manager, quiero registrar las actividades de mantenimiento de los equipos, para garantizar la trazabilidad de su estado operativo.</td><td>3</td></tr>
  <tr><td>44</td><td>US44</td><td>Historial de mantenimiento de equipo</td><td>Como QA Manager, quiero consultar el historial de mantenimientos de un equipo, para verificar su estado de calibración.</td><td>2</td></tr>
  <tr><td>45</td><td>US45</td><td>Alerta de calibración próxima a vencer</td><td>Como QA Manager, quiero recibir alertas de calibración próxima a vencer, para programar el mantenimiento con anticipación.</td><td>3</td></tr>
  <tr><td>46</td><td>TS-IOT01</td><td>Ingesta de telemetría desde sensores IoT</td><td>Como Developer, quiero gestionar la recepción de telemetría desde sensores IoT, para procesar las mediciones en tiempo real.</td><td>3</td></tr>
  <tr><td>47</td><td>TS-IOT02</td><td>Evaluación de compliance BPM en tiempo real</td><td>Como Developer, quiero la evaluación automática de mediciones contra parámetros BPM.</td><td>3</td></tr>
  <tr><td>48</td><td>TS-EQ001</td><td>Registro de equipos industriales</td><td>Como Developer, quiero el registro de equipos industriales con sus parámetros BPM.</td><td>3</td></tr>
  <tr><td>49</td><td>TS-EQ002</td><td>Listado de equipos del laboratorio</td><td>Como Developer, quiero la consulta de equipos con su estado de conexión.</td><td>2</td></tr>
  <tr><td>50</td><td>TS-LOT001</td><td>Creación de lotes de producción</td><td>Como Developer, quiero la creación de lotes con validaciones obligatorias.</td><td>3</td></tr>
  <tr><td>51</td><td>TS-LOT002</td><td>Obtención de detalle de lote</td><td>Como Developer, quiero la consulta del detalle completo de un lote con su historial.</td><td>3</td></tr>
  <tr><td>52</td><td>TS-LOT003</td><td>Actualización de estado de lote</td><td>Como Developer, quiero la actualización de estado de lotes con registro del responsable.</td><td>3</td></tr>
  <tr><td>53</td><td>TS-REP001</td><td>Generación de reporte PDF de lote</td><td>Como Developer, quiero la generación de reportes PDF inmutables con historial de lotes.</td><td>3</td></tr>
  <tr><td>54</td><td>TS-REP002</td><td>Exportación de log de eventos de equipo</td><td>Como Developer, quiero la exportación de logs de eventos en formato PDF.</td><td>3</td></tr>
</table>

<div align="center">
  <img src="../assets/img/Backlog-ClosedSource.jpeg" alt="Evidence Product Backlog" width="90%">
  <p><em>Figura: Captura del Product Backlog en la herramienta de gestión del proyecto.</em></p>
</div>
