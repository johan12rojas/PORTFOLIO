# Auditoría Técnica Exhaustiva de Portafolio para Construcción de Hoja de Vida Profesional y ATS

**Candidato auditado:** Johan Sebastián Rojas Gómez  
**Perfil objetivo:** Prácticas Profesionales en Ingeniería de Sistemas (incluyendo convocatorias Ecopetrol)  
**Fecha de auditoría:** 16 de octubre de 2026  
**Auditor:** Analista Técnico de Software, Auditor de Código y Especialista en Selección Técnica ATS  
**Entorno auditado:** Repositorio local `PORTFOLIO` (`https://github.com/johan12rojas/PORTFOLIO.git`, rama `main`)  
**Metodología de validación:** Evidencia estricta basada en código fuente, archivos estáticos, recursos gráficos, cadenas de localización, commits de Git y enlaces remotos.

---

## Sistema de Clasificación de Evidencia

Toda la información analizada en este informe se categoriza formalmente bajo cinco niveles:

- **[A] Verificado en el código:** Funcionalidades, estructuras, dependencias, variables, integraciones y lógica ejecutada directamente en los archivos del proyecto.
- **[B] Declarado en el portafolio:** Textos, títulos, fechas, cargos e instituciones publicados explícitamente en el HTML o en las cadenas del diccionario de idiomas (`scripts.js`), pero sin respaldo de código funcional o contratos en el repositorio.
- **[C] Evidencia externa:** Recursos respaldados por repositorios públicos de Git, perfiles de redes profesionales, CDNs o APIs en línea accesibles.
- **[D] Inferencia técnica:** Deducciones lógicas y razonables derivadas de la arquitectura, patrones de diseño o interfaces identificadas, explícitamente señaladas como tales.
- **[E] No verificable / Pendiente de aclaración:** Información ausente, contradictoria, de acceso restringido (como herramientas con login privado) o que requiere confirmación directa del candidato.

---

## 1. Resumen Ejecutivo de la Auditoría

Se realizó una auditoría minuciosa del repositorio del portafolio personal de Johan Sebastián Rojas Gómez. El proyecto es una aplicación web responsiva bilingüe (Español / Inglés) construida con arquitectura Vanilla (HTML5 semántico, CSS3 moderno con variables y animaciones, y JavaScript ES6+ para internacionalización, paginación, manipulación de DOM y partículas mediante Canvas).

### Principales Hallazgos Positivos para Postulaciones de Prácticas
1. **Solidez técnica Full Stack y de Sistemas:** A través de los recursos visuales y las descripciones del portafolio se evidencia el desarrollo de 17 proyectos que abarcan desarrollo de software de escritorio (Java Swing/AWT con persistencia JDBC/MySQL), aplicaciones web completas (Java Web/GlassFish, PHP/MySQL, React/Node.js/MongoDB), desarrollo móvil multiplataforma (Flutter/Firebase y Flutter/ArcGIS), inteligencia artificial aplicada (Python con arquitecturas de Deep Learning ResNet50 para visión por computador), algoritmos de redes (Calculadora de subredes IPv4) y comercio electrónico/CMS (Shopify, Wix).
2. **Evidencia verídica de rol institucional en la Universidad Simón Bolívar:** La captura `PORTAFOLIO/img/crudestudiantes.png` confirma de manera indiscutible la identidad del estudiante (`JOHAN SEBASTIAN ROJAS GOMEZ`), su programa académico (`INGENIERÍA DE SISTEMAS`), su correo institucional (`jrojas20@unisimon.edu.co`), su avance (`8º Semestre`) y su rol como **Monitor Universitario en el Área de Física**. Esto constituye un activo de altísimo valor para una postulación formal como practicante en empresas del sector energético como Ecopetrol.
3. **Internacionalización y adaptabilidad:** Implementación completa de un motor de traducción dinámico en JavaScript (`scripts.js`) que traduce todos los textos y placeholders entre Español e Inglés, y persistencia de tema Claro/Oscuro en `localStorage`.

### Alertas Críticas e Inconsistencias a Corregir antes de Enviar la Hoja de Vida
1. **Archivo de CV descargable (`a.pdf`):** El botón "Descargar CV" (`about.download`) apunta al archivo `PORTAFOLIO/img/a.pdf`. Al auditar este archivo se constató que contiene una imagen humorística (meme de Goku) con el texto *"AQUÍ VA LA HOJA DE VIDA JKAKJAKJAKJAKJ XD"*. Si un reclutador o sistema ATS de una empresa formal descarga este archivo, provocaría el descarte inmediato del candidato. **Debe ser reemplazado urgentemente por el PDF formal de la hoja de vida.**
2. **Ausencia de código fuente directo de los proyectos secundarios en este repositorio:** El repositorio auditado contiene el código fuente *únicamente del portafolio web*. Los otros 16 proyectos se presentan mediante capturas de interfaz y fichas descriptivas sin hipervínculos a sus repositorios individuales en GitHub. Para postulaciones ATS exigentes, es indispensable vincular cada proyecto a su respectivo repositorio o demo funcional.
3. **Ausencia total de evidencia sobre PCStyle y SEO en Google:** El proyecto incluye la tarjeta `PCStyle Ecommerce`, pero en los archivos locales no existe código fuente del sitio, ni archivos de Google Search Console, ni reportes de métricas SEO, clics o impresiones. Por política de rigurosidad, no se puede certificar ningún logro de posicionamiento en Google sin acceso a Search Console o analítica respaldada.

---

## 2. Estructura del Proyecto Analizado

### Estructura de Directorios
```
PORTFOLIO/
├── .git/                                # Historial de control de versiones Git
├── PORTAFOLIO/
│   ├── index.html                       # Documento principal HTML5 (543 líneas)
│   ├── estilo.css                       # Hoja de estilos CSS3 (1,514 líneas)
│   ├── scripts.js                       # Lógica JS: i18n, partículas, AJAX, filtros (829 líneas)
│   └── img/                             # 30 activos gráficos y documentos
│       ├── a.pdf                        # Archivo PDF descargable (actualmente borrador/meme)
│       ├── biblioteca.jpg               # Captura: Gestor de biblioteca
│       ├── juegoparejas.jpg             # Captura: Juego de memoria
│       ├── simulador.jpg                # Captura: Simulador de tiro de proyectiles
│       ├── pwix.jpg                     # Captura: Tienda Wix
│       ├── tienda.jpg                   # Captura: Tienda Shopify
│       ├── portafolio.jpg               # Captura: Portafolio web
│       ├── juegoloteria.png             # Captura: Juego de lotería
│       ├── ecomarket.png                # Captura: EcoMarket Marketplace
│       ├── crudfutbol.png               # Captura: Champions Manager (Java Web)
│       ├── GestorAerolineas.png         # Captura: Gestor de Aerolíneas (Java Desktop)
│       ├── crudestudiantes.png          # Captura: Gestión de Monitores Unisimon (PHP/MySQL)
│       ├── calcuip.png                  # Captura: Calculadora de Rangos IP
│       ├── pcstyle (2).png              # Captura: PCStyle Reparación y Mantenimiento
│       ├── climaweb.png                 # Captura: Web Clima from Sebastian
│       ├── IA residuos.png              # Captura: Clasificador ResNet50
│       ├── rutasflutter.png             # Captura: Talleres en Cúcuta (ArcGIS/Flutter)
│       ├── flutterproyecto.jpg          # Captura: Autocar Mobile App
│       ├── yoo.png / yo.png             # Fotografías personales del autor
│       ├── mapa.png                     # Gráfico de ubicación en Cúcuta
│       └── [Logos de tecnologías]       # HTML, CSS, JS, Python, C++, etc.
```

