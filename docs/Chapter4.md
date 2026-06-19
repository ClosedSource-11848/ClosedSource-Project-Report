# Capítulo IV: Product Design

En este capítulo se detallan las decisiones de diseño de producto para la plataforma QualiTrack y su respectiva Landing Page. Se establecen las guías de estilo visuales, la arquitectura de la información y los criterios que aseguran una experiencia de usuario (UX) intuitiva y profesional, alineada a las exigencias de la industria farmacéutica y entidades regulatorias como la DIGEMID.

## 4.1. Style Guidelines

### 4.1.1. General Style Guidelines

El diseño visual de la plataforma **QualiTrack** se rige por una estética limpia, tecnológica y de alta precisión, reflejando el compromiso de **ClosedSource** con la integridad de datos en la manufactura farmacéutica. El objetivo es proyectar un entorno de confianza y profesionalismo que minimice la carga cognitiva del usuario al monitorear variables críticas.

En este capítulo, detallaremos cada uno de los elementos visuales y de estilo que guían el desarrollo de la aplicación QualiTrack, siempre siguiendo los principios de Diseño de Experiencia de Usuario (UX) e Interfaz de Usuario (UI) para garantizar la máxima usabilidad y accesibilidad.

**Branding**

El logotipo principal de QualiTrack está compuesto por un isotipo que integra múltiples elementos semánticos de nuestro dominio técnico: El Escudo y la Cerradura representan la seguridad inquebrantable, la inmutabilidad de los registros y el cumplimiento regulatorio frente a DIGEMID. El check central Simboliza la aprobación de calidad (BPM) y la liberación de lotes de producción. Los Nodos de Circuitos evocan la automatización industrial y la conexión directa a los equipos mediante telemetría IoT. Y finalmente la tipografía del logo el nombre divide sus conceptos utilizando el azul tecnológico para la calidad y el verde de cumplimiento para la trazabilidad.

<br>
<p align="center">
  <img src="../assets/img/QualiTrack.png" alt="QualiTrack Logo" width="350px" height="auto"/>
</p>
<br>

**Typography**

La tipografía empleada en QualiTrack será **Rubik**, con sus variantes Light, Regular, Medium, SemiBold, Bold y ExtraBold. La elección de Rubik se basa en su estética moderna y profesional, que se equilibra con una excelente legibilidad de datos numéricos en diversas resoluciones y dispositivos (móviles, tabletas, pantallas industriales). Además, su disponibilidad a través de Google Fonts asegura una carga eficiente y consistente.

La jerarquía tipográfica se establece de la siguiente manera para garantizar claridad y ritmo visual:

* **Títulos principales (H1/Sección heading):** 5rem (aprox. 50px) en escritorio, 4.5rem (aprox. 45px) en móvil.
* **Subtítulos (H2/Sub-headings):** 3rem (aprox. 30px) en escritorio.
* **Títulos de componentes (H3/H4):** 2rem (aprox. 20px) a 2.5rem (aprox. 25px).
* **Cuerpo del texto (p):** 1.6rem (aprox. 16px) con un interlineado de 1.6.
* **Botones y etiquetas (span):** 1.4rem (aprox. 14px) a 1.8rem (aprox. 18px).

<p align="center">
  <img src="../assets/img/StyleFont.png" alt="Rubik Typography Guide" width="500px" height="auto"/>
</p>

Esta distribución garantiza un contraste óptimo entre el texto y el fondo, superando un ratio mínimo de 4.5:1 según las WCAG 2.1 AA para una accesibilidad superior en entornos de laboratorio.

<br>

**Colors**

Nuestra paleta de colores ha sido cuidadosamente seleccionada para evocar sensaciones de pulcritud, profesionalismo tecnológico y control. Se ha distribuido en tres categorías principales:

