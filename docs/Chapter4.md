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
* **Primario (Azul QualiTrack):** var(--primary-color) (referencia principal).
* **Secundario (Azul Profundo):** var(--secondary-color) (para texto principal y elementos interactivos).
* **Terciario (Gris Oscuro):** var(--tertiary-color) (para texto secundario y detalles).
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

### 4.4.2. Web Applications Wireflow Diagrams

### 4.4.3. Web Applications Mock-ups

### 4.4.4. Web Applications User Flow Diagrams

## 4.5. Web Applications Prototyping

## 4.6. Domain-Driven Software Architecture

## 4.6.1. Design-Level Event Storming

Para identificar los eventos de dominio, es recomendable realizar una sesión de Event 
Storming. Esta técnica permite visualizar y comprender el flujo de eventos dentro del 
dominio, facilitando la identificación de los Bounded Contexts.

El desarrollo del proceso del Domain-Driven Design se realizó en la aplicación Miro: 
[https://shorturl.at/0eSVT]

---

### Bounded Context IAM

El bounded context IAM (Identity and Access Management) se encarga de la autenticación, 
autorización y gestión de credenciales dentro del ecosistema QualiTrack. Administra 
procesos como el registro de usuarios, inicio de sesión, recuperación de contraseñas y 
asignación de permisos según el rol (jefe de QA, operario, auditor). Su propósito es 
garantizar accesos seguros, confiables y alineados con las políticas de protección de la 
información regulatoria en toda la plataforma.

<img src="../assets/img/bc-iam.jpg" alt="Bounded Context IAM" width="80%"/>

---

### Bounded Context Laboratory Management

El bounded context Laboratory Management gestiona toda la información institucional del 
laboratorio farmacéutico dentro de QualiTrack: datos del laboratorio, normativas 
regulatorias aplicables, catálogo de productos farmacéuticos, materias primas y personal 
técnico. Administra la creación, actualización y mantenimiento de los datos base del 
laboratorio. Su propósito es centralizar la ficha institucional y servir como base para 
otros contextos como Equipment Management, Batch Management y Reporting & Audit.

<img src="../assets/img/bc-laboratory.jpg" alt="Bounded Context Laboratory Management" width="80%"/>

---

### Bounded Context Equipment Management

El bounded context Equipment Management gestiona el ciclo de vida completo de los equipos 
industriales del laboratorio: autoclaves, medidores de pH, termómetros y sensores de 
presión. Incluye el registro de equipos, la vinculación con sensores IoT, la configuración 
de parámetros BPM por variable, el registro de mantenimientos y el control de calibración. 
Se integra con Tracking para habilitar la recepción de telemetría y con Compliance & 
Alerting para aplicar los rangos configurados. Su propósito es asegurar que todos los 
equipos conectados estén correctamente identificados, calibrados y con parámetros de control 
actualizados.

<img src="../assets/img/bc-equipment.jpg" alt="Bounded Context Equipment Management" width="80%"/>

---

### Bounded Context Tracking (IoT)

El bounded context Tracking constituye uno de los núcleos del sistema QualiTrack. Captura, 
sincroniza y almacena la telemetría enviada por los sensores IoT vinculados a los equipos 
industriales. Registra variables críticas como temperatura, presión y pH en tiempo real, 
con marca de tiempo y asociación al equipo y lote correspondiente. Estos datos son enviados 
al contexto Compliance & Alerting para su evaluación normativa y a Reporting & Audit para 
análisis histórico. Su propósito es brindar monitoreo continuo y automático del estado 
operativo de los equipos de producción, eliminando la dependencia de registros manuales.

<img src="../assets/img/bc-tracking.jpg" alt="Bounded Context Tracking IoT" width="80%"/>

---

### Bounded Context Compliance & Alerting

El bounded context Compliance & Alerting es el otro núcleo estratégico de QualiTrack. 
Procesa, evalúa y clasifica cada medición recibida desde Tracking comparándola con los 
parámetros BPM configurados para el equipo correspondiente. Cuando detecta una desviación 
crítica, genera alertas inmediatas para el operario de turno, notifica al jefe de 
Aseguramiento de la Calidad y bloquea automáticamente el lote asociado, impidiendo su 
avance en la cadena de suministro. Administra también el historial de eventos de compliance 
y las preferencias de notificación de los usuarios. Su propósito es garantizar que ninguna 
desviación de los parámetros BPM pase desapercibida, protegiendo la integridad del producto 
y el cumplimiento normativo ante DIGEMID.

<img src="../assets/img/bc-compliance.jpg" alt="Bounded Context Compliance and Alerting" width="80%"/>

---

### Bounded Context Batch Management

El bounded context Batch Management representa el núcleo operativo de la gestión de 
producción en QualiTrack. Administra el ciclo de vida completo de cada lote farmacéutico: 
desde su creación y vinculación con materias primas y equipos, hasta su liberación digital 
mediante firma del jefe de QA o su rechazo documentado. Conecta flujos con Equipment 
Management para asociar equipos al lote, con Tracking para recibir telemetría vinculada, 
con Compliance & Alerting para gestionar bloqueos automáticos y con Reporting & Audit para 
la generación de registros inmutables. Su propósito es garantizar la trazabilidad completa 
de cada lote de producción, asegurando que toda decisión de liberación o rechazo quede 
registrada de forma inmutable y auditable.

<img src="../assets/img/bc-batch.jpg" alt="Bounded Context Batch Management" width="80%"/>

---

### Bounded Context Reporting & Audit

El bounded context Reporting & Audit recopila información de múltiples fuentes (Tracking, 
Compliance & Alerting, Batch Management, Equipment Management) para generar reportes de 
trazabilidad inmutables, logs de auditoría y visualizaciones de indicadores clave de 
calidad (KPIs). Permite la generación de reportes PDF no editables por lote o por periodo, 
la exportación de logs de eventos de equipos y el análisis de tendencias de desviaciones. 
Su propósito es ofrecer una capa de transparencia y evidencia documental que permita 
afrontar inspecciones de DIGEMID con toda la información consolidada, reduciendo el tiempo 
de preparación de auditorías en un 80%.

<img src="../assets/img/bc-reporting.jpg" alt="Bounded Context Reporting and Audit" width="80%"/>

---

### Bounded Context Shared

El bounded context Shared contiene los elementos reutilizables y transversales utilizados 
por todos los demás contextos de QualiTrack, como configuraciones globales, value objects 
comunes (LabId, UserId, DateRange, Quantity), clases base auditables, plantillas de 
eventos de dominio y políticas compartidas. Gestiona además el registro de tenants y la 
propagación de configuraciones por defecto a los contextos dependientes. Su propósito es 
evitar la duplicidad de lógica entre contextos, asegurar la coherencia de los datos 
compartidos y proveer una base técnica sólida y reutilizable para toda la arquitectura de 
QualiTrack.

<img src="../assets/img/b-c-shared.jpg" alt="Bounded Context Shared" width="80%"/>

### 4.6.2. Software Architecture Context Diagram

El diagrama de contexto de QualiTrack muestra a la plataforma como el sistema central que gestiona la calidad farmacéutica, integrando sensores IoT, monitoreo de variables, trazabilidad de lotes y soporte para auditorías. A su alrededor interactúan actores como el jefe de calidad, operarios, auditores y administradores, junto con sistemas externos que permiten su funcionamiento.

### 4.6.3. Software Architecture Container Diagrams

### 4.6.4. Software Architecture Components Diagrams

## 4.7. Software Object-Oriented Design

### 4.7.1. Class Diagrams

## 4.8. Database Design

### 4.8.1. Database Diagrams