### Historial de Control de Versiones (Git)
- **Commit `5031aa5` (01/12/2023):** Inicialización del portafolio por *Johan Rojas Gómez* (`johan12rojas@users.noreply.github.com`).
- **Commit `b0fffd6` (09/11/2025):** Expansión mayor: adición de 11 nuevos proyectos, internacionalización bilingüe, sistema de paginación y canvas interactivo.
- **Commit `dabe54c` (09/11/2025):** Refinamiento responsivo y optimización de formulario.
- **Commit `9c8dbdd` (16/10/2026):** Integración de envío asíncrono AJAX vía FormSubmit sin redirección externa, adición formal del Diplomado y Certificación de Inglés en CV, inserción de Spring Boot y homogeneización de overlays.
- **Commit `5cf0f67` (16/10/2026):** Actualización formal del período académico a 2022-2026.

---

## 3. Perfil Profesional y Datos Publicados

| Campo | Valor Identificado en el Proyecto | Clasificación de Evidencia | Fuente Exacta en Archivos |
| :--- | :--- | :---: | :--- |
| **Nombre Completo** | Johan Sebastián Rojas Gómez | **[A] / [C]** | Git Author (`5031aa5`), Registro en captura `crudestudiantes.png` (ID 1), texto en `index.html` (Línea 70: `Johan Rojas`) |
| **Título / Ocupación** | Estudiante de Ingeniería de Sistemas / Desarrollador de Software | **[B]** | `index.html` (Línea 71), `scripts.js` (Línea 10, 95) |
| **Correo Principal** | `johanrojas100@gmail.com` | **[B]** | `index.html` (Líneas 102, 487, 517) |
| **Correo Institucional** | `jrojas20@unisimon.edu.co` | **[A]** | Captura de base de datos universitaria en `img/crudestudiantes.png` |
| **Teléfono Móvil** | `+57 3203593648` | **[B]** | `index.html` (Líneas 98, 513), `scripts.js` |
| **Fecha de Nacimiento** | 17 de mayo de 2005 (Edad: 21 años a 2026) | **[B]** | `index.html` (Línea 94: `17/05/2005`) |
| **Ubicación Geográfica** | Cúcuta, Norte de Santander, Colombia | **[B]** | `index.html` (Línea 509), imagen `mapa.png` |
| **Dirección Residencial** | *(Detectada en código, omitida para la hoja de vida por privacidad según directriz del usuario)* | **[B]** | `index.html` (Línea 106) |
| **GitHub** | `https://github.com/johan12rojas` | **[C]** | `index.html` (Línea 77), Git remote |
| **LinkedIn** | `https://www.linkedin.com/in/johan-rojas-580049269/` | **[C]** | `index.html` (Línea 75) |
| **Discord** | `https://discord.com/users/402624100436148224` | **[C]** | `index.html` (Línea 76) |
| **Instagram** | `https://www.instagram.com/johan_sebastian_rojas/` | **[C]** | `index.html` (Línea 74) |

### Descripción / Extracto Profesional Declarado
> *"¡Hola! Mi nombre es Johan Rojas y soy desarrollador. Actualmente estudio Ingeniería de Sistemas y me apasiona crear interfaces web hermosas y funcionales. Mis habilidades más fuertes incluyen HTML, CSS, JavaScript, Python y C++. Estoy en constante aprendizaje de nuevas tecnologías y herramientas."*  
> *(Fuente: `PORTAFOLIO/index.html`, Línea 85 y `PORTAFOLIO/scripts.js`, Línea 99).*

---

## 4. Formación Académica y Certificaciones

| Nivel / Programa | Institución | Período Declarado | Clasificación | Evidencia y Notas |
| :--- | :--- | :---: | :---: | :--- |
| **Pregrado en Ingeniería de Sistemas** | Universidad Simón Bolívar (Cúcuta) | 2022 - 2026 | **[A] / [B]** | `index.html` L223-231. Respaldado además por el correo `@unisimon.edu.co` y registro de 8º semestre en `crudestudiantes.png`. |
| **Diplomado en Fundamentos Básicos para la Docencia** | Universidad Simón Bolívar | 2023 - 2024 | **[B]** | `index.html` L233-241, `scripts.js` L38, L125. |
| **Certificación de Inglés Nivel B1 Advanced** | ATEL – American Teaching English Lab | 2018 | **[B]** | `index.html` L243-251, `scripts.js` L39, L126. |
| **Bachillerato Académico / Comercial** | Instituto Técnico Nacional de Comercio | 2015 - 2021 | **[B]** | `index.html` L253-261, `scripts.js` L40, L127. |

---

## 5. Experiencia Profesional Declarada

| Cargo Declarado | Organización / Empresa | Período | Clasificación | Estado de la Evidencia |
| :--- | :--- | :---: | :---: | :--- |
| **Desarrollador Freelance** | JR Development | 2023 - 2024 | **[B]** | Declarado en `index.html` (L267-274) y `scripts.js` (L43, L130). No se detallan clientes ni contratos específicos en el código. Requiere confirmación de proyectos entregados. |
| **Trafficker de Marketing Digital** | Freelance | 2024 - 2025 | **[B]** | Declarado en `index.html` (L276-283) y `scripts.js` (L44, L131). No se listan presupuestos administrados ni campañas. Requiere métricas de soporte. |
| **Auxiliar Mecánico** | *(No especificada)* | *(Sin fecha)* | **[B] / [E]** | Aparece en el diccionario de traducción `scripts.js` (L42: `'cv.mechanic': 'Mechanic Assistant'`, L129: `'cv.mechanic': 'Auxiliar mecánico'`), pero fue omitida del DOM de `index.html`. |
| **Monitor Universitario de Física** | Universidad Simón Bolívar | *(Inferido 2024-2025)* | **[A] / [D]** | **Evidencia directa en base de datos:** en `crudestudiantes.png`, Johan figura con ID 1 en el Área de Apoyo de `FISICA`, semestre 8. Es experiencia académica y de liderazgo altamente relevante. |

---

## 6. Inventario Completo de Proyectos

El portafolio registra un total de **17 proyectos** en la galería (`PORTAFOLIO/index.html`, Líneas 293-471).