**Paleta principal**: Colores que definen la identidad de QualiTrack y se usan en elementos clave.
* **Primario (Verde Azulado / Teal QualiTrack):** var(--primary-color | #0D9488) (referencia principal).
* **Secundario (Azul Pizarra Oscuro):** var(--secondary-color | #0F172A) (para texto principal y elementos interactivos).
* **Terciario (Gris Pizarra):** var(--tertiary-color | #64748B) (para texto secundario y detalles).
* **Fondo Claro:** var(--bg-light) (fondos de secciones).
* **Fondo Blanco:** var(--white) (fondos de tarjetas y elementos principales).
  
**Paleta de Soporte**: Colores complementarios que añaden profundidad y contraste.
* **Gris Neutro:** Para bordes sutiles, líneas divisorias y fondos de alternancia.

**Colores Funcionales**: Reservados para comunicar estados específicos al usuario.
* **Éxito:** Verde (#4CAF50) para confirmaciones y acciones exitosas.
* **Error:** Rojo (#F44336) para alertas y mensajes de error.
* **Advertencia:** Amarillo (#FFC107) para notificaciones y avisos importantes.


<p align="center">
  <img src="../assets/img/Color_Pallete.png" alt="QualiTrack Color Palette" width="800px" height="auto"/>
</p>

Esta combinación cromática refleja los valores de nuestra marca y busca transmitir al público (laboratorios e instituciones como DIGEMID) una imagen de rigor científico, seguridad y trazabilidad inmutable.

<br>

**Spacing**

El espaciado en QualiTrack sigue un sistema de espaciado modular y consistente para garantizar un ritmo visual armonioso y una jerarquía clara en toda la interfaz. La consistencia en el espaciado ayuda a reducir la carga cognitiva del usuario y mejora la legibilidad de los reportes técnicos.

* **Espaciado Básico:** Usamos un espaciado base en el sistema de grid. Este valor es la unidad mínima y se multiplica para crear espacios más grandes.
* **Margen Interno (Padding) Generoso:** Las secciones principales de la página utilizan un padding vertical de 5rem (50px) para crear pausas visuales claras. Los contenedores de tarjetas o elementos secundarios usan padding más pequeños, como 3rem a 4rem (30px - 40px), para agrupar el contenido de forma lógica.
* **Espacio entre Elementos:** El espaciado entre elementos relacionados, como las tarjetas de planes o el bloque de características (features), varía entre 3rem (30px) y 5rem (50px). Esto mantiene una densidad de información adecuada sin abrumar visualmente al usuario frente a las métricas.
* **Line Height del Texto:** El interlineado del texto (line-height) está configurado en 1.6, lo que facilita la lectura de párrafos largos y evita que las líneas de datos se sientan demasiado juntas.

<br>

**Tono de Comunicación**

La voz y el tono de QualiTrack están diseñados para ser tan confiables y precisos como nuestra telemetría IoT. Nuestro objetivo es conectar con Jefes de Calidad e Inspectores Públicos de manera altamente profesional y técnica.

* **Tono: Formal y corporativo,** con un enfoque en la precisión. Buscamos proyectar autoridad y dominio sobre normativas regulatorias (BPM, Data Integrity), manteniendo la seriedad que exigen los laboratorios farmacéuticos.
* **Actitud: Resolutiva y segura.** El 90% de nuestra comunicación es orientada a la eficiencia y reducción de errores ("Eliminación del error humano", "Trazabilidad Inmutable"), mientras que el 10% restante es persuasiva, especialmente en los llamados a la acción para solicitar demos.
* **Lenguaje: Técnico y directo.** No evitamos la jerga de la industria, ya que nuestro usuario final la utiliza a diario (ej. LIMS, DIGEMID, Autoclaves, Telemetría). Nos enfocamos en los beneficios operativos que QualiTrack aporta a las líneas de producción.
* **Voz: Experta y vanguardista.** Posicionamos a QualiTrack como el estándar de la industria 4.0 en manufactura farmacéutica, siendo el escudo digital frente a las inspecciones regulatorias.

Este enfoque comunicacional busca generar confianza corporativa, asegurando a los laboratorios que están automatizando sus procesos de forma segura, y a las entidades de salud pública, que la plataforma garantiza la transparencia absoluta de los datos.

### 4.1.2. Web Style Guidelines

Las directrices de estilo web de **QualiTrack** se centran en la precisión técnica, la inmutabilidad de los datos y la eficiencia operativa. Nuestro objetivo es crear una experiencia visual que refleje la misión de nuestra plataforma: digitalizar y automatizar el control de calidad farmacéutico con un diseño limpio, tecnológico y altamente funcional.

**1) Layout**

* **Sistema de Grid:** Utilizamos un diseño de cuadrícula flexible para garantizar que el contenido de QualiTrack se adapte perfectamente a cualquier resolución. Este enfoque permite que las tarjetas de telemetría y los planes de suscripción se ajusten dinámicamente, manteniendo el orden y la coherencia visual necesarios en un entorno industrial.
* **Headers y Footers:** El encabezado (header) es fijo en la parte superior, proporcionando acceso constante a la navegación principal y a los botones de acceso al sistema (*Sign In*, *Sign Up*). El pie de página (footer) es completo y funcional, centralizando los enlaces legales, información de contacto institucional y la suscripción a actualizaciones.
* **Cards:** Las tarjetas son el componente central de nuestra interfaz para estructurar información crítica. Se utilizan para destacar los pilares de nuestra oferta (IoT, *Compliance*, Auditorías) y los planes de precios. Cuentan con bordes redondeados y sombras suaves para darles una apariencia moderna y "elevada", facilitando la lectura de parámetros técnicos.

**2) Responsive Design**

* **Desktop:** La navegación principal es totalmente visible en la barra superior junto a las acciones de usuario. El contenido se presenta en múltiples columnas para un uso eficiente del espacio en monitores de estaciones de trabajo de laboratorio.
* **Tablet:** Los elementos de la cuadrícula se adaptan a un diseño de dos columnas. Los botones y campos táctiles mantienen un tamaño adecuado para facilitar la interacción con guantes o en movimiento.
* **Mobile:** La experiencia está optimizada para una sola columna. La navegación se desplaza a un menú desplegable, y todos los elementos interactivos son grandes y claros, ideales para supervisores que monitorean la planta desde dispositivos móviles.

**3) Interaction Design**

* **Botones:** Nuestros botones son llamativos y utilizan los colores de marca. Cuentan con efectos visuales lineales al pasar el cursor para confirmar la interactividad. El botón principal de llamado a la acción destaca claramente para incentivar la conversión.
* **Formularios:** El formulario de contacto en el pie de página es sencillo y directo, ofreciendo una guía visual rápida y coherente en toda la página.

**4) Images and Icons**

* **Imágenes:** Se utilizan fotografías de alta calidad que evocan el entorno farmacéutico moderno: científicos en laboratorios y plantas de manufactura digitalizadas. Las imágenes están optimizadas para carga rápida y refuerzan el mensaje de tecnología aplicada a la seguridad de la salud.
* **Íconos:** Empleamos un estilo lineal y minimalista. Estos íconos representan visualmente servicios críticos como la telemetría IoT (antena), gestión de lotes (matraz) y cumplimiento regulatorio (escudo), ofreciendo una guía visual rápida y coherente en toda la página.

**5) Repositorio Central**

* **Organización:** El proyecto sigue una estructura de archivos lógica y modular. Los activos visuales se encuentran en `public/assets/images`, los estilos en `public/assets/styles/style.css`, y la lógica interactiva en `public/assets/scripts/main.js`.
* **Versionado:** Usamos **Git** como sistema de control de versiones para gestionar los cambios en el código y asegurar que todo el equipo de ClosedSource trabaje sobre la versión más estable y actualizada del producto.

## 4.2. Information Architecture

La arquitectura de la información de **QualiTrack** está diseñada para una navegación intuitiva y técnica, permitiendo que los Jefes de Aseguramiento de Calidad y Directores de Salud Pública encuentren rápidamente la información sobre cumplimiento y telemetría.

### 4.2.1. Organization Systems

* **Jerarquía de Contenidos:** La información está estructurada de lo general a lo específico para facilitar la toma de decisiones. Comenzamos con una propuesta de valor en la sección **Hero**, seguida de los pilares de nuestra oferta, y profundizamos en beneficios técnicos y planes de suscripción en las secciones finales.
* **Secciones Principales:** La página de inicio está organizada en bloques clave:
    * **Hero:** El futuro de la gestión de QualityTrack.
    * **What We Offer:** Visión general de los servicios ofrecidos.
    * **Features:** Desglose técnico de funcionalidades clave del producto.
    * **Benefits:** Ventajas competitivas como la eliminación del error humano.
    * **About Us:** Propósito de QualiTrack y cumplimiento con DIGEMID.
    * **Our Team:** Perfiles del equipo de ClosedSource.
    * **Plans:** Opciones de precios Standard y Enterprise.
    * **Testimonials & CTA:** Reseñas de directores de QA y llamado a la acción final.
* **Agrupación de Contenidos:** El contenido se agrupa lógicamente mediante el uso de contenedores visuales. Por ejemplo, las funcionalidades de la plataforma se presentan en un acordeón interactivo para no saturar al usuario, permitiéndole expandir solo el área de su interés técnico.

### 4.2.2. Labeling Systems

* **Nomenclatura:** Se utiliza un lenguaje técnico alineado a la industria farmacéutica en los títulos de las secciones. Los botones tienen etiquetas accionables como *Request a Demo*, *Sign In* y *Sign Up*.
* **Consistencia:** Mantenemos una nomenclatura uniforme en toda la plataforma. La sección de costos se identifica como *Plans* tanto en la navegación principal como en el título de la sección de precios.
* **Lenguaje Adaptativo:** El contenido está diseñado para ser comprendido por profesionales del sector farmacéutico, integrando términos regulatorios clave como DIGEMID y BPM sin perder la claridad operativa.

### 4.2.3. Searching Systems

* **Barra de Búsqueda:** Aunque la *landing page* informativa no la requiere, una vez que el usuario accede a la aplicación SaaS de QualiTrack, esta funcionalidad será crítica. Estará ubicada en el panel de control para buscar rápidamente por **ID de Lote**, sensores específicos o reportes de auditoría.
* **Filtros y Facetas:** Dentro de la aplicación, los usuarios podrán filtrar datos por tipo de equipo (autoclaves, pH metros), rangos de fecha de producción o severidad de alertas de cumplimiento detectadas.
* **Historial de Búsqueda:** Se implementará un registro para que los auditores y administradores puedan acceder rápidamente a los lotes consultados con mayor frecuencia durante las inspecciones.
* **Resultados Relevantes:** Los resultados se priorizarán según la criticidad de la alerta o la fase actual del lote de producción.

### 4.2.4. Navigation Systems

* **Navegación Global:** La barra de navegación en el encabezado proporciona acceso principal a las secciones de la página de inicio (*Home, Features, Benefits, About Us, Plans*).
* **Navegación Contextual:** Enlaces internos y botones estratégicos (CTAs) guían al usuario hacia la siguiente etapa de su recorrido, como la solicitud de una demostración técnica.

## 4.3. Landing Page UI Design

El diseño de la interfaz de usuario (UI) de la página de inicio de QualiTrack es fundamental para captar la atención de los profesionales del sector farmacéutico y guiarlos hacia una acción clara: garantizar el cumplimiento normativo y la integridad de datos en sus procesos de manufactura. Nos hemos centrado en la creación de una experiencia intuitiva y fluida, asegurando que cada elemento de la página sea interactivo y fácil de usar, reflejando el compromiso de QualiTrack con la precisión, la transparencia y la automatización inteligente en la gestión de calidad farmacéutica.

### 4.3.1. Landing Page Wireframe

El wireframe de nuestra página de inicio sirve como un mapa visual que define la estructura y el flujo de la información, alineado con los principios de rigurosidad y claridad que exige el sector farmacéutico. Este esquema asegura una disposición lógica de los componentes, facilitando la navegación y destacando la propuesta de valor de **QualiTrack.** Las secciones del wireframe están diseñadas para contar una historia completa y persuasiva:

**Nav y Hero:**

Esta sección inicial incluye el logotipo de QualiTrack junto con una presentación breve que introduce al visitante en la propuesta de valor de la plataforma: 'The Future of Pharmaceutical Quality Management' (El futuro de la gestión de calidad farmacéutica). La barra de navegación permite un acceso rápido a secciones clave como Features, Benefits y About Us, mientras que el área principal ofrece una visión concisa del producto, acompañada de un claro llamado a la acción: 'Start now →' (Comenzar ahora →). Un elemento visual atractivo refuerza el mensaje de innovación tecnológica, precisión y cumplimiento regulatorio que distingue a QualiTrack.

<img src="../assets/img/hero-section-landing-wireframe.png" alt="Landing Page Mockup" style="max-width: 100%; height: auto; border: 2px solid #00bfff;">

**Services (What We Offer):**

Aquí se detallan los servicios principales de QualiTrack: Real-Time IoT Monitoring, Automated BPM Compliance, Immutable Audit Trails y Digital Batch Management. Cada servicio se presenta con un icono representativo y una breve descripción, haciendo que nuestra oferta sea fácil de entender y visualmente accesible.

<img src="../assets/img/whatweoffer-section-landing-wireframe.png" alt="Landing Page Mockup" style="max-width: 100%; height: auto; border: 2px solid #00bfff;">

**Acerca de la aplicación (About the Platform):**

Esta sección presenta lo que hace única a QualiTrack: una plataforma para laboratorios farmacéuticos que automatiza el control de calidad mediante integración IoT, elimina errores manuales y garantiza la trazabilidad inmutable. Destacamos beneficios clave como captura automática de telemetría, alertas en tiempo real y cumplimiento nativo con normativas DIGEMID.

<img src="../assets/img/benefits-section-landing-wireframe.png" alt="Landing Page Mockup" style="max-width: 100%; height: auto; border: 2px solid #00bfff;">

**Sobre el Equipo (Our Team):**

En esta sección, se humaniza la marca al presentar al equipo detrás de QualiTrack. Con fotos y descripciones de los miembros, mostramos a las personas dedicadas a este proyecto, construyendo confianza y una conexión personal con los visitantes.

<img src="../assets/img/ourteam-section-landing-wireframe.png" alt="Landing Page Mockup" style="max-width: 100%; height: auto; border: 2px solid #00bfff;">

**Precios (Plans):**

La sección de Precios ofrece una visión clara de los planes disponibles. Presentamos el Standard Lab Plan y el Enterprise Plan, con una comparativa de características para ayudar a los usuarios a elegir la opción que mejor se adapte a sus necesidades, ya sea para un laboratorio mediano o para una institución de salud pública. Un selector entre tarifas mensuales y anuales, junto con la indicación del ahorro asociado, facilita una elección más informada.

<img src="../assets/img/plans-section-landing-wireframe.png" alt="Landing Page Mockup" style="max-width: 100%; height: auto; border: 2px solid #00bfff;">

**Footer:**

El pie de página es un elemento crucial para la usabilidad. Contiene enlaces a información vital como "Terms of Service" y "Privacy Policy", además de detalles de contacto (correo electrónico, teléfono y ubicación). Esto proporciona un acceso rápido a la información sin saturar la interfaz, ofreciendo un cierre limpio y funcional a la página.

<img src="../assets/img/footer-section-landing-wireframe.png" alt="Landing Page Mockup" style="max-width: 100%; height: auto; border: 2px solid #00bfff;">

Este wireframe sienta las bases para un diseño visual que no solo se ve bien, sino que también guía al usuario de manera intuitiva a través de nuestra propuesta de valor, reforzando la confianza y la conexión que QualiTrack promete.

<div style="page-break-after: always;"></div>

### 4.3.2. Landing Page Mock-up

**Hero de la aplicación**

El hero de nuestra plataforma QualiTrack presenta una imagen principal que evoca precisión tecnológica y cumplimiento normativo, con un título claro: 'The Future of Pharmaceutical Quality Management'. Una breve descripción capta nuestra esencia de automatización y trazabilidad inmutable, y un botón de llamado a la acción 'Start now →' invita a los usuarios a dar el primer paso hacia la digitalización de sus procesos de calidad. Una barra de navegación en la parte superior permite acceder de forma fluida a todas las secciones de la página, proporcionando una experiencia de usuario intuitiva.

<img src="../assets/img/hero-section-landing.png" alt="Landing Page Mockup" style="max-width: 100%; height: auto; border: 2px solid #00bfff;">

**What We Offer**

En la sección 'What We Offer', presentamos nuestras principales áreas de servicio a través de tarjetas con iconos representativos. Cada tarjeta cuenta con un título y una breve descripción, como 'IoT Integration', 'Immutable Traceability' o 'Regulatory Compliance', lo que permite a los usuarios entender rápidamente el alcance de nuestra plataforma y los tipos de soluciones que ofrecemos para la gestión de calidad farmacéutica.

<img src="../assets/img/whatweoffer-section-landing.png" alt="Landing Page Mockup" style="max-width: 100%; height: auto; border: 2px solid #00bfff;">

**Features**

La sección de "Features" muestra las funcionalidades clave de QualiTrack. El diseño tipo acordeón permite a los usuarios expandir cada característica para leer su descripción completa, mientras que un video de demostración de YouTube al lado les ofrece una vista visual de la plataforma en acción. Esto combina información detallada con un formato interactivo y dinámico.

<img src="../assets/img/features-section-landing.png" alt="Landing Page Mockup" style="max-width: 100%; height: auto; border: 2px solid #00bfff;">

**Benefits**

En 'Benefits', destacamos las ventajas de utilizar QualiTrack. A través de un diseño de tarjetas con imágenes, títulos y descripciones, comunicamos cómo nuestra plataforma elimina el error humano en registros críticos, agiliza la preparación para auditorías regulatorias y aumenta la integridad y trazabilidad de los datos tanto para laboratorios farmacéuticos como para entidades de salud pública.

<img src="../assets/img/benefits-section-landing.png" alt="Landing Page Mockup" style="width: auto; height: auto; border: 2px solid #00bfff;">

**About Us**

La sección 'About Us' presenta a ClosedSource, la empresa detrás de QualiTrack. Aquí, compartimos nuestra misión de transformar la supervisión de procesos farmacéuticos mediante la integración IoT y el cumplimiento normativo, así como los valores de innovación, transparencia e integridad de datos que nos impulsan. Un video o imagen animada acompaña el texto, reforzando nuestro mensaje de una manera visualmente atractiva y moderna.

<img src="../assets/img/aboutus-section-landing.png" alt="Landing Page Mockup" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Our Team**

La sección "Our Team" presenta a los ingenieros de software detrás de ClosedSource. Las tarjetas de perfil muestran una foto, el nombre, el cargo y una breve biografía de cada miembro. El diseño de 3 tarjetas arriba y 2 abajo, centradas, brinda un aspecto organizado y profesional, permitiendo a los usuarios conocer al equipo de desarrollo.

<img src="../assets/img/ourteam-section-landing.png" alt="Landing Page Mockup" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Plans**

En la sección de "Plans", ofrecemos los detalles de nuestros planes de precios. Las tarjetas de "Standard Lab Plan" y "Enterprise Home Plan" incluyen descripciones, precios con opciones mensuales y anuales, y listas de características. El diseño permite un fácil cambio entre planes mensuales y anuales, facilitando la elección del plan adecuado.

<img src="../assets/img/plans-section-landing.png" alt="Landing Page Mockup" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Footer**

El "Footer" de nuestra landing page contiene enlaces útiles y recursos adicionales. Un formulario de suscripción invita a los usuarios a unirse a nuestra comunidad. El logo de QualiTrack, enlaces de contacto, información legal y de derechos de autor se encuentran aquí, asegurando que toda la información relevante esté fácilmente accesible para los usuarios.

<img src="../assets/img/footer-section-landing.png" alt="Landing Page Mockup" style="width: auto; height: auto; border: 2px solid #00bfff;">

<div style="page-break-after: always;"></div>

## 4.4. Web Applications UX/UI Design

### 4.4.1. Web Applications Wireframes

En esta sección se presentan los **wireframes diseñados para la aplicación web de ClosedSource(QualiTrack)**. Cada pantalla responde a las funcionalidades principales del sistema de gestión de calidad e integración IoT, atendiendo a los roles de usuario definidos: Jefe de Aseguramiento de la Calidad (QA), Operario de planta y Auditor.

**Portal de Inicio - ClosedSource** 

Pantalla principal de presentación donde se ofrecen las opciones de ingreso y registro de nuevas plantas industriales.

<img src="../assets/img/Login - ClosedSource.jpeg" alt="Login - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Crear Cuenta - ClosedSource**  

Formulario para registrar laboratorios, solicitando datos del responsable y credenciales de acceso.

<img src="../assets/img/Registro – ClosedSource.jpeg" alt="Registro – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Ingreso al Sistema - ClosedSource** 

Pantalla de autenticación para usuarios registrados con campos de correo y contraseña.

<img src="../assets/img/Inicio de Sesión – ClosedSource.jpeg" alt="Inicio de Sesión – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Panel de Control - ClosedSource** 

Vista general de la planta que muestra el progreso del lote activo y el estado de las unidades de producción.

<img src="../assets/img/Ingreso-al-Sistema- ClosedSource.jpeg" alt="Ingreso-al-Sistema- ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Ejecución de Lote - ClosedSource** 

Interfaz para registrar materias primas y verificar procesos con monitoreo de telemetría en vivo.

<img src="../assets/img/Ejecución-de-Lote-Activo – ClosedSource.jpeg" alt="Ejecución-de-Lote-Activo – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Estado de Equipos - ClosedSource** 

Pantalla de monitoreo técnico que detalla el funcionamiento de la maquinaria y sus sensores IoT.

<img src="../assets/img/Estado-de-Equipamiento-IoT – ClosedSource.jpeg" alt="Estado-de-Equipamiento-IoT – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Centro de Alertas - ClosedSource** 

Módulo de respuesta ante emergencias que permite pausar procesos cuando se detectan desviaciones críticas.

<img src="../assets/img/Gestión-de-Alertas-e-Incidentes – ClosedSource.jpeg" alt="Gestión-de-Alertas-e-Incidentes – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Resumen de Calidad - ClosedSource** 

Panel consolidado con gráficos e indicadores de cumplimiento (KPIs) globales del laboratorio.

<img src="../assets/img/Dashboard-General – ClosedSource.jpeg" alt="Dashboard-General – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Módulo de Cumplimiento - ClosedSource** 

Sección dedicada a la validación de normativas y estándares de calidad para cada producto.

<img src="../assets/img/Cumplimiento - Normativo – ClosedSource.jpeg" alt="Cumplimiento - Normativo – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Historial de Lotes - ClosedSource** 

Listado de trazabilidad que permite buscar y filtrar todos los lotes fabricados anteriormente.

<img src="../assets/img/Ciclo-de-Vida-del-Lote – ClosedSource.jpeg" alt="Ciclo-de-Vida-del-Lote – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Análisis y Configuración de Equipos - ClosedSource**

Panel técnico para el monitoreo de telemetría de equipos activos y la configuración detallada de umbrales y parámetros BPM

<img src="../assets/img/Análisis-y-Configuración-de-Equipos - ClosedSource.jpeg" alt="Análisis-y-Configuración-de-Equipos - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;"> 

**Logs de Auditoría - ClosedSource**

Interfaz para exportar registros de eventos inmutables para inspecciones de DIGEMID.

<img src="../assets/img/Logs-de-Auditoría - ClosedSource .jpeg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

### 4.4.2. Web Applications Wireflow Diagrams

Los Wireflows se utilizan, sobre todo, en el diseño de la experiencia del usuario (UX) y son particularmente beneficiosos para aplicaciones que contienen interacciones complejas y flujos de trabajo.

<img src="../assets/img/Web-Applications-Wireflow-Diagrams.jpeg" alt="Web-Applications-Wireflow-Diagrams" style="width: auto; height: auto; border: 2px solid #00bfff;">

### 4.4.3. Web Applications Mock-ups

En esta sección se presentan los mock-ups diseñados para la aplicación web de ClosedSource(QualiTrack). Cada pantalla responde a las funcionalidades principales del sistema

**Inicio - ClosedSource**

Página de bienvenida con selección de rol (QA Manager/Supervisor o Lab Operator) para acceder al sistema.

<img src="../assets/img/mockup/outside/home.jpg" alt="Login - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Inicio de Sesión - ClosedSource**

Módulo de autenticación de usuarios con credenciales (usuario y contraseña) para acceder a QualiTrack.

<img src="../assets/img/mockup/outside/iam_sign-in.jpg" alt="Registro – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Registro de Gestor de Calidad - ClosedSource**

Creación de cuenta para rol de QA Manager/Supervisor con permisos de administración de calidad.

<img src="../assets/img/mockup/outside/iam_sign-up_role=manager.png" alt="Inicio de Sesión – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Registro de Operador de Laboratorio - ClosedSource**

Creación de cuenta para rol de Operador de Laboratorio con acceso a operaciones diarias del laboratorio.

<img src="../assets/img/mockup/outside/iam_sign-up_role=operator.jpg" alt="Ingreso-al-Sistema- ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Panel de Telemetría - ClosedSource**

Monitorización en tiempo real de datos sensoriales de equipos, mostrando estado de conexión y lecturas actuales.

<img src="../assets/img/mockup/tracking/tracking_dashboard.jpg" alt="Panel-de-Telemetría – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Análisis de Telemetría - ClosedSource**

Módulo de análisis de datos históricos de telemetría de equipos con gráficos y filtros por fecha.

<img src="../assets/img/mockup/tracking/tracking_analysis.jpg" alt="Análisis-de-Telemetría – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

Registro de Telemetría - ClosedSource

Registro detallado de datos crudos de telemetría con búsqueda y filtros por equipo y rango de fechas.

<img src="../assets/img/mockup/tracking/tracking_history.jpg" alt="Registro-de-Telemetría – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Listado de Lotes de Producción - ClosedSource**

Módulo de listado y seguimiento de lotes para control de trazabilidad y calidad en los ciclos productivos.

<img src="../assets/img/mockup/batch/batch_batch-list.jpg" alt="Ejecución-de-Lote-Activo – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Registro de Nuevo Lote - ClosedSource**

Formulario para registrar lotes de producción con especificaciones de calidad, número de lote de proveedor y stock inicial.

<img src="../assets/img/mockup/batch/batch_batch-form.jpg" alt="Estado-de-Equipamiento-IoT – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Ficha Técnica de Lote - ClosedSource**

Módulo de visualización de detalles técnicos de lotes de producción, incluyendo información general y materias primas asociadas.

<img src="../assets/img/mockup/batch/batch_batch-detail_1.jpg" alt="Gestión-de-Alertas-e-Incidentes – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Liberación de Lote - ClosedSource**

Módulo para liberar lotes que cumplen especificaciones, con registro de notas del proceso BPM.

<img src="../assets/img/mockup/batch/batch_batch-release-form_1.jpg" alt="Dashboard-General – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Rechazo de Lote - ClosedSource**

Registro de lotes no conformes, especificando motivo de rechazo y fecha para auditoría de calidad.

<img src="../assets/img/mockup/batch/batch_batch-reject-form_1.jpg" alt="Cumplimiento - Normativo – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Catálogo de Equipos - ClosedSource**

Gestión y monitoreo de activos de laboratorio con listado de equipos, modelo, número de serie y estado.

<img src="../assets/img/mockup/equipment/equipment_equipment-list.jpg" alt="Ciclo-de-Vida-del-Lote – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Registro de Nuevo Equipo - ClosedSource**

Alta de nuevos equipos en el catálogo ingresando especificaciones técnicas como nombre, tipo, modelo y número de serie.

<img src="../assets/img/mockup/equipment/equipment_register-equipment.jpg" alt="Análisis-y-Configuración-de-Equipos - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;"> 

**Detalle de Equipo - ClosedSource**

Visualización de información general y configuración BPM de equipos de laboratorio.

<img src="../assets/img/mockup/equipment/equipment_equipment-detail_1.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Detalle de Mantenimiento del Equipo - ClosedSource**

Módulo de detalles técnicos de equipos, incluyendo configuración BPM y acceso al historial de mantenimiento.

<img src="../assets/img/mockup/equipment/equipment_equipment-detail_2.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Historial de Mantenimiento - ClosedSource**

Registro cronológico de eventos de mantenimiento y calibración de equipos.

<img src="../assets/img/mockup/equipment/equipment_equipment-detail_3.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Configuración de Parámetros BPM - ClosedSource**

Definición de rangos de tolerancia y parámetros de monitoreo de calidad para equipos industriales.

<img src="../assets/img/mockup/equipment/equipment_bpm-config-form_1.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Historial de Mantenimiento - ClosedSource**

Registro cronológico de actividades técnicas con opción de añadir nuevos eventos de mantenimiento.

<img src="../assets/img/mockup/equipment/equipment_maintenance-history_1.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Registro de Actividad Técnica - ClosedSource**

Formulario para registrar intervenciones técnicas, mantenimientos y calibraciones realizadas por técnicos responsables.

<img src="../assets/img/mockup/equipment/equipment_maintenance-form_1.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Centro de Alertas - ClosedSource**

Módulo de respuesta ante emergencias que permite pausar procesos cuando se detectan desviaciones críticas.

<img src="../assets/img/mockup/ca/ca_alert-dashboard.jpg" alt="Gestión-de-Alertas-e-Incidentes – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Historial de Alertas - ClosedSource**

Registro completo de todas las desviaciones de calidad con filtros por equipo, severidad y estado.

<img src="../assets/img/mockup/ca/ca_alert-history.jpg" alt="Gestión-de-Alertas-e-Incidentes – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Detalle de Desviación - ClosedSource**

Inspección técnica de alertas de calidad mostrando detalles específicos de la desviación detectada.

<img src="../assets/img/mockup/ca/ca_deviation-detail_1.jpg" alt="Gestión-de-Alertas-e-Incidentes – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Preferencias de Notificación - ClosedSource**

Configuración de canales (app, email, SMS) y umbrales de severidad para recibir alertas del sistema.

<img src="../assets/img/mockup/ca/ca_notification-settings.jpg" alt="Gestión-de-Alertas-e-Incidentes – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Panel de KPIs - ClosedSource**

Indicadores clave de rendimiento y métricas de calidad para supervisión de laboratorio.

<img src="../assets/img/mockup/ra/ra_kpi-dashboard.jpg" alt="Dashboard-General – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Análisis de Tendencias - ClosedSource**

Módulo de análisis de tendencias de desviaciones para identificar patrones y mejorar procesos de calidad.

<img src="../assets/img/mockup/ra/ra_deviation-trends.jpg" alt="Dashboard-General – ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Generador de Reportes - ClosedSource**

Generación de informes de calidad, trazabilidad de lotes, cumplimiento y exportación de datos técnicos (PDF/CSV).

<img src="../assets/img/mockup/ra/ra_report-generator.jpg" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Registro de Auditoría - ClosedSource**

Trazabilidad completa de acciones del sistema con timestamp, entidad afectada y usuario responsable.

<img src="../assets/img/mockup/ra/ra_audit-log.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Perfil de Laboratorio - ClosedSource**

Gestión de información del laboratorio y acceso a módulos de personal, productos y materias primas.

<img src="../assets/img/mockup/laboratory/laboratory_lab-profile.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Listado de Personal - ClosedSource**

Lista de miembros del laboratorio con sus roles, correo corporativo y estado laboral.

<img src="../assets/img/mockup/laboratory/laboratory_staff-list.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Registro de Personal - ClosedSource**

Formulario para añadir personal autorizado al laboratorio, asignando rol y correo electrónico.

<img src="../assets/img/mockup/laboratory/laboratory_staff-form.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Catálogo de Productos Farmacéuticos - ClosedSource**

Listado de productos con especificaciones BPM, código SKU y estado, con funcionalidad de búsqueda.

<img src="../assets/img/mockup/laboratory/laboratory_product-catalog.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Registro de Producto - ClosedSource**

Formulario para registrar nuevos productos farmacéuticos con nombre comercial, descripción terapéutica y especificaciones de calidad.

<img src="../assets/img/mockup/laboratory/laboratory_product-form.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Listado de Materias Primas - ClosedSource**

Inventario de materias primas con código interno, proveedor autorizado, stock actual y fecha de caducidad.

<img src="../assets/img/mockup/laboratory/laboratory_raw-material-list.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

**Registro de Materia Prima - ClosedSource**

Entrada de materiales al inventario farmacéutico con control de lote, proveedor, fecha de caducidad, cantidad y umbral de stock mínimo.

<img src="../assets/img/mockup/laboratory/laboratory_raw-material-form.jpg" alt="Logs-de-Auditoría - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

### Mock-ups Version Mobile
<p>La sección de Web Applications UX/UI Design presenta la propuesta visual, estructural y de interacción desarrollada para las distintas aplicaciones que conforman la experiencia digital de QualiTrack, el ecosistema orientado a la gestión integral de operaciones de precisión clínica, el monitoreo de telemetría IoT en tiempo real y la trazabilidad inmutable de lotes de producción.

El diseño se elaboró siguiendo principios de usabilidad, accesibilidad, consistencia visual y orientación a tareas críticas, asegurando que cada interfaz responda a las exigentes necesidades normativas y operativas identificadas durante el proceso de investigación. La propuesta UI/UX se centra en crear una experiencia clara, confiable y altamente precisa, facilitando la interacción transparente y la toma de decisiones rápidas para distintos perfiles, desde operarios de planta hasta jefes de calidad e inspectores públicos (como DIGEMID).</p>

<img src="../assets/img/mobile1.png" alt="inicio" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile2.png" alt="mobile2" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile3.png" alt="mobile3" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile4.png" alt="mobile4" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile5.png" alt="mobile5" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile6.png" alt="mobile6" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile7.png" alt="mobile7" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile8.png" alt="mobile8" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile9.png" alt="mobile9" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile10.png" alt="mobile10" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile11.png" alt="mobile11" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile12.png" alt="mobile12" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile13.png" alt="mobile13" style="width:auto; height:auto; border:2px solid #00bfff;">
<img src="../assets/img/mobile14.png" alt="mobile14" style="width:auto; height:auto; border:2px solid #00bfff;">

### 4.4.4. Web Applications User Flow Diagrams

El user flow es la representación visual del camino que un usuario sigue dentro de la plataforma QualiTrack para alcanzar un objetivo específico, como registrar un lote de producción, atender una alerta de desviación o generar un reporte de auditoría. Estos diagramas son esenciales para garantizar que la navegación sea lógica, intuitiva y libre de obstáculos, asegurando una experiencia de usuario satisfactoria y eficiente para cada uno de los roles definidos en el sistema: Jefe de Aseguramiento de la Calidad (QA Manager), Operario de laboratorio y Auditor regulatorio. A continuación, se detallan los flujos para las tareas clave de la plataforma, alineados con los procesos de cumplimiento BPM, monitoreo IoT y trazabilidad inmutable exigidos por DIGEMID.

---

- #### **Objetivo 1: Un operativo o supervisor desea registrarse e iniciar sesión en el sistema.**

  **Happy Path**

  En este flujo ideal, el usuario accede por primera vez a QualiTrack y, al no tener una cuenta registrada, desde la pantalla de inicio de sesión selecciona la opción "Registrarse", completa el formulario con los datos del laboratorio y sus credenciales, y una vez finalizado el proceso exitosamente es redirigido a la sección de inicio de sesión, donde ingresa su correo y contraseña; si se trata de un Jefe de Aseguramiento de la Calidad (QA Manager), el sistema le presenta el dashboard de telemetría en tiempo real con los indicadores de cumplimiento BPM y el estado de los lotes activos, mientras que si el usuario es un Operario de planta, se le muestra una interfaz especializada enfocada en el monitoreo de equipos industriales, alertas de desviación y registro de observaciones en el laboratorio.

  <img src="../assets/img/web-applications-user-flow-diagrams/happy-path-1(1).png" alt="Inició de sesión - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">
  <img src="../assets/img/web-applications-user-flow-diagrams/happy-path-1(2).png" alt="Inició de sesión - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">
  
  **Unhappy Path**

  En este escenario alternativo, el usuario intenta acceder a QualiTrack con su cuenta, pero se presenta un problema técnico como credenciales incorrectas, conectividad inestable o bloqueo temporal por múltiples intentos fallidos; por lo tanto, el sistema no permite el ingreso y muestra un mensaje de error específico según la causa, invitando al usuario a verificar sus datos, revisar su conexión o contactar al administrador del laboratorio, registrando cada intento fallido en el log de auditoría para garantizar la trazabilidad exigida por DIGEMID.

  <img src="../assets/img/web-applications-user-flow-diagrams/unhappy-path-1.png" alt="Inició de sesión - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

----

- #### **Objetivo 2: Un supervisor necesita realizar una investigación de una alerta activa.**

  **Happy Path**

  En este flujo ideal, el Supervisor de QA identifica una alerta activa en el dashboard de telemetría, presiona el botón "Investigate" para iniciar el análisis de la desviación detectada, luego presiona el botón "Complete Investigation" una vez que ha revisado la información, y finalmente espera a que el sistema realice el proceso de investigación automática, el cual confirma el origen de la desviación y, si corresponde, libera o mantiene el bloqueo del lote conforme a los parámetros BPM, registrando toda la acción en el historial inmutable de cumplimiento.

  <img src="../assets/img/web-applications-user-flow-diagrams/happy-path-2.png" alt="Inició de sesión - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

  **Unhappy Path**

  En este escenario alternativo, el supervisor presiona el botón "Investigate" sobre una alerta activa, luego presiona "Complete Investigation" para finalizar el análisis, pero al esperar el proceso de investigación automática, el sistema presenta dificultades técnicas como lentitud extrema, timeout de conexión o error en el motor de compliance, impidiendo que la investigación se complete correctamente; como resultado, la alerta permanece sin resolver, el lote no cambia de estado y se muestra un mensaje de error, quedando registrado el incidente en el log de auditoría para su revisión posterior.

  <img src="../assets/img/web-applications-user-flow-diagrams/unhappy-path-2.png" alt="Inició de sesión - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

----

- #### **Objetivo 3: El usuario requiere modificar la configuración tanto del sistema como su perfil.**

  **Happy Path**

  En este flujo ideal, el usuario accede a la sección de configuración, modifica los datos que necesita actualizar (como perfil de usuario, información de la organización o preferencias de notificación), luego presiona el botón "Save Settings" y finalmente espera a que el sistema procese y cargue los cambios correctamente, mostrando un mensaje de confirmación y aplicando las nuevas configuraciones en toda la plataforma sin afectar la continuidad operativa del laboratorio.

  <img src="../assets/img/web-applications-user-flow-diagrams/happy-path-3.png" alt="Inició de sesión - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

  **Unhappy Path**

  En este escenario alternativo, el usuario modifica los datos necesarios en la sección de configuración y presiona el botón "Save Settings", pero al esperar que se carguen los cambios, el sistema presenta dificultades técnicas como validación de campos fallida (formato de correo incorrecto, contraseñas que no coinciden, URL inválida), problemas de conectividad con el servidor o un error interno en la API; como resultado, la configuración no se guarda, se muestra un mensaje de error específico indicando la causa, y el usuario debe corregir los datos o reintentar la operación, quedando registrado el intento fallido en el log de auditoría para garantizar la trazabilidad exigida por DIGEMID.

  <img src="../assets/img/web-applications-user-flow-diagrams/unhappy-path-3.png" alt="Inició de sesión - ClosedSource" style="width: auto; height: auto; border: 2px solid #00bfff;">

## 4.5. Web Applications Prototyping

La sección de Web Applications Prototyping presenta los prototipos interactivos diseñados para la versión Desktop y Mobile Web de QualiTrack. Estos prototipos permiten simular la navegación real dentro de la plataforma y visualizar cómo los usuarios recorren los principales paths definidos en los User Flow Diagrams.

Las decisiones de interacción tomadas en esta etapa responden a tres criterios fundamentales:

- Claridad y eficiencia operativa, especialmente considerando que los operarios y supervisores requieren acceder a datos críticos en entornos de producción donde cada segundo cuenta.

- Rapidez de acceso a la información de cumplimiento, alineada con la necesidad de monitorear telemetría IoT en tiempo real y atender alertas de desviación BPM antes de que afecten la calidad del lote.

- Consistencia visual y funcional, asegurando que las interacciones sean predecibles y estén alineadas con el Design System de QualiTrack, reflejando la rigurosidad exigida por DIGEMID.
  <br>

**Criterios que guiaron las decisiones de interacción**

1. Arquitectura de Información basada en prioridades del usuario

La estructura del contenido se organizó priorizando los elementos más consultados por los Jefes de Aseguramiento de la Calidad y los Operarios de planta.

- Telemetría en tiempo real

- Estado y trazabilidad de lotes activos

- Alertas de desviación y bloqueo automático

- Registro y liberación digital de lotes

- Historial de auditoría y reportes PDF

- Configuración de equipos y parámetros BPM

Estos componentes se ubicaron en zonas de acceso rápido tanto en desktop como en mobile, asegurando rutas de navegación cortas y directas.

<br>

2. Navegación clara y consistente

Se optó por un sistema de navegación híbrido:

En desktop, un menú superior horizontal que mantiene visibles las secciones principales.

En mobile, un menú inferior tipo tab-bar para accesos frecuentes y un menú hamburguesa para secciones secundarias.

Esta decisión refleja la arquitectura de información previamente definida y garantiza que las rutas de navegación coincidan con los User Flow Diagrams propuestos.

<br>

3. Interacciones basadas en patrones familiares

Para reducir la curva de aprendizaje se utilizaron patrones estándar, como:

- Tarjetas para resumir el estado de cada equipo IoT y sus últimas mediciones.

- Gráficos en tiempo real para visualizar la evolución de variables críticas.

- Acordeones para desglosar el historial de alertas por lote o equipo.

- Iconos universales (alerta, bloqueo, liberación, calibración).

- Transiciones suaves que evitan saturar la experiencia durante la actualización de datos.

<br>

4. Principios de diseño inclusivo

Los prototipos consideran la diversidad de entornos donde se usa QualiTrack:

- Tipografías legibles y de alto contraste para pantallas industriales con iluminación variable.

- Botones amplios y bien espaciados para facilitar el uso con guantes o en dispositivos táctiles.

- Lenguaje visual claro y directo, utilizando colores funcionales (verde = conforme, rojo = desviación, amarillo = advertencia).

Los prototipos desktop muestran una interfaz amplia, optimizada para Jefes de Aseguramiento de la Calidad (QA Manager) y supervisores que consultan información desde una laptop o PC en la sala de control. Entre los elementos destacados:

• Dashboard principal

Vista general del cumplimiento BPM del laboratorio.

Resumen de lotes activos y su estado de trazabilidad.

Gráficos en tiempo real de telemetría (temperatura, presión, pH).

<br>

• Navegación superior

Acceso rápido a Dashboard, Lotes, Equipos, Alertas, Reportes y Configuración.

Persistencia visual para orientar al usuario.

<br>

• Secciones modulares

El contenido se divide en bloques visuales que permiten una lectura rápida:

Tarjetas de estado de cada equipo IoT con sus últimas mediciones.

Tablas de trazabilidad de lotes y materias primas.

Calendarios interactivos para mantenimientos y calibraciones.

Panel lateral con alertas de desviación no atendidas.

La versión móvil prioriza la usabilidad y accesibilidad para operarios de planta que se desplazan por el laboratorio, manteniendo la esencia visual del desktop pero adaptada a pantallas reducidas.

<br>

• Home simplificado

Resumen instantáneo de alertas activas, último lote en producción y estado de conexión de los equipos IoT.

Acceso directo a alertas, lotes activos y telemetría crítica.

<br>

• Tab-Bar inferior

Incluye 4 accesos principales:

Telemetría

Alertas

Lotes

Perfil

Esto reduce la carga cognitiva y facilita el uso con una sola mano.

<br>

• Menú hamburguesa

Incluye secciones secundarias como Reportes de auditoría, Configuración de equipos, Logs de cumplimiento y Ayuda. Se evita sobrecargar la pantalla principal.

<br>

• Interacción táctil optimizada

Botones grandes y espaciados.

Acordeones y sliders fáciles de usar.

Scroll vertical continuo para favorecer fluidez.

<br>

**Relación con los User Flow Diagrams**

Cada prototipo fue diseñado respetando los recorridos definidos en los User Flows, garantizando que:

Las pantallas aparezcan en el orden lógico previsto.

No existan rutas muertas o pasos innecesarios.

Las tareas principales (atender una alerta de desviación, investigar su causa, completar la investigación, guardar configuración de equipos) se completen con la menor cantidad de clics posible.

La navegación sea intuitiva para usuarios con distintos niveles tecnológicos, desde operarios hasta QA Managers.

<img src="../assets/img/prototypy.png" alt="ContextDiagram-Diagram" style="width: auto; height: auto; border: 2px solid #00bfff;">

https://shorturl.at/kcHKY

## 4.6. Domain-Driven Software Architecture

La arquitectura de QualiTrack se fundamenta en Domain-Driven Design (DDD) para modelar con precisión las reglas de negocio del sector farmacéutico, incluyendo el cumplimiento BPM, la integración IoT y la trazabilidad inmutable exigida por DIGEMID. Mediante la delimitación de bounded contexts, se separan claramente las responsabilidades de cada subsistema. En esta sección se presentan los resultados del Event Storming, así como los diagramas de contexto, contenedores y componentes que estructuran la solución.

## 4.6.1. Design-Level Event Storming

Para identificar los eventos de dominio, es recomendable realizar una sesión de Event 
Storming. Esta técnica permite visualizar y comprender el flujo de eventos dentro del 
dominio, facilitando la identificación de los Bounded Contexts.

El desarrollo del proceso del Domain-Driven Design se realizó en la aplicación Miro: 
[https://shorturl.at/0eSVT]

---
#### Paso 1: Brainstorming (Unstructured Exploration)

El primer paso consistió en realizar una exploración sin estructura para identificar todos los posibles eventos del dominio. Durante esta etapa, el equipo analizó criterios como la mutación de estados y la ejecución exitosa de comandos en el sistema, identificando 38 situaciones concretas (Domain Events) que los diferentes actores del sistema desencadenan. Entre los eventos más relevantes se capturaron: "Batch created", "Measurement recorded", "Deviation alert triggered", "Equipment registered", "Calibration alert triggered", "Raw material usage recorded" y "Batch released", entre otros. Esta exploración permitió capturar el núcleo operativo e IoT del laboratorio en su totalidad.


<img src="../assets/img/design-level-event-storming-step-1.png" alt="Bounded Context brainstorming" width="80%"/>

#### Paso 2: Timelines

Posteriormente, organizamos los eventos en líneas de tiempo para visualizar el flujo de interacciones y secuencias entre eventos. Se identificaron los siguientes flujos principales:

* **IAM & Security Flow:** gestión de identidad, roles, registro, inicio de sesión y desactivación de accesos del personal.
* **Laboratory Setup Flow:** configuración inicial del laboratorio, registro de personal, creación de catálogo de productos farmacéuticos y materias primas.
* **Equipment & IoT Configuration Flow:** registro de maquinaria industrial, configuración de parámetros BPM, vinculación de sensores IoT y alertas de calibración
* **Tracking & Telemetry Flow:** recepción continua de mediciones IoT, actualización de estado de los equipos y registro de historiales telemétricos.
* **Compliance & Alerting Flow:** configuración de umbrales de alerta, detección de anomalías, registro de eventos de cumplimiento y despacho de alertas de calidad.
* **Production Batch Flow:** creación de lotes, asignación de materia prima, procesamiento y decisión final de liberación (Release) o rechazo (Reject).
* **Reporting & Analytics Flow:** evaluación del desempeño productivo, generación de reportes BPM consolidados y generación de reportes de auditoría de equipos.
* **Subscription & Payments Flow:** selección de planes SaaS para el laboratorio y procesamiento de transacciones financieras.

Esta organización temporal facilitó la comprensión de dependencias y secuencias críticas entre la configuración humana y la automatización del sistema.

<img src="../assets/img/design-level-event-storming-step-11.png" alt="Bounded Context Timelines" width="80%"/>
<img src="../assets/img/design-level-event-storming-step-12.png" alt="Bounded Context Timelines" width="80%"/>
<img src="../assets/img/design-level-event-storming-step-13.png" alt="Bounded Context Timelines" width="80%"/>

#### Paso 3: Commands

En este paso definimos los comandos que los diferentes actores pueden ejecutar en el sistema. Los comandos representan las intenciones o acciones (en verbo imperativo) que mutan el estado de la aplicación y desencadenan los eventos en el dominio.

| Actor | Comandos |
|-------|----------|
| **QA Manager** | Assign Staff Responsibility, Deactivate User Access, Update Laboratory, Register Staff, Create Product, Create Raw Material, Register Equipment, Configure BPM, Link Sensor, Register Maintenance, Configure Alert Threshold, Acknowledge Deviation, Create Batch, Link Raw Material, Release Batch, Reject Batch, Generate Batch Report, Generate Compliance Report. |
| **Lab Operator** | Update Staff Profile, Record Raw Material Usage, Start Batch Processing. |
| **Auditor** | Generate Equipment Audit Report. |
| **IoT Sensor** | Record Measurement. |
| **System (QualiTrack)** | Detect Connection Loss, Evaluate Calibration Status, Update Equipment Status, Record Telemetry History, Trigger Deviation Alert, Record Compliance Event, Dispatch Quality Alert, Evaluate Production Performance. |
| **Payment System** | Process Payment. |

<img src="../assets/img/design-level-event-storming-step-21.png" alt="Bounded Context Commands" width="80%"/>
<img src="../assets/img/design-level-event-storming-step-22.png" alt="Bounded Context Commands" width="80%"/>
<img src="../assets/img/design-level-event-storming-step-23.png" alt="Bounded Context Commands" width="80%"/>

#### Paso 4: Policies and Actors

En este paso identificamos las políticas de negocio (reglas WHEN/THEN) y los actores responsables de cada flujo. Las políticas representan las reglas automáticas que el sistema ejecuta en respuesta a ciertos eventos, garantizando el estricto cumplimiento de las normativas de manufactura sin depender de la intervención humana constante.

Las políticas identificadas fueron:

* **WHEN** raw material stock reaches the minimum threshold THEN trigger a minimum stock alert.
* **WHEN** an equipment's calibration date is near THEN trigger a calibration due alert internally.
* **WHEN** an IoT device loses connection THEN trigger an equipment connection lost alert.
* **WHEN** telemetry is received THEN evaluate the measurement against the configured BPM parameters automatically.
* **WHEN** a non-critical deviation is detected THEN trigger a warning alert and dispatch a quality alert to the QA Manager.
* **WHEN** a critical deviation is detected in telemetry THEN block the batch automatically and register a compliance event.
* **WHEN** a batch is successfully released with a digital signature THEN auto-generate the immutable batch record PDF.
* **WHEN** a QA Manager deactivates a user access THEN revoke all permissions immediately while keeping the audit log intact.

Estas políticas permiten automatizar procesos críticos del sistema, reduciendo drásticamente el error humano y asegurando respuestas oportunas ante situaciones de riesgo que podrían comprometer la calidad de los medicamentos.

<img src="../assets/img/design-level-event-storming-step-31.png" alt="Bounded Context Policies" width="80%"/>
<img src="../assets/img/design-level-event-storming-step-32.png" alt="Bounded Context Policies" width="80%"/>

#### 4.6.1.1. Candidate Context Discovery

Una vez identificados los eventos, flujos, comandos y políticas del dominio, se procedió al descubrimiento de contextos candidatos. Esta etapa permitió agrupar elementos relacionados según su cohesión funcional y sus reglas de negocio compartidas, delimitando áreas específicas como configuración de equipos, telemetría IoT, cumplimiento normativo (compliance), gestión de lotes y reportes de auditoría. De esta manera, el equipo logró estructurar el dominio de QualiTrack en contextos con responsabilidades claramente diferenciadas y alineadas a los módulos desarrollados en el código fuente.

#### Paso 5: Read Models

Los Read Models representan las vistas de consulta que los actores utilizan para tomar decisiones dentro del sistema. De acuerdo con el modelado, se identificaron las siguientes vistas principales mediante los post-its verdes:

* **User Directory & role Permissions:** utilizado en el flujo de IAM para consultar accesos y permisos.
* **Equipment Inventory & Connectivity Status:** utilizado para verificar el inventario de maquinaria y su estado de conexión a la red.
* **Laboratory Infrastructure Map:** permite consultar el estado y la configuración de la infraestructura del laboratorio.
* **Sensor Config:** vista utilizada para consultar los parámetros de configuración de los dispositivos IoT.
* **Real-time Telemetry Dashboard:** panel para el monitoreo continuo y en vivo de los datos transmitidos por los sensores.
* **Batch Genealogy & Material Stock:** utilizado para consultar la trazabilidad del lote y el inventario disponible de materias primas.
* **Performance Metrics & KPI Summary:** dashboard utilizado por Analytics para visualizar el rendimiento y los indicadores clave.
* **Plan Options:** permite consultar los planes de suscripción disponibles antes de realizar el pago.

<img src="../assets/img/design-level-event-storming-step-41.png" alt="Bounded Context Models" width="80%"/>
<img src="../assets/img/design-level-event-storming-step-42.png" alt="Bounded Context Models" width="80%"/>
<img src="../assets/img/design-level-event-storming-step-43.png" alt="Bounded Context Models" width="80%"/>

#### Paso 6: External Systems

En este paso identificamos los sistemas externos que interactúan con el dominio, pero que están fuera del control directo del sistema (representados con post-its rosados).

* **SendGrid / Email Service:** sistema externo utilizado en el contexto de IAM para el envío de correos, como la recuperación de contraseñas.
* **IoT Hub:** infraestructura externa encargada de gestionar la conectividad y recepción de datos de los equipos.
* **Cloudinary (Product Assets):** servicio en la nube utilizado para el almacenamiento de imágenes y recursos del laboratorio.
* **OneSignal:** sistema externo utilizado para el envío de notificaciones push ante eventos de cumplimiento y alertas.
* **Audit Vault (Secure Storage):** servicio de almacenamiento seguro utilizado para resguardar los registros de auditoría inmutables.
* **Stripe / Payment Gateway:** pasarela de pagos externa utilizada para procesar las transacciones de las suscripciones.

<img src="../assets/img/design-level-event-storming-step-51.png" alt="Bounded Context External" width="80%"/>
<img src="../assets/img/design-level-event-storming-step-52.png" alt="Bounded Context External" width="80%"/>
<img src="../assets/img/design-level-event-storming-step-53.png" alt="Bounded Context External" width="80%"/>

#### Paso 7: Add Aggregates

En este paso identificamos los Aggregates, que representan los objetos de dominio centrales que agrupan entidades relacionadas y se tratan como una sola unidad. Cada aggregate (post-it amarillo grande) actúa como el punto central alrededor del cual giran los eventos y comandos:

* **User Security:** centraliza la lógica de autenticación y roles de usuario.
* **Equipment:** gestiona el estado y ciclo de vida de la maquinaria industrial.
* **Maintenance Log:** controla los registros de mantenimiento de los equipos.
* **Laboratory:** agrupa la configuración y catálogo central del laboratorio.
* **Telemetry Log:** concentra el registro histórico de las mediciones capturadas.
* **Compliance Event:** gestiona las incidencias y alertas de cumplimiento normativo.
* **Audit Trail:** centraliza la traza inmutable de acciones críticas en el sistema.
* **Analytics Engine:** procesa la información para la generación de métricas.
* **Manufacturing Batch:** controla el ciclo de vida de producción de un lote.
* **Inventory Ledger:** gestiona el registro exacto de los movimientos de inventario.

<img src="../assets/img/design-level-event-storming-step-61.png" alt="Bounded Context aggregates" width="80%"/>
<img src="../assets/img/design-level-event-storming-step-62.png" alt="Bounded Context aggregates" width="80%"/>
<img src="../assets/img/design-level-event-storming-step-63.png" alt="Bounded Context aggregates" width="80%"/>

#### Paso 8: Bounded Contexts

Finalmente, definimos los Bounded Contexts que agrupan los flujos relacionados en contextos delimitados con responsabilidades claras. Según las agrupaciones finales del tablero, se definieron los siguientes:

| Bounded Context | Descripción de Componentes Clave |
|-----------------|----------------------------------|
| **BC: IAM** | Contiene el Aggregate `User Security` y las políticas de sesión. |
| **BC: Equipment Management** | Agrupa los Aggregates `Equipment` y `Maintenance Log`, junto con IoT Hub. |
| **BC: Laboratory Management** | Contiene el Aggregate `Laboratory`. |
| **BC: Tracking (IoT)** | Agrupa el Aggregate `Telemetry Log` y las pantallas de monitoreo en tiempo real. |
| **BC: Compliance & Alerting** | Contiene los Aggregates `Compliance Event` y `Audit Trail`. |
| **BC: Reporting & Audit** | Contiene el Aggregate `Analytics Engine` y el almacenamiento seguro. |
| **BC: Batch Management** | Agrupa los Aggregates `Manufacturing Batch` e `Inventory Ledger`. |
| **BC: Context Shared** | Contiene el Aggregate `Billing Account` y la integración para cobros. |

<img src="../assets/img/bc-iam.png" alt="Bounded Context iam" width="80%"/>
<img src="../assets/img/bc-em.png" alt="Bounded Context em" width="80%"/>
<img src="../assets/img/bc-lm.png" alt="Bounded Context lm" width="80%"/>
<img src="../assets/img/bc-tracking.png" alt="Bounded Context tracking" width="80%"/>
<img src="../assets/img/bc-ca.png" alt="Bounded Context ca" width="80%"/>
<img src="../assets/img/bc-ra.png" alt="Bounded Context ra" width="80%"/>
<img src="../assets/img/bc-bm.png" alt="Bounded Context bm" width="80%"/>
<img src="../assets/img/bc-shared.png" alt="Bounded Context shared" width="80%"/>


## 4.6.2. Software Architecture Context Diagram

En este nivel se presenta una vista de alto nivel de la arquitectura, donde el foco está
en el sistema de software QualiTrack como una "caja negra" y en las interacciones que
mantiene con sus usuarios y con otros sistemas externos.

El context diagram muestra al **QualiTrack Software System** como un recuadro en el
centro, rodeado por los principales actores y sistemas con los que se comunica:

- **QA Manager / Supervisor:** usuario interno responsable de gestionar el laboratorio,
registrar y liberar lotes de producción, configurar parámetros BPM de los equipos,
supervisar el dashboard de telemetría en tiempo real y generar reportes de auditoría
para DIGEMID.

- **Lab Operator:** usuario operativo que monitorea el estado de los equipos industriales
durante los turnos de producción, recibe alertas de desviación de parámetros BPM y
registra observaciones sobre el proceso de fabricación.

- **IoT Sensors / Industrial Equipment:** sistema externo compuesto por los sensores
conectados a los equipos industriales del laboratorio (autoclaves, medidores de pH,
termómetros, sensores de presión). No representan un actor humano, sino un sistema
automatizado que envía telemetría de variables críticas de forma continua hacia
QualiTrack mediante endpoints REST, sin intervención manual.

- **Email Notification Service:** servicio externo de correo electrónico utilizado para
enviar notificaciones transaccionales a los usuarios (alertas de desviación crítica,
confirmación de registro, alertas de calibración próxima a vencer, reportes de auditoría
generados).

- **PDF Generation Service:** servicio externo utilizado para generar los reportes de
trazabilidad inmutables en formato PDF no editable, garantizando la integridad documental
requerida para las inspecciones de DIGEMID.

En el diagrama se representan las relaciones entre estos elementos. El QA Manager y el
Lab Operator interactúan con QualiTrack a través de la interfaz web. Los sensores IoT
envían telemetría entrante hacia QualiTrack de forma automática. QualiTrack se encarga
de orquestar las integraciones salientes con los servicios externos (notificaciones por
correo y generación de reportes PDF). Esta vista permite entender el alcance del sistema,
los límites de responsabilidad y el ecosistema en el que se inserta QualiTrack antes de
entrar a detalles de implementación.

<img src="../assets/img/ContextDiagram-v2.svg" alt="Context Diagram" width="100%"/>

---

## 4.6.3. Software Architecture Container Diagrams

En el nivel de contenedores, la atención se desplaza desde "quién usa el sistema" hacia
"cómo se organiza internamente el sistema en aplicaciones y fuentes de datos". El
container diagram muestra los elementos de alto nivel de la arquitectura de QualiTrack,
sus responsabilidades principales y la forma en que se comunican entre sí y con los
sistemas externos.

La arquitectura lógica de QualiTrack se estructura en los siguientes contenedores:

- **Landing Page:** aplicación web estática que presenta la propuesta de valor de
QualiTrack, informa sobre las funcionalidades de la plataforma y los planes de
suscripción disponibles para laboratorios farmacéuticos. Está desarrollada con
tecnologías web estándar (HTML, CSS y JavaScript). Cuando el usuario desea acceder a
la aplicación, delega la entrega del bundle al servidor web.

- **Web Application:** servidor web implementado con **Nginx** que actúa como servidor
de archivos estáticos. Recibe la delegación de la Landing Page y entrega el bundle
compilado de la SPA Angular al navegador del usuario. Este contenedor separa la
responsabilidad de servir el contenido estático de la lógica de negocio del backend.

- **QualiTrack Web Client Application (SPA):** aplicación web principal implementada en
**Angular** que corre directamente en el navegador del usuario. Una vez entregado el
bundle por el Web Application, el QA Manager y el Lab Operator interactúan con esta
SPA para gestionar el laboratorio, monitorear la telemetría IoT, administrar lotes y
generar reportes de auditoría. Concentra la lógica de presentación para los contextos
de IAM, Laboratory Management, Equipment Management, Tracking, Compliance & Alerting,
Batch Management, Reporting & Audit y Shared.

- **API Application:** backend implementado con **Spring Boot**, que expone una API REST
y encapsula la lógica de negocio, reglas de validación de parámetros BPM y orquestación
de procesos de compliance farmacéutico. Este contenedor agrupa los módulos backend por
contexto (IAM Backend, Laboratory Management Backend, Equipment Management Backend,
Tracking Backend, Compliance & Alerting Backend, Batch Management Backend,
Reporting & Audit Backend y Shared Backend).

- **Database:** base de datos relacional **MySQL**, donde se persiste la información
estructurada del sistema: laboratorios, equipos, configuraciones BPM, mediciones de
telemetría, lotes de producción, eventos de compliance, alertas, materias primas,
reportes de auditoría y usuarios.

En el diagrama se observa que:

- Los usuarios acceden primero a la **Landing Page**, que delega la entrega del bundle
al **Web Application (Nginx)**, el cual sirve el bundle compilado al navegador del
usuario como la **SPA Angular**.
- La **SPA** se comunica exclusivamente con la **API Application** mediante peticiones
**HTTP/HTTPS** con mensajes **JSON**, siguiendo un estilo REST.
- La **API Application** persiste y consulta datos en la **Database** mediante JDBC y
mapeo objeto–relacional.
- Los **sensores IoT** envían telemetría entrante directamente a la **API Application**
mediante peticiones POST al endpoint de ingesta, sin intervención de la SPA.
- La **API Application** interactúa con los sistemas externos salientes: el **Email
Notification Service** para el envío de alertas críticas y notificaciones, y el **PDF
Generation Service** para la generación de reportes de trazabilidad inmutables.

Esta vista permite apreciar cómo se distribuyen las responsabilidades entre la capa de
presentación (Landing Page, Web Application y SPA), la capa de lógica de negocio
(API Application) y la capa de persistencia (Database), así como las principales
decisiones tecnológicas adoptadas para cada contenedor.

<img src="../assets/img/ContainerDiagram-v2.svg" alt="Container Diagram" width="100%"/>

---

## 4.6.4. Software Architecture Components Diagrams

En el nivel de componentes se detalla la descomposición interna de los contenedores,
mostrando los bloques estructurales que conforman cada uno y las relaciones entre ellos.
Dado que la **SPA** y la **Database** ya fueron descritas en otros apartados mediante
diagramas de clases frontend y de base de datos, en esta sección se pone especial énfasis
en el contenedor **API Application**, donde reside la mayor parte de la lógica de negocio
y las reglas de compliance farmacéutico.

El component diagram de la **API Application** agrupa la arquitectura interna siguiendo
los bounded contexts definidos en el dominio de QualiTrack. Cada módulo backend representa
un componente principal dentro del contenedor:

- **IAM Backend:** se encarga de la autenticación, gestión de usuarios, roles, permisos
y validaciones de acceso a la plataforma. Garantiza que cada usuario acceda únicamente
a las funcionalidades habilitadas según su rol (QA Manager, Lab Operator, Auditor).
Se integra con el Email Notification Service para el envío de correos de activación de
cuenta y recuperación de contraseña.

- **Laboratory Management Backend:** gestiona la información institucional del laboratorio,
el catálogo de productos farmacéuticos, el inventario de materias primas y el personal
técnico. Sirve como base de datos maestra para los demás contextos del sistema.

- **Equipment Management Backend:** administra el ciclo de vida de los equipos
industriales, la vinculación con sensores IoT, la configuración de parámetros BPM por
variable y el historial de mantenimientos y calibraciones.

- **Tracking Backend:** implementa el endpoint de ingesta de telemetría que recibe los
datos enviados automáticamente por los sensores IoT (sistemas externos, no actores
humanos). Almacena las mediciones de temperatura, presión y pH asociadas al equipo y
lote correspondiente, y las pone a disposición del contexto de Compliance & Alerting
para su evaluación inmediata mediante eventos de dominio.

- **Compliance & Alerting Backend:** constituye el núcleo de inteligencia de QualiTrack.
Evalúa cada medición recibida desde Tracking comparándola con los parámetros BPM
configurados, clasifica las desviaciones por severidad, genera alertas inmediatas y
bloquea automáticamente los lotes no conformes. Se integra con el Email Notification
Service para el envío de alertas críticas al QA Manager y al operario asignado.

- **Batch Management Backend:** gestiona el ciclo de vida completo de los lotes de
producción, desde su creación hasta su liberación digital o rechazo documentado.
Registra la trazabilidad de materias primas utilizadas y mantiene el historial inmutable
de cada lote. Recibe eventos de bloqueo automático desde el Compliance & Alerting
Backend cuando se detecta una desviación crítica.

- **Reporting & Audit Backend:** genera reportes de trazabilidad en PDF para lotes
individuales y periodos de tiempo, exporta logs de eventos de equipos y calcula KPIs
de calidad. Se integra con el PDF Generation Service para producir documentos inmutables
listos para inspecciones de DIGEMID.

- **Shared Backend:** provee componentes compartidos, value objects comunes (LabId,
UserId, DateRange, Quantity), clases base auditables, eventos de dominio y mecanismos
de infraestructura transversales utilizados por todos los módulos backend.

En el diagrama se refleja cómo:

- La **SPA** consume los servicios expuestos por cada módulo backend a través de la
**API Application**, utilizando endpoints REST específicos por contexto.
- Los **sensores IoT** envían telemetría entrante directamente al **Tracking Backend**
mediante HTTP POST, sin pasar por la SPA.
- El **Tracking Backend** y el **Compliance & Alerting Backend** trabajan en conjunto
como el core domain del sistema: el primero ingesta las mediciones y publica el evento
`MeasurementRecorded`; el segundo lo evalúa y, si detecta una desviación crítica,
publica el evento `BatchBlocked` hacia el Batch Management Backend.
- El **Reporting & Audit Backend** se integra con el **PDF Generation Service** externo
para garantizar la inmutabilidad de los reportes de auditoría.
- El **IAM Backend** se integra con el **Email Notification Service** para el envío de
notificaciones de activación de cuenta y recuperación de contraseña.
- Todos los módulos backend reutilizan capacidades comunes provistas por el
**Shared Backend**, favoreciendo la consistencia, la reutilización y la reducción de
duplicación de código entre contextos.

De esta forma, los component diagrams complementan los diagramas de clases del frontend,
backend y base de datos, mostrando cómo los contenedores se descomponen en componentes
coherentes con los bounded contexts del dominio farmacéutico y cómo estos colaboran entre
sí para implementar la funcionalidad completa de QualiTrack.

<img src="../assets/img/ComponentDiagram-v2.svg" alt="Component Diagram" width="100%"/>

## 4.7. Software Object-Oriented Design

En esta sección se presenta el diseño orientado a objetos del sistema QualiTrack, el cual
desarrolla con mayor detalle la implementación interna de los componentes identificados
en los diagramas C4 del apartado 4.6. A partir de los contenedores y componentes definidos
en Structurizr (Frontend SPA, API Application y Database), se derivan diagramas de clases
específicos para cada bounded context del dominio, con el objetivo de mostrar:

- Cómo se modelan las entidades, agregados, servicios y recursos en el backend para cada
contexto de dominio farmacéutico.
- Cómo se estructuran los componentes de presentación, estado e infraestructura en el
frontend Angular.
- Cómo se reflejan estos modelos en el diseño de la base de datos relacional MySQL.

De esta forma, el diseño orientado a objetos enlaza el nivel arquitectónico (C4 Model)
con el nivel de implementación, permitiendo verificar coherencia entre bounded contexts,
responsabilidades de cada módulo y decisiones de diseño técnico.

## 4.7.1. Class Diagrams

En esta subsección se presentan los diagramas de clases que detallan la estructura interna de los principales componentes del frontend y backend para cada bounded context. Estos diagramas complementan al Component Diagram de la **Web Application**, al Component Diagram de la **API Application** y a los contenedores definidos en Structurizr, proporcionando una vista centrada en clases, atributos, métodos y relaciones entre componentes de presentación, stores de aplicación, servicios de infraestructura, recursos, ensambladores, modelos de dominio, entidades persistentes, repositorios, controladores y servicios de aplicación.

A nivel de **frontend**, se modelan las clases en función de los módulos y vistas que consumen los servicios expuestos por la API:

- **Frontend completo**: muestra la organización general de la capa de presentación de QualiTrack, incluyendo la configuración global de la aplicación, rutas principales, vistas generales, stores, APIs, endpoints, assemblers y bounded contexts frontend.
- **IAM Frontend**: incluye los componentes relacionados con autenticación, registro, recuperación de contraseña, gestión de usuarios, asignación de roles, manejo de sesión y guards de autorización.
- **Laboratory Management Frontend**: detalla las clases que gestionan la información institucional del laboratorio, personal técnico, catálogo de productos farmacéuticos, inventario de materias primas y control de stock bajo.
- **Equipment Management Frontend**: modela los componentes responsables del registro de equipos industriales, configuración de parámetros BPM, historial de mantenimientos y alertas de calibración.
- **Tracking Frontend**: presenta los componentes de interfaz que construyen el dashboard de telemetría, gráficos de historial, filtros de mediciones, estado de equipos conectados y detección visual de anomalías.
- **Compliance & Alerting Frontend**: modela las vistas de alertas BPM, historial de desviaciones, detalle de alertas, resolución de incidencias y configuración de preferencias de notificación.
- **Batch Management Frontend**: detalla los componentes para la gestión de lotes de producción, trazabilidad de materias primas, liberación digital, rechazo documentado y consulta del detalle de lote.
- **Reporting & Audit Frontend**: presenta los componentes del dashboard KPI, análisis de tendencias de desviación, generación de reportes y visualización de logs de auditoría.
- **Subscription & Billing Frontend**: integra las clases relacionadas con planes de suscripción, selección de plan, creación de sesión de checkout, pagos, resumen de facturación y estados de pago.
- **Shared Frontend**: agrupa componentes reutilizables, clases base, recursos compartidos, assemblers genéricos, endpoints base, layout principal, toolbar, selector de idioma, dashboard general y vistas comunes.

A nivel de **backend**, los diagramas de clases reflejan la implementación detallada de los módulos definidos como componentes en la **API Application**:

- **Backend completo**: ilustra la estructura general de la capa de dominio, aplicación, infraestructura e interfaces REST, mostrando cómo se distribuyen las clases entre los distintos bounded contexts modelados como componentes.
- **IAM Backend**: muestra las clases relacionadas con usuarios, roles, credenciales, autenticación, autorización, manejo de tokens y repositorios de identidad.
- **Laboratory Management Backend**: incluye agregados y entidades relacionados con laboratorios, personal técnico, productos farmacéuticos y materias primas, junto con sus servicios, comandos, consultas, repositorios y recursos REST.
- **Equipment Management Backend**: detalla las clases responsables del ciclo de vida de equipos industriales, configuración de parámetros BPM y registros de mantenimiento.
- **Tracking Backend**: define las clases utilizadas para gestionar telemetría de equipos, mediciones, historial de variables y estados de conectividad.
- **Compliance & Alerting Backend**: modela las clases responsables de eventos de compliance, alertas de desviación, preferencias de notificación y flujos de resolución o reconocimiento de incidencias.
- **Batch Management Backend**: contiene las clases asociadas con lotes de producción, uso de materias primas, firmas digitales, registros de rechazo y cambios de estado del lote.
- **Reporting & Audit Backend**: modela las clases utilizadas para dashboards KPI, métricas, tendencias de desviación, reportes de auditoría y logs de acciones.
- **Subscription & Billing Backend**: integra las clases relacionadas con planes de suscripción, suscripciones activas, pagos, sesiones de checkout, integración con Stripe, eventos de suscripción y webhooks de pago.
- **Shared Backend**: concentra clases base, resultados de aplicación, errores, entidades auditables, configuraciones compartidas, ensambladores comunes y patrones transversales usados por los demás módulos.

---

### Diagrama de clases del frontend

#### Diagrama del frontend completo:

![Frontend Completo](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/ClosedSource-Frontend/main/docs/diagrams/qualitrack/qualitrack-frontend-diagram.puml&fmt=svg&v=4)

<h3><strong>Diagrama del frontend dividido por contextos:</strong></h3>

<h4>iam frontend:</h4>
<p><strong>Responsabilidad:</strong> Maneja las vistas de autenticación, registro de usuarios, recuperación de contraseña, administración de usuarios, asignación de roles, manejo de sesión y control de acceso mediante guards de autenticación y autorización.</p>

![IAM Frontend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/ClosedSource-Frontend/main/docs/diagrams/iam/iam-frontend-diagram.puml&fmt=svg&v=4)

<h4>laboratory management frontend:</h4>
<p><strong>Responsabilidad:</strong> Maneja las vistas de perfil institucional del laboratorio, registro y edición de información del laboratorio, catálogo de productos farmacéuticos, inventario de materias primas, control de bajo stock y gestión de personal técnico.</p>

![Laboratory Management Frontend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/ClosedSource-Frontend/main/docs/diagrams/laboratory/laboratory-frontend-diagram.puml&fmt=svg&v=4)

<h4>equipment management frontend:</h4>
<p><strong>Responsabilidad:</strong> Maneja las vistas de listado, registro y detalle de equipos industriales, configuración de parámetros BPM, historial de mantenimientos, registro de mantenimientos y alertas de calibración asociadas al estado operativo de los equipos.</p>

![Equipment Management Frontend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/ClosedSource-Frontend/main/docs/diagrams/equipment/equipment-frontend-diagram.puml&fmt=svg&v=4)

<h4>tracking frontend:</h4>
<p><strong>Responsabilidad:</strong> Maneja las vistas del dashboard de telemetría, gráficos de historial de mediciones, consulta de variables críticas, panel de estado de equipos conectados y visualización de información operativa en tiempo real.</p>

![Tracking Frontend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/ClosedSource-Frontend/main/docs/diagrams/tracking/tracking-frontend-diagram.puml&fmt=svg&v=4)

<h4>compliance & alerting frontend:</h4>
<p><strong>Responsabilidad:</strong> Maneja las vistas de alertas de desviación BPM, historial de alertas, eventos de compliance, preferencias de notificación, seguimiento de incidencias y control de cumplimiento regulatorio.</p>

![Compliance Alerting Frontend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/ClosedSource-Frontend/main/docs/diagrams/ca/ca-frontend-diagram.puml&fmt=svg&v=4)

<h4>batch management frontend:</h4>
<p><strong>Responsabilidad:</strong> Maneja las vistas de listado, creación y detalle de lotes de producción, trazabilidad de materias primas utilizadas, liberación digital de lotes y rechazo documentado de lotes no conformes.</p>

![Batch Management Frontend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/ClosedSource-Frontend/main/docs/diagrams/batch/batch-frontend-diagram.puml&fmt=svg&v=4)

<h4>reporting & audit frontend:</h4>
<p><strong>Responsabilidad:</strong> Maneja las vistas del KPI dashboard, métricas operativas, tendencias de desviaciones, generación de reportes, consulta de logs de auditoría y visualización de información para seguimiento regulatorio.</p>

![Reporting Audit Frontend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/ClosedSource-Frontend/main/docs/diagrams/ra/ra-frontend-diagram.puml&fmt=svg&v=4)

<h4>subscription & billing frontend:</h4>
<p><strong>Responsabilidad:</strong> Maneja las vistas de planes de suscripción, selección de plan, proceso de checkout, creación de sesión de pago, resumen de facturación, pagos asociados a la suscripción y visualización del estado de la transacción.</p>

![Subscription Billing Frontend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/ClosedSource-Frontend/main/docs/diagrams/subscription/subscription-frontend-diagram.puml&fmt=svg&v=4)

<h4>shared frontend:</h4>
<p><strong>Responsabilidad:</strong> Maneja los componentes comunes, layouts, toolbar, selector de idioma, vistas generales, clases base, recursos compartidos, assemblers, servicios reutilizables y patrones transversales usados por los demás módulos frontend.</p>

![Shared Frontend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/ClosedSource-Frontend/main/docs/diagrams/shared/shared-frontend-diagram.puml&fmt=svg&v=4)

<div style="page-break-after: always;"></div>

---

### Diagrama de clases del backend

#### Diagrama del backend completo:

![Backend Completo](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/qualitrack/qualitrack-backend-diagram.puml&fmt=svg&v=4)

<h3><strong>Diagrama del backend dividido por contextos:</strong></h3>

<h4>iam backend:</h4>
<p><strong>Responsabilidad:</strong> Maneja usuarios, autenticación, autorización, roles, credenciales, servicios de aplicación, repositorios de identidad y recursos REST asociados al control de acceso.</p>

![IAM Backend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/iam/iam-backend-diagram.puml&fmt=svg&v=4)

<h4>laboratory management backend:</h4>
<p><strong>Responsabilidad:</strong> Maneja la gestión institucional del laboratorio, catálogo de productos farmacéuticos, inventario de materias primas, personal técnico, comandos, consultas, repositorios y endpoints REST del contexto.</p>

![Laboratory Management Backend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/laboratory/laboratory-backend-diagram.puml&fmt=svg&v=4)

<h4>equipment management backend:</h4>
<p><strong>Responsabilidad:</strong> Maneja el ciclo de vida de equipos industriales, configuración de parámetros BPM, registros de mantenimiento, entidades de persistencia, repositorios y controladores REST del contexto.</p>

![Equipment Management Backend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/equipment/equipment-backend-diagram.puml&fmt=svg&v=4)

<h4>tracking backend:</h4>
<p><strong>Responsabilidad:</strong> Maneja la ingesta, registro, consulta e historial de telemetría de equipos, incluyendo mediciones, estados de conectividad, puntos históricos y servicios de consulta para dashboards.</p>

![Tracking Backend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/tracking/tracking-backend-diagram.puml&fmt=svg&v=4)

<h4>compliance & alerting backend:</h4>
<p><strong>Responsabilidad:</strong> Maneja la evaluación de mediciones contra parámetros BPM, generación de alertas de desviación, eventos de compliance, preferencias de notificación, reconocimiento de alertas y resolución de incidencias.</p>

![Compliance Alerting Backend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/ca/ca-backend-diagram.puml&fmt=svg&v=4)

<h4>batch management backend:</h4>
<p><strong>Responsabilidad:</strong> Maneja el ciclo de vida de lotes de producción, trazabilidad de materias primas, liberación digital, rechazo documentado, firmas digitales y registros asociados al estado del lote.</p>

![Batch Management Backend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/batch/batch-backend-diagram.puml&fmt=svg&v=4)

<h4>reporting & audit backend:</h4>
<p><strong>Responsabilidad:</strong> Maneja la generación de reportes, logs de auditoría, dashboards KPI, métricas de calidad, tendencias de desviación y servicios de consulta para seguimiento operativo y regulatorio.</p>

![Reporting Audit Backend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/ra/ra-backend-diagram.puml&fmt=svg&v=4)

<h4>subscription & billing backend:</h4>
<p><strong>Responsabilidad:</strong> Maneja planes de suscripción, suscripciones activas, pagos, sesiones de checkout, integración con Stripe, webhooks, activación, cancelación y consulta de estados de facturación.</p>

![Subscription Billing Backend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/subscription/subscription-backend-diagram.puml&fmt=svg&v=4)

<h4>shared backend:</h4>
<p><strong>Responsabilidad:</strong> Maneja clases base, resultados de aplicación, errores compartidos, entidades auditables, configuraciones transversales, ensambladores comunes y patrones reutilizables por los demás módulos backend.</p>

![Shared Backend](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/shared/shared-backend-diagram.puml&fmt=svg&v=4)

<div style="page-break-after: always;"></div>

---

## 4.8. Database Design

### 4.8.1. Database Diagrams

En esta sección se presenta el diseño de la base de datos relacional de QualiTrack, organizado por bounded context. Cada contexto gestiona su propio conjunto de tablas, garantizando la separación de responsabilidades y la alineación con la arquitectura DDD definida en los apartados anteriores. La base de datos está implementada en **MySQL** y sus tablas principales incluyen campos de auditoría como `created_at` y `updated_at`, con el objetivo de mantener trazabilidad sobre la creación y actualización de los registros.

Los diagramas de base de datos se organizan en los siguientes contextos:

- **Base de datos completa**: muestra la integración general de las tablas principales de todos los bounded contexts.
- **IAM Database**: contiene las tablas relacionadas con usuarios, roles y asignaciones de rol.
- **Laboratory Management Database**: contiene laboratorios, regulaciones, personal técnico, productos farmacéuticos y materias primas.
- **Equipment Management Database**: contiene equipos industriales, configuraciones de parámetros BPM y registros de mantenimiento.
- **Batch Management Database**: contiene lotes, uso de materias primas, firmas digitales y registros de rechazo.
- **Tracking Database**: contiene telemetría de equipos, estados de conectividad, mediciones e historial de variables.
- **Compliance & Alerting Database**: contiene alertas de desviación, eventos de compliance y preferencias de notificación.
- **Reporting & Audit Database**: contiene reportes de auditoría, logs, dashboards KPI, métricas y tendencias de desviación.
- **Subscription & Billing Database**: contiene planes de suscripción, suscripciones, pagos, estados de facturación e identificadores asociados al proveedor de pago.

#### Diagrama de base de datos completo:

![Database](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/qualitrack/qualitrack-database-diagram.puml&fmt=svg&v=4)

<h3><strong>Diagrama de base de datos dividido por contextos:</strong></h3>

<h4>iam base de datos:</h4>
<p><strong>Responsabilidad:</strong> Gestiona las tablas de usuarios, roles y asignaciones de roles utilizadas para autenticación, autorización y control de acceso dentro de la plataforma.</p>

![IAM Database](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/iam/iam-database-diagram.puml&fmt=svg&v=4)

<h4>laboratory management base de datos:</h4>
<p><strong>Responsabilidad:</strong> Gestiona la información institucional de laboratorios, regulaciones aplicables, personal técnico, catálogo de productos farmacéuticos y materias primas disponibles.</p>

![Laboratory Database](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/laboratory/laboratory-database-diagram.puml&fmt=svg&v=4)

<h4>equipment management base de datos:</h4>
<p><strong>Responsabilidad:</strong> Gestiona equipos industriales, configuraciones de parámetros BPM, rangos permitidos de operación y registros de mantenimiento asociados a cada equipo.</p>

![Equipment Database](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/equipment/equipment-database-diagram.puml&fmt=svg&v=4)

<h4>batch management base de datos:</h4>
<p><strong>Responsabilidad:</strong> Gestiona lotes de producción, uso de materias primas, firmas digitales de liberación y registros de rechazo documentado para mantener la trazabilidad del proceso productivo.</p>

![Batch Database](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/batch/batch-database-diagram.puml&fmt=svg&v=4)

<h4>tracking base de datos:</h4>
<p><strong>Responsabilidad:</strong> Gestiona la telemetría de equipos, estados de conectividad, mediciones de variables críticas e historial de valores registrados para análisis operativo.</p>

![Tracking Database](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/tracking/tracking-database-diagram.puml&fmt=svg&v=4)

<h4>compliance & alerting base de datos:</h4>
<p><strong>Responsabilidad:</strong> Gestiona alertas de desviación, eventos de compliance, estados de resolución, responsables de atención y preferencias de notificación por usuario.</p>

![Compliance Database](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/ca/ca-database-diagram.puml&fmt=svg&v=4)

<h4>reporting & audit base de datos:</h4>
<p><strong>Responsabilidad:</strong> Gestiona reportes generados, logs de auditoría, dashboards KPI, métricas de calidad, tendencias de desviación y puntos históricos para análisis regulatorio.</p>

![Reporting Database](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/ra/ra-database-diagram.puml&fmt=svg&v=4)

<h4>subscription & billing base de datos:</h4>
<p><strong>Responsabilidad:</strong> Gestiona planes de suscripción, suscripciones activas o históricas, pagos registrados, ciclos de facturación, estado de suscripción e identificadores de Stripe asociados al proceso de checkout.</p>

![Subscription Billing Database](https://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/ClosedSource-11848/qualitrack-platform/main/docs/diagrams/subscription/subscription-database-diagram.puml&fmt=svg&v=4)