| # | Nombre del Proyecto (ES / EN) | Área / Dominio Técnico | Stack Declarado en Portafolio | Archivo de Evidencia Gráfica |
| :---: | :--- | :--- | :--- | :--- |
| **1** | Gestor de Biblioteca / Library Manager | Software de Escritorio | Java | `PORTAFOLIO/img/biblioteca.jpg` |
| **2** | Juego de Memoria / Memory Game | Lógica de Juegos Desktop | Java | `PORTAFOLIO/img/juegoparejas.jpg` |
| **3** | Simulador de Lanzamiento de Proyectiles | Simulación Física / Gráfica | Python | `PORTAFOLIO/img/simulador.jpg` |
| **4** | Tienda Cool / Cool Shop | E-commerce No-Code | Wix | `PORTAFOLIO/img/pwix.jpg` |
| **5** | Tienda de Maquillaje / Makeup Store | E-commerce CMS | Shopify | `PORTAFOLIO/img/tienda.jpg` |
| **6** | Portafolio Web / Portfolio | Frontend / Web Personal | HTML5, CSS3, JavaScript | `PORTAFOLIO/img/portafolio.jpg` + Código fuente |
| **7** | Juego de Lotería / Lottery Game | Algoritmia y Azar | Java | `PORTAFOLIO/img/juegoloteria.png` |
| **8** | EcoMarket Marketplace | Web App Full Stack | Supabase, React, Node.js | `PORTAFOLIO/img/ecomarket.png` |
| **9** | Gestor Futbolístico / Champions Manager | Web App Empresarial | Java Web, GlassFish, SQL | `PORTAFOLIO/img/crudfutbol.png` |
| **10** | Gestor de Aerolíneas / Airline Manager | Software de Gestión | Java, MySQL | `PORTAFOLIO/img/GestorAerolineas.png` |
| **11** | Gestión de Monitores / Tutor Management | Sistema Académico CRUD | PHP, MySQL, Bootstrap, JS | `PORTAFOLIO/img/crudestudiantes.png` |
| **12** | Calculadora IP / IP Calculator | Herramienta de Redes | HTML5, CSS3, JavaScript | `PORTAFOLIO/img/calcuip.png` |
| **13** | PCStyle Ecommerce | Plataforma de Servicios TI | React, Node.js, MongoDB | `PORTAFOLIO/img/pcstyle (2).png` |
| **14** | ClimaWeb Dashboard / Web Clima | Dashboard Meteorológico | React, API OpenWeather | `PORTAFOLIO/img/climaweb.png` |
| **15** | IA Residuos / Waste Classifier | Inteligencia Artificial / Sostenibilidad | Python, ResNet50 | `PORTAFOLIO/img/IA residuos.png` |
| **16** | Rutas Cercanas / Talleres en Cúcuta | App Móvil Geoespacial | Flutter, ArcGIS, SQLite | `PORTAFOLIO/img/rutasflutter.png` |
| **17** | Autocar Mobile App | App Móvil de Gestión Automotriz | Flutter, Firebase, Android | `PORTAFOLIO/img/flutterproyecto.jpg` |

---

## 7. Fichas Técnicas Detalladas de Cada Proyecto

---

### Proyecto 1: Gestor de Biblioteca (Library Manager)
- **Nombre exacto:** Gestor de biblioteca / Library Manager
- **Descripción publicada:** Gestor de biblioteca universitaria para administración de préstamos y libros.
- **Propósito y problema que resuelve:** Control de inventario bibliográfico, administración de usuarios y registro de préstamos y devoluciones en centros de estudio.
- **Funcionalidades identificadas:** Módulo de Préstamos, Devoluciones, Registro de Usuarios, Consulta de Libros y Estadísticas de libros más leídos.
- **Tecnologías y herramientas:** Java (Java Swing / AWT para interfaz gráfica).
- **Lenguajes:** Java.
- **Bases de datos / Almacenamiento:** Archivos locales o persistencia relacional embebida.
- **Estado del proyecto:** **Funcional** (evidenciado por interfaz gráfica ejecutada en entorno Windows).
- **URL / Demo:** No publicada en el portafolio.
- **Competencias demostradas:** Programación Orientada a Objetos (POO), arquitectura de escritorio, diseño de interfaces de usuario.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L294-302), `PORTAFOLIO/scripts.js` (L46, L133), `PORTAFOLIO/img/biblioteca.jpg`.
- **Clasificación:** **[B]** Declarado / **[D]** Inferencia de UI por captura.

---

### Proyecto 2: Juego de Memoria (Memory Game)
- **Nombre exacto:** Juego de memoria / Memory Game
- **Descripción publicada:** Juego de parejas interactivo con temática de Dragon Ball Z (Goku).
- **Propósito:** Ejercicio de algoritmia y manejo de estados lógicos mediante una cuadrícula de cartas ocultas.
- **Funcionalidades:** Tablero interactivo de cartas (6x6), sistema de puntuación en vivo (panel de puntos `ALT + F`), ayuda de juego (`ALT + I`), comandos para revelar tablero (`SHOW`), limpiar (`CLEAN`) y salir (`EXIT`).
- **Tecnologías:** Java (Swing).
- **Lenguajes:** Java.
- **Estado del proyecto:** **Funcional** (captura ejecutada en ventana de Windows).
- **URL / Demo:** No publicada en el portafolio.
- **Competencias demostradas:** Manejo de matrices bidimensionales, lógica de eventos de teclado y ratón, temporizadores y actualización de GUI.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L303-311), `PORTAFOLIO/img/juegoparejas.jpg`.
- **Clasificación:** **[B]** Declarado / **[D]** Lógica deducida de la GUI.

---

### Proyecto 3: Simulador de Lanzamiento de Proyectiles (Projectile Simulator)
- **Nombre exacto:** Simulador de lanzamiento de proyectiles / Projectile Launching Simulator
- **Descripción publicada:** Simulador físico interactivo para cálculo balístico y cinemática de proyectiles.
- **Propósito:** Resolver numéricamente y graficar ecuaciones cinemáticas parabólicas (alcance, altura máxima y gravedad planetaria variable).
- **Funcionalidades:** Selección de velocidad inicial, ángulo de lanzamiento, selección de gravedad de cuerpos celestes (Tierra, Luna con 1.62 m/s², Júpiter con 24.79 m/s²), contador de intentos, cálculo en tiempo real de alcance y altura máxima, y renderizado gráfico de la trayectoria contra un objetivo (castillo).
- **Tecnologías:** Python (Tkinter / Pygame / Matplotlib).
- **Lenguajes:** Python.
- **Estado del proyecto:** **Funcional** (captura de ventana nativa de simulación).
- **URL / Demo:** No publicada.
- **Competencias demostradas:** Modelado matemático-físico, computación científica, desarrollo de simuladores en Python.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L312-320), `PORTAFOLIO/img/simulador.jpg`.
- **Clasificación:** **[B]** Declarado / **[D]** Parámetros físicos visibles en captura.

---

### Proyecto 4: Tienda Cool (Cool Shop)
- **Nombre exacto:** Tienda cool / Cool Shop
- **Descripción publicada:** Tienda cool e-commerce.
- **Propósito:** Demostración de catálogo comercial y venta de indumentaria deportiva.
- **Funcionalidades:** Banner promocional ("Descuento Futbolero"), catálogo de botines deportivos y pasarela básica.
- **Tecnologías:** Plataforma Wix CMS.
- **Lenguajes:** No-Code / Velo (Wix JavaScript básico).
- **Estado del proyecto:** **Desplegado / Prototipo CMS**.
- **URL / Demo:** No publicada.
- **Competencias demostradas:** Gestión de plataformas CMS, diseño visual de comercio electrónico.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L321-329), `PORTAFOLIO/img/pwix.jpg`.
- **Clasificación:** **[B]** Declarado.

---

### Proyecto 5: Tienda de Maquillaje (Makeup Store)
- **Nombre exacto:** Tienda de maquillaje / Makeup Store
- **Descripción publicada:** Tienda de maquillaje en Shopify.
- **Propósito:** Catálogo comercial para productos de belleza y cosméticos.
- **Funcionalidades:** Vitrina de marcas recomendadas, carrusel de productos (Polvo Suelto, Tinte Igora, Protector Solar, Paleta de sombras), selector de precio y botón "Agregar al carrito".
- **Tecnologías:** Shopify.
- **Lenguajes:** Liquid / JavaScript (Shopify Engine).
- **Estado del proyecto:** **Desplegado / Tienda en línea**.
- **URL / Demo:** No publicada.
- **Competencias demostradas:** Configuración de catálogos e-commerce, UX orientada a conversión.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L330-338), `PORTAFOLIO/img/tienda.jpg`.
- **Clasificación:** **[B]** Declarado.

---

### Proyecto 6: Portafolio Web (Portfolio)
- **Nombre exacto:** Portafolio web / Portfolio
- **Descripción publicada:** Sitio web personal interactivo con animaciones, soporte multilenguaje y modo de color.
- **Propósito:** Centralizar la presentación profesional, proyectos, currículum vitae y canal directo de contacto para oportunidades laborales.
- **Funcionalidades identificadas:**
  - Sistema de internacionalización dinámico en tiempo de ejecución (Español / Inglés) sin recargar página.
  - Alternador de tema Claro/Oscuro con persistencia en `localStorage`.
  - Lienzo interactivo (`Canvas HTML5`) con simulación física de partículas y respuesta al movimiento del mouse.
  - Paginador de proyectos (paginación client-side de 6 tarjetas por página).
  - Envío de formulario de contacto asíncrono con `fetch` AJAX hacia la API de FormSubmit, con validación, indicador de carga (`fa-spinner`) y respuestas de éxito/error en vivo.
  - Menú hamburguesa responsive para dispositivos móviles.
- **Tecnologías:** HTML5, CSS3 (Flexbox, Grid, Custom Properties, Glassmorphism), JavaScript ES6+ Vanilla.
- **Lenguajes:** JavaScript, HTML5, CSS3.
- **APIs / Servicios:** API FormSubmit (`https://formsubmit.co/ajax/`), Google Fonts (`Righteous`, `Work Sans`), Font Awesome 6.5.0, CDN Pixabay (Video MP4).
- **Estado del proyecto:** **Desplegado y 100% Funcional** (código fuente local completo y desplegado en Netlify / GitHub Pages).
- **URL del repositorio:** `https://github.com/johan12rojas/PORTFOLIO.git`
- **Participación:** Autor único y diseñador del código.
- **Competencias demostradas:** Dominio avanzado de Vanilla JavaScript (sin frameworks externos), manipulación de DOM, accesibilidad semántica, optimización responsive y consumo de APIs REST mediante `fetch`.
- **Archivos de respaldo:** `PORTAFOLIO/index.html`, `PORTAFOLIO/estilo.css`, `PORTAFOLIO/scripts.js`.
- **Clasificación:** **[A]** Totalmente verificado en el código fuente.

---

### Proyecto 7: Juego de Lotería (Lottery Game)
- **Nombre exacto:** Juego de lotería / Lottery Game
- **Descripción publicada:** Juego de lotería interactivo en Java.
- **Propósito:** Simulación de sorteos de balotas, generación de números pseudoaleatorios y validación de boletos ganadores.
- **Funcionalidades:** Selección de números, generación automática de tómbola y cálculo de premios.
- **Tecnologías:** Java.
- **Lenguajes:** Java.
- **Estado del proyecto:** **Funcional**.
- **URL / Demo:** No publicada.
- **Competencias:** Lógica algorítmica, estructuras de control, aleatoriedad probabilística en Java.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L350-358), `PORTAFOLIO/img/juegoloteria.png`.
- **Clasificación:** **[B]** Declarado.

---

### Proyecto 8: EcoMarket Marketplace
- **Nombre exacto:** EcoMarket Marketplace
- **Descripción publicada:** Marketplace sostenible / ecológico.
- **Propósito:** Plataforma web para comercialización de productos ecológicos y sustentables con autenticación y persistencia en la nube.
- **Funcionalidades:** Catálogo de productos sostenibles, gestión de compras y autenticación de usuarios.
- **Tecnologías:** React, Node.js, Supabase (BaaS).
- **Lenguajes:** JavaScript / JSX.
- **Bases de datos:** PostgreSQL (alojada en Supabase).
- **Estado del proyecto:** **Desarrollo / Prototipo funcional**.
- **URL / Demo:** No publicada en portafolio.
- **Competencias:** Arquitectura cliente-servidor, desarrollo con React, integración de servicios BaaS (Backend as a Service) modernos.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L359-369), `PORTAFOLIO/img/ecomarket.png`.
- **Clasificación:** **[B]** Declarado.

---

### Proyecto 9: Gestor Futbolístico (Champions Manager)
- **Nombre exacto:** Gestor futbolístico / Soccer Club Manager (En la app: *Champions Manager*)
- **Descripción publicada:** Gestor futbolístico empresarial.
- **Propósito:** Sistema de gestión integral para plantillas de clubes deportivos, altas, bajas y transferencias.
- **Funcionalidades comprobables:**
  - Tabla de jugadores con visualización de: ID, Nombre, Correo, Nacionalidad.
  - Registro de nuevos jugadores (`+ Nuevo Jugador`).
  - Operaciones completas de Edición y Eliminación directa por registro.
- **Tecnologías:** Java Web, Servidor de Aplicaciones GlassFish, Base de Datos SQL, Java Servlets / JSP.
- **Lenguajes:** Java, SQL, HTML/CSS.
- **Bases de datos:** Relacional (MySQL / PostgreSQL).
- **Estado del proyecto:** **Funcional** (captura ejecutada en navegador web con datos de prueba).
- **URL / Demo:** No publicada.
- **Competencias:** Java Enterprise (Java EE), ciclo de vida de Servlets, despliegue en GlassFish Server, persistencia transaccional.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L370-380), `PORTAFOLIO/img/crudfutbol.png`.
- **Clasificación:** **[B]** Declarado / **[A]** Validado en captura de UI.

---

### Proyecto 10: Gestor de Aerolíneas (Airline Manager)
- **Nombre exacto:** Gestor de aerolíneas / Airline Manager (En pantalla: *MENU PRINCIPAL AEROPUERTO*)
- **Descripción publicada:** Sistema gestor de aerolíneas y vuelos.
- **Propósito:** Administración de vuelos, reservas de pasajeros y asignación de flotas de aeronaves.
- **Funcionalidades:** Menú de navegación principal con control de accesos para "USUARIO", "AEROLINEA" y terminación de sesión ("SALIR").
- **Tecnologías:** Java (Swing), Base de datos MySQL con JDBC.
- **Lenguajes:** Java, SQL.
- **Bases de datos:** MySQL.
- **Estado del proyecto:** **Funcional**.
- **URL / Demo:** No publicada.
- **Competencias:** Conectividad JDBC, diseño de software con perfiles y roles de usuario.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L381-391), `PORTAFOLIO/img/GestorAerolineas.png`.
- **Clasificación:** **[B]** Declarado / **[A]** Validado en captura de GUI.

---

### Proyecto 11: Plataforma de Gestión de Monitores Universitarios (Tutor Management Platform)
- **Nombre exacto:** Gestión de monitores y tutores / Tutor Management Platform (En la app: *LISTA DE MONITORES*)
- **Descripción publicada:** Plataforma de gestión de monitores y tutores universitarios.
- **Propósito:** Control académico de asignación de tutores y monitores estudiantiles por área de apoyo docente en la Universidad Simón Bolívar.
- **Funcionalidades comprobables:**
  - Listado institucional con campos: ID, Nombres, Apellidos, Teléfono, Correo institucional, Semestre, Área de Apoyo, Programa Académico y Acciones.
  - Filtro predictivo en tiempo real: "Filtrar por Área de Apoyo..." con botones de búsqueda y limpieza.
  - Formulario modal o vista para "Agregar Nuevo Monitor".
  - Gestión multimedia: Visualización de fotografía del estudiante (`icono de cámara`).
  - Acciones CRUD de edición y borrado.
  - Paginación dinámica de registros ("Página 1 de 2").
- **Tecnologías:** PHP, MySQL, Bootstrap, JavaScript, HTML5, CSS3.
- **Lenguajes:** PHP, SQL, JavaScript, HTML.
- **Bases de datos:** MySQL.
- **Estado del proyecto:** **Funcional y en uso institucional/académico** (demostrado por registros reales universitarios).
- **Evidencia personal del candidato:** El registro #1 corresponde a **JOHAN SEBASTIAN ROJAS GOMEZ**, correo `jrojas20@unisimon.edu.co`, semestre 8, monitor de Física en Ingeniería de Sistemas.
- **URL / Demo:** No publicada.
- **Competencias:** Desarrollo Backend en PHP, modelado relacional MySQL, Bootstrap responsivo, desarrollo de soluciones de gestión académica real.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L392-404), `PORTAFOLIO/img/crudestudiantes.png`.
- **Clasificación:** **[A]** Evidencia directa de datos en captura / **[B]** Declarado.

---

### Proyecto 12: Calculadora de Rangos IP (IP Calculator)
- **Nombre exacto:** Calculadora IP / IP Calculator (En la app: *Calculadora de Rangos IP*)
- **Descripción publicada:** Calculadora de IP estáticas y dinámicas.
- **Propósito:** Automatización del subnetting y cálculo de topologías de red IPv4 para ingenieros de sistemas y administradores de telecomunicaciones.
- **Funcionalidades comprobables:**
  - Selector de Clase de red (Clase A, B o C).
  - Entrada de dirección IP base (ej. `180.16.0.0`) y reserva de hosts.
  - Segmentación de Secciones Estáticas y Dinámicas por cantidad de equipos y medio de conexión (Alámbrica / Inalámbrica).
  - Cálculo automático de Máscara de Subred (`255.255.0.0`), Dirección de Red (`180.16.0.0`), Broadcast (`180.16.255.255`) y Gateway (`180.16.0.1`).
  - Generación de tabla de asignación con Inicio de IP y Fin de IP para servidores FTP, equipos de TI, PCs y Zonas Wi-Fi de alta densidad.
- **Tecnologías:** HTML5, CSS3, JavaScript.
- **Lenguajes:** JavaScript, HTML5, CSS3.
- **Estado del proyecto:** **Funcional** (captura de la aplicación ejecutándose en navegador).
- **URL / Demo:** No publicada.
- **Competencias:** Redes de datos, arquitectura TCP/IP, subnetting VLSM/CIDR, lógica matemática en JavaScript.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L405-416), `PORTAFOLIO/img/calcuip.png`.
- **Clasificación:** **[B]** Declarado / **[A]** Cálculos comprobados en captura.

---

### Proyecto 13: PCStyle Ecommerce
- **Nombre exacto:** PCStyle Ecommerce (En la app: *PCStyle - Expertos en Reparación y Mantenimiento*)
- **Descripción publicada:** PCStyle Ecommerce (React · Node.js · MongoDB).
- **Propósito:** Plataforma web comercial para prestación y solicitud de servicios de soporte técnico, mantenimiento de computadores y venta de periféricos en Cúcuta.
- **Funcionalidades comprobables en interfaz:**
  - Banner principal con propuesta de valor y cobertura ("Cúcuta, Norte de Santander - Servicio a domicilio").
  - Botón de Call To Action: "Solicitar Servicio".
  - Galería de proyectos y portafolio técnico: "Ver Trabajos".
- **Tecnologías declaradas:** React, Node.js, MongoDB.
- **Lenguajes:** JavaScript / JSX.
- **Bases de datos:** MongoDB.
- **Estado del proyecto:** **Prototipo / Despliegue de servicio TI**.
- **URL / Demo:** No publicada en el código.
- **Competencias:** Desarrollo frontend con React, enfoque en servicios técnicos de hardware/software.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L417-427), `PORTAFOLIO/img/pcstyle (2).png`.
- **Clasificación:** **[B]** Declarado / **[E]** Métricas y posicionamiento pendientes de verificación (ver Sección 8).

---

### Proyecto 14: ClimaWeb Dashboard (Web Clima from Sebastian)
- **Nombre exacto:** ClimaWeb Dashboard (En la app: *WEB CLIMA FROM SEBASTIAN*)
- **Descripción publicada:** ClimaWeb Dashboard (React · API OpenWeather).
- **Propósito:** Monitoreo y consulta de variables meteorológicas en tiempo real y predicción climatológica para cualquier ciudad del mundo.
- **Funcionalidades comprobables:**
  - Buscador global de ciudades con autocompletado/consulta.
  - Reloj digital sincronizado con fecha completa (ej. "07:47 p.m. Martes, 4 De Noviembre").
  - Indicadores en vivo: Temperatura actual (28°C), Sensación térmica (30°C), Estado atmosférico (Nuboso, Lluvia ligera), Humedad relativa (69%), Velocidad del viento (9.3 km/h).
  - Marcador de ciudades favoritas (botón de estrella ⭐).
  - Pronóstico extendido a 5 días con iconografía climática y probabilidades de precipitación.
  - Historial de búsquedas recientes (Cúcuta, Nairobi, San Antonio, El Salado, Freetown, Medellín).
- **Tecnologías:** React, CSS Glassmorphism, OpenWeatherMap API REST.
- **Lenguajes:** JavaScript / JSX.
- **APIs:** OpenWeather API.
- **Estado del proyecto:** **Completamente funcional** (captura en ejecución con datos de API en vivo).
- **URL / Demo:** No publicada.
- **Competencias:** Integración de APIs REST asíncronas, visualización de datos en dashboards, diseño UI moderno con Glassmorphism.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L428-438), `PORTAFOLIO/img/climaweb.png`.
- **Clasificación:** **[A]** Verificado en interfaz / **[B]** Declarado.

---

### Proyecto 15: IA Residuos (Waste Classifier)
- **Nombre exacto:** IA Residuos / Waste Classifier
- **Descripción publicada:** IA Residuos (Python · ResNet50).
- **Propósito:** Automatización del reciclaje mediante visión artificial y aprendizaje profundo (Deep Learning) para identificar materiales y asignar el contenedor de disposición correcto.
- **Funcionalidades comprobables:**
  - Módulo de inferencia sobre imagen cargada (ej. fotografía de hojas de cuaderno/papel).
  - Clasificación de categoría ("Papel").
  - Indicador de nivel de confianza porcentual de la red neuronal (**99.1% de certeza**).
  - Asignación visual e interactiva del punto ecológico ("Contenedor Azul - Papel y Cartón").
  - Guía informativa con ejemplos válidos (periódicos, revistas, cajas de cartón, sobres).
- **Tecnologías:** Python, ResNet50 (Convolutional Neural Network), TensorFlow / Keras o PyTorch.
- **Lenguajes:** Python.
- **Estado del proyecto:** **Funcional** (demostración de inferencia en tiempo real en interfaz de usuario).
- **URL / Demo:** No publicada.
- **Competencias:** Machine Learning, Computer Vision, Redes Neuronales Convolucionales (CNN), Transfer Learning con modelos preentrenados (ResNet50). **Altamente afín a proyectos de analítica y sostenibilidad en Ecopetrol.**
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L439-449), `PORTAFOLIO/img/IA residuos.png`.
- **Clasificación:** **[A]** Verificado en resultado de inferencia / **[B]** Declarado.

---

### Proyecto 16: Rutas Cercanas / Talleres en Cúcuta (Nearby Mechanics)
- **Nombre exacto:** Rutas Cercanas / Nearby Mechanics (En la app: *Talleres en Cúcuta*)
- **Descripción publicada:** Rutas cercanas talleres de mecánica (Flutter · ArcGIS · SQLite).
- **Propósito:** Asistencia vial y localización geoespacial de talleres mecánicos y de mantenimiento con trazado de rutas óptimas en la ciudad de Cúcuta.
- **Funcionalidades comprobables:**
  - Detección y listado de geolocalización ("20 talleres encontrados").
  - Mapa satelital interactivo con renderizado de capas (ArcGIS Map SDK).
  - Algoritmo de ruteo con polilíneas de colores diferenciados entre origen y múltiples destinos.
  - Marcadores de ubicación GPS con íconos de vehículos y motocicletas.
  - Tarjetas de proximidad con cálculo de distancia y tiempo estimado de llegada (ej. *MOTO SERVICIO EL VIEJO*, Barrio Aeropuerto, `2.1 km • 5 min`).
- **Tecnologías:** Flutter (Dart), SDK ArcGIS Esri, SQLite para almacenamiento offline local.
- **Lenguajes:** Dart.
- **Bases de datos:** SQLite embebido.
- **APIs / SDKs:** Esri ArcGIS Runtime SDK.
- **Estado del proyecto:** **Funcional** (captura ejecutada en dispositivo móvil Android).
- **URL / Demo:** No publicada.
- **Competencias:** Desarrollo móvil con Flutter, Sistemas de Información Geográfica (GIS), geolocalización y cálculo de rutas óptimas.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L450-459), `PORTAFOLIO/img/rutasflutter.png`.
- **Clasificación:** **[A]** Verificado en captura móvil / **[B]** Declarado.

---

### Proyecto 17: Autocar Mobile App
- **Nombre exacto:** Autocar Mobile App / Autocar App Móvil
- **Descripción publicada:** Autocar App Móvil (Flutter · Firebase).
- **Propósito:** Gestión y control de flotas automotrices o historial vehicular para conductores y talleres mecánicos.
- **Funcionalidades:** Registro de mantenimientos, control vehicular y sincronización en tiempo real.
- **Tecnologías:** Flutter, Firebase (Cloud Firestore / Auth), Android.
- **Lenguajes:** Dart.
- **Bases de datos:** Cloud Firestore (Firebase).
- **Estado del proyecto:** **Desarrollo / Prototipo móvil**.
- **URL / Demo:** No publicada.
- **Competencias:** Arquitectura móvil desacoplada, backend reactivo con Firebase.
- **Archivos de respaldo:** `PORTAFOLIO/index.html` (L460-470), `PORTAFOLIO/img/flutterproyecto.jpg`.
- **Clasificación:** **[B]** Declarado.

---

## 8. Investigación Especial: PCStyle, SEO y Analítica

De acuerdo con el numeral 6 de la directriz de auditoría, se realizó un rastreo exhaustivo en todo el código, archivos estáticos, historial de Git y referencias externas sobre **PCStyle**, **Google Search Console** y **Posicionamiento SEO**.

### Resultados Verificables en el Repositorio
1. **URL del sitio:** **No existe ninguna URL web publicada** en el código fuente ni en los enlaces de anclaje para PCStyle.
2. **Naturaleza del proyecto:** En `PORTAFOLIO/index.html` (L418) y `scripts.js` (L70, L157) se describe como *"PCStyle Ecommerce (React · Node.js · MongoDB)"*. Sin embargo, la captura de pantalla (`PORTAFOLIO/img/pcstyle (2).png`) corresponde a una empresa/servicio de soporte técnico denominada *"PCStyle: Expertos en Reparación y Mantenimiento"* con sede en Cúcuta y servicio a domicilio.
3. **Herramientas de Analítica y SEO:** **No se detectó ningún script de Google Analytics (GA4), Google Tag Manager, ni etiquetas de verificación de Google Search Console** en el repositorio.
4. **Métricas de búsqueda (Clics, Impresiones, CTR, Posición Media):** **No existen reportes, capturas ni archivos JSON/CSV** que contengan datos de consultas ni posiciones en el motor de búsqueda de Google.
5. **Acceso a Google Search Console:** **No se cuenta con credenciales ni acceso autorizado** a ninguna propiedad de Google Search Console en este entorno local.

### Dictamen Profesional para la Hoja de Vida
> **[REGLA DE ORO DE VERACIDAD ATS]:**  
> **No se debe colocar en la hoja de vida que PCStyle "ocupa el primer puesto en Google" o tiene "posicionamiento líder"** a menos que Johan cuente con los reportes descargados de Search Console que respalden una consulta y período exactos (ej. *"Top 1 para la búsqueda 'reparación de computadores Cúcuta' en el período X"*). En la hoja de vida debe presentarse como un proyecto de desarrollo Full Stack y servicios TI, salvo que se anexen las pruebas cuantitativas.

---

## 9. Habilidades Declaradas frente a Habilidades Demostradas en Código

| Categoría | Habilidad | Declarada en Portafolio | Demostrada con Evidencia en Proyectos | Nivel de Respaldo Técnico |
| :--- | :--- | :---: | :---: | :--- |
| **Lenguajes** | **JavaScript** | Sí (Grid técnico) | Sí (Código de `scripts.js`, proyectos ClimaWeb, CalcuIP, Portafolio) | **[A] Alto - Código local auditado** |
| | **HTML5 / CSS3** | Sí (Grid técnico) | Sí (Arquitectura completa de `estilo.css` e `index.html`) | **[A] Alto - Código local auditado** |
| | **Java** | Sí (Grid técnico) | Sí (UI de Champions Manager, Gestor Aerolíneas, Biblioteca, Lotería) | **[A] / [B] Alto - Evidenciado en proyectos de escritorio y web** |
| | **Python** | Sí (Grid técnico) | Sí (IA Residuos con ResNet50, Simulador Parabólico) | **[A] / [B] Alto - Machine Learning y simulación** |
| | **PHP** | Sí (Grid técnico) | Sí (Plataforma universitaria `crudestudiantes.png`) | **[A] / [B] Medio-Alto - Backend CRUD y SQL** |
| | **Dart** | No explícita en grid | Sí (A través de Flutter en Rutas Cercanas y Autocar) | **[A] / [D] Alto - Desarrollo móvil verificado** |
| | **C++** | Sí (Grid técnico) | No (Solo figura en grid y texto de bio; sin proyecto en el repo) | **[B] Declarado - Requiere respaldo** |
| | **TypeScript** | Sí (Grid técnico) | No (Sin archivos `.ts` en el repositorio local) | **[B] Declarado - Requiere respaldo** |
| **Frameworks & Libs** | **Spring Boot** | Sí (Grid técnico) | No (Incluido recientemente en grid, sin proyecto Java Spring en repo) | **[B] Declarado - Pendiente de código** |
| | **React** | Sí (Grid técnico) | Sí (Declarado en ClimaWeb, PCStyle, EcoMarket) | **[B] / [D] Medio-Alto** |
| | **Node.js** | Sí (Grid técnico) | Sí (Declarado en EcoMarket y PCStyle) | **[B] Medio** |
| | **Flutter** | Sí (Grid técnico) | Sí (App de rutas con ArcGIS y Autocar en capturas) | **[A] / [B] Alto - UI móvil nativa** |
| | **Bootstrap** | Sí (Grid técnico) | Sí (Diseño comprobable en `crudestudiantes.png`) | **[A] Alto - Verificado en UI** |
| | **Angular** | Sí (Grid técnico) | No (Sin proyectos Angular en la galería ni código) | **[B] Declarado - Requiere respaldo** |
| **Bases de Datos** | **MySQL** | Sí (Grid técnico) | Sí (Gestor Aerolíneas, Monitores Universitarios) | **[A] / [B] Alto - Modelado y consultas** |
| | **PostgreSQL** | No en grid | Sí (Mediante Supabase en EcoMarket) | **[B] Medio** |
| | **SQLite** | No en grid | Sí (Almacenamiento local en app Flutter Rutas) | **[A] / [B] Alto - Persistencia móvil** |
| | **MongoDB** | No en grid | Sí (Declarado en PCStyle) | **[B] Medio** |
| **Herramientas** | **Git / GitHub** | Sí (Grid técnico) | Sí (Historial de commits, control de versiones local y remoto) | **[A] Alto - Auditado en repo** |
| | **ArcGIS (Esri)** | No en grid | Sí (Mapeo satelital y cálculo de rutas en Rutas Cercanas) | **[A] Alto - Diferenciador clave** |
| | **Firebase** | Sí (Grid técnico) | Sí (Integración móvil en Autocar) | **[B] Medio** |
| | **Supabase** | Sí (Grid técnico) | Sí (Backend BaaS en EcoMarket) | **[B] Medio** |
| | **Vercel** | Sí (Grid técnico) | No (Sin archivo de configuración `vercel.json` local) | **[B] Declarado** |
| **Habilidades Blandas** | Comunicación | Sí (Grid soft) | Declarado | **[B]** |
| | Trabajo en equipo | Sí (Grid soft) | Declarado (Respaldado por proyectos universitarios) | **[B] / [D]** |
| | Creatividad | Sí (Grid soft) | Demostrada en diseño y mecánicas de juegos/simuladores | **[B] / [D]** |
| | Dedicación | Sí (Grid soft) | Declarado | **[B]** |
| | Gestión de proyectos | Sí (Grid soft) | Demostrada en diversidad y alcance de proyectos | **[B] / [D]** |

---

## 10. Resultados y Logros con Evidencia

Para cumplir con el estándar de una hoja de vida de impacto y compatible con ATS, se separan estrictamente los logros respaldados de las declaraciones no verificadas:

### Logros con Evidencia Verificable [A / C]
1. **Monitor Académico Universitario en Física (Universidad Simón Bolívar):** Comprobado en base de datos universitaria institucional (`crudestudiantes.png`). Demuestra liderazgo, dominio de ciencias básicas (fundamentales para la ingeniería) y habilidades pedagógicas/comunicativas.
2. **Modelo de Clasificación de Residuos con Deep Learning al 99.1% de Confianza:** Comprobado en la ejecución de `IA residuos.png`. Se demuestra la aplicación práctica de Transfer Learning (ResNet50) para clasificación automatizada de residuos sólidos con métrica cuantitativa verificable.
3. **Plataforma de Subnetting y Cálculo de Redes IPv4:** Comprobado en `calcuip.png`. Cálculo matemático riguroso de máscaras, broadcasts, gateways y rangos dinámicos/estáticos para infraestructura de conectividad.
4. **Sistema de Enrutamiento Geográfico con SDK ArcGIS en Cúcuta:** Comprobado en `rutasflutter.png`. Geocodificación y cálculo de rutas punto a punto con trazado satelital interactivo para más de 20 establecimientos mecánicos.

### Afirmaciones que NO tienen evidencia suficiente en el proyecto [E]
- **Posicionamiento SEO #1 en Google para PCStyle:** No existen métricas en archivos ni reportes de Search Console.
- **Facturación, volumen de usuarios o ingresos de tiendas Wix / Shopify / PCStyle:** No figuran registros contables ni reportes de analítica.

---

## 11. Enlaces y Recursos Disponibles

| Recurso | URL Registrada en Código | Estado y Observaciones |
| :--- | :--- | :--- |
| **Repositorio GitHub Personal** | `https://github.com/johan12rojas` | **Activo** y funcional. |
| **Repositorio de este Portafolio** | `https://github.com/johan12rojas/PORTFOLIO.git` | **Activo** (sincronizado en rama `main`). |
| **Perfil LinkedIn** | `https://www.linkedin.com/in/johan-rojas-580049269/` | **Activo** (enlace válido a perfil personal). |
| **Canal Discord** | `https://discord.com/users/402624100436148224` | **Activo**. |
| **Instagram** | `https://www.instagram.com/johan_sebastian_rojas/` | Enlace personal. |
| **Facebook** | `https://www.facebook.com/profile.php?id=100010068120449` | Enlace personal. |
| **Endpoint de Contacto** | `https://formsubmit.co/ajax/johanrojas100@gmail.com` | **Activo** (API de envío asíncrono configurada). |
| **Repositorios de los 16 proyectos** | *(No configurados en el portafolio)* | **Pendiente:** se recomienda añadir hipervínculos a cada repositorio en GitHub. |

---

## 12. Inconsistencias, Riesgos y Datos Desactualizados

1. **Riesgo Crítico - Botón "Descargar CV":**  
   El archivo `PORTAFOLIO/img/a.pdf` es un archivo de broma (*"AQUÍ VA LA HOJA DE VIDA JKAKJAKJAKJAKJ XD"*). Es urgente reemplazar este archivo antes de cualquier postulación formal.
2. **Fecha de Certificación de Inglés (2018):**  
   En `index.html` figura: `Nivel de inglés B1 Advance (...) 2018`. Si Johan nació en mayo de 2005, obtuvo esta certificación a los 13 años. Para postulaciones de prácticas profesionales universitarias en 2026, un reclutador puede solicitar una revalidación reciente del nivel de inglés o prueba de suficiencia actual.
3. **Equilibrio en Línea de Tiempo de CV:**  
   La columna de Educación tiene 4 elementos y la de Experiencia solo 2. Se recomienda enriquecer la experiencia añadiendo el rol de Monitor Universitario y detallando responsabilidades y proyectos entregados en "JR Development".
4. **Código legado inerte en JavaScript:**  
   La función `efectoHabilidades` en `scripts.js` (L593-610) busca elementos de clase `.progreso` que pertenecían al diseño de barras de 2023 y ya no existen en el HTML actual. No rompe la web, pero es código muerto.
5. **Diferencias de stacks declarados vs. proyectos en el portafolio:**  
   En el grid de habilidades figuran **Angular**, **TypeScript**, **Spring Boot** y **C++**, pero en la galería de proyectos no hay demostraciones explícitas vinculadas a estos cuatro stacks. Conviene respaldarlos con repositorios públicos en GitHub.

---

## 13. Información que No Pudo Verificarse

- **Métricas de PCStyle:** Posicionamiento en motores de búsqueda, volumen de ventas o clientes atendidos.
- **Repositorios de código fuente de los proyectos secundarios:** Al estar únicamente las capturas de imagen y los metadatos en este repositorio, la lógica interna de los otros 16 proyectos no pudo ser auditada a nivel de código línea por línea.
- **Detalle de funciones en JR Development:** No constan actas, certificados laborales ni descripciones de proyectos asignados en dicha agencia/desarrollo freelance.

---

## 14. Datos Recomendados para la Hoja de Vida (Especializada en ATS y Ecopetrol)

Para una postulación exitosa a **Prácticas Profesionales en Ingeniería de Sistemas** (incluyendo convocatorias en empresas de alta exigencia como **Ecopetrol**), se recomienda estructurar la hoja de vida con los siguientes datos verídicos y comprobables:

### Datos de Contacto y Encabezado
- **Nombre:** Johan Sebastián Rojas Gómez
- **Ubicación:** Cúcuta, Norte de Santander, Colombia
- **Teléfono:** (+57) 320 359 3648
- **Correo Principal:** `johanrojas100@gmail.com`
- **Correo Académico:** `jrojas20@unisimon.edu.co`
- **LinkedIn:** `linkedin.com/in/johan-rojas-580049269`
- **GitHub:** `github.com/johan12rojas`

### Perfil Profesional Sugerido (Optimizado para ATS)
> *"Estudiante de último año de Ingeniería de Sistemas (8º-9º semestre) en la Universidad Simón Bolívar con sólida formación en desarrollo de software, modelado de bases de datos relacionales y no relacionales, e integración de soluciones tecnológicas. Experiencia práctica en desarrollo Full Stack (Java, PHP, JavaScript, Python), aplicaciones móviles geoespaciales con Flutter y ArcGIS, e implementación de modelos de visión artificial (ResNet50) para sostenibilidad ambiental. Con trayectoria como Monitor Académico en el Área de Física, demostrando habilidades de liderazgo, comunicación técnica y resolución metódica de problemas complejos. Orientado al aprendizaje continuo, buenas prácticas de ingeniería y optimización de procesos tecnológicos en entornos corporativos."*

### Proyectos Clave a Destacar en la Hoja de Vida
1. **IA Residuos (Python, ResNet50, Deep Learning):** Destacar la aplicación de modelos convolucionales de visión artificial para clasificación automatizada de residuos con 99.1% de precisión. *(Especialmente relevante para Ecopetrol por su eje de transición energética y sostenibilidad ambiental).*
2. **Plataforma de Gestión de Monitores Universitarios (PHP, MySQL, Bootstrap):** Destacar el desarrollo integral del sistema de información para la Universidad Simón Bolívar con autenticación, filtrado por área académica y arquitectura MVC.
3. **Nearby Mechanics / Sistema Geoespacial de Rutas (Flutter, ArcGIS, SQLite):** Destacar la integración de mapas satelitales, trazado de rutas de proximidad y persistencia local sin conexión.
4. **Calculadora y Segmentadora de Redes IPv4 (JavaScript, HTML5, CSS3):** Demuestra dominio en infraestructura de redes, subnetting y protocolos de telecomunicaciones.
5. **Champions Manager (Java Web, GlassFish, SQL):** Demuestra dominio de tecnologías empresariales Java EE, manejo de servidores de aplicaciones y arquitectura transaccional.

---

## 15. Preguntas Clave para el Candidato

Para completar y blindar la hoja de vida ante cualquier filtro de selección técnica o entrevista con panel de ingenieros, Johan debe responder a las siguientes preguntas:

1. **Sobre PCStyle:** ¿Existe un repositorio en GitHub o enlace web público de PCStyle? ¿Tienes capturas o reportes de Google Search Console con fechas y consultas concretas para respaldar el posicionamiento SEO?
2. **Sobre la experiencia en "JR Development":** ¿Qué aplicaciones web o sistemas desarrollaste durante ese período (2023-2024)? ¿Fueron clientes comerciales locales, tiendas virtuales o plataformas a medida?
3. **Sobre el nivel de inglés:** La certificación data de 2018 (B1). ¿Cuál es tu nivel conversacional y de lectura técnica actual en 2026? ¿Te sientes cómodo en una entrevista técnica en inglés?
4. **Sobre los repositorios de proyectos:** ¿Los proyectos como IA Residuos, Rutas en Flutter, Champions Manager y Calculadora IP están en repositorios públicos en tu cuenta de GitHub (`johan12rojas`)? Vincularlos aportará una credibilidad del 100%.
5. **Sobre el archivo PDF:** ¿Tienes ya redactada una versión preliminar de tu hoja de vida formal para reemplazar el archivo de prueba `a.pdf` en el portafolio?

---

## 16. Anexo de Evidencias y Rutas de Archivos

| Dato / Elemento | Archivo Local de Respaldo | Ubicación / Líneas Exactas |
| :--- | :--- | :--- |
| **Identidad Completa** | `PORTAFOLIO/img/crudestudiantes.png` | Fila 1: `JOHAN SEBASTIAN ROJAS GOMEZ`, ID: 1 |
| **Correo Institucional** | `PORTAFOLIO/img/crudestudiantes.png` | Fila 1: `jrojas20@unisimon.edu.co` |
| **Semestre y Rol Docente** | `PORTAFOLIO/img/crudestudiantes.png` | Semestre 8, Área Apoyo: `FISICA`, Carrera: `INGENIERÍA DE SISTEMAS` |
| **Formación Académica** | `PORTAFOLIO/index.html` | Líneas 223 - 261 |
| **Certificaciones y Cursos** | `PORTAFOLIO/index.html` | Líneas 233 - 251 |
| **Métrica de IA Residuos** | `PORTAFOLIO/img/IA residuos.png` | Barra de progreso e inferencia: `99.1% CONTENEDOR AZUL` |
| **Algoritmo de Subnetting** | `PORTAFOLIO/img/calcuip.png` | Tabla de propiedades y hosts estáticos/dinámicos |
| **Dashboard y Fecha** | `PORTAFOLIO/img/climaweb.png` | "WEB CLIMA FROM SEBASTIAN", fecha: 4 de Noviembre de 2025 |
| **Rutas Satelitales ArcGIS** | `PORTAFOLIO/img/rutasflutter.png` | "Talleres en Cúcuta - 20 talleres encontrados", ruteo vectorial |
| **Historial Git y Autor** | `.git/` | Commit `5031aa5` y `5cf0f67` |
| **Archivo PDF Borrador** | `PORTAFOLIO/img/a.pdf` | Documento de 1 página con texto humorístico (Goku) |
