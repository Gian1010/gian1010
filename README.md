<h1 align="center">Hola, soy Gianfranco 👋</h1>
<h3 align="center">Desarrollador web · IA generativa y automatización de procesos</h3>

<p align="center">
  Estudiante de 5.° año de Ingeniería en Sistemas de Información (UTN FRRE) · Resistencia, Chaco 🇦🇷
</p>

<p align="center">
  <a href="https://gianweb-tau.vercel.app"><img src="https://img.shields.io/badge/Portfolio-gianweb--tau.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white" /></a>
  <a href="mailto:gianfranconiveiro@hotmail.com"><img src="https://img.shields.io/badge/Email-gianfranconiveiro%40hotmail.com-0078D4?style=for-the-badge&logo=microsoftoutlook&logoColor=white" /></a>
</p>

---

## 🚀 Sobre mí

Diseño y entrego **sistemas web a medida para clientes reales**: comercios, profesionales de la salud y particulares.
Trabajo con asistentes y agentes de IA en todo el ciclo: **análisis, programación, testing y documentación**.

Lo que más me gusta es encontrar tareas repetitivas y hacer que **se resuelvan solas**: avisos automáticos, cálculos, control de stock, cierres financieros.
Cada sistema que entrego incluye **manual de usuario y capacitación personalizada**, para que el cliente lo use desde el primer día.

- 🔭 Actualmente: desarrollo freelance y soporte a usuarios en UTN FRRE
- 🤖 Me interesa: IA aplicada a procesos reales, agentes y automatización
- 📚 Formación reciente: *Una mirada hacia la inteligencia artificial* (Fundación Sadosky, 2026)

---

## 🔒 Proyectos para clientes

> [!NOTE]
> Los repositorios de estos proyectos son **privados** porque el código pertenece a cada cliente.
> Puedo mostrar demos o contar en detalle cómo están hechos.

### 🩺 Gestor de turnos
**Turnos online para profesionales de la salud independientes** (kinesiólogos, médicos, psicólogos).
El paciente entra desde un link, elige servicio, día y horario, y manda una **solicitud sin crear cuenta**. El profesional la acepta o la rechaza desde un panel con *Hoy, Solicitudes, Agenda, Pacientes y Configuración*. Reemplaza el ida y vuelta por WhatsApp sin que el profesional pierda el control de su agenda.

**⚙️ Automatizaciones**
- 📧 Emails automáticos cuando un turno se crea, se acepta, se rechaza o se cancela
- ⏰ Recordatorio al paciente **24 h antes** del turno
- ⚠️ Aviso al profesional cuando una solicitud está por vencer
- ⌛ Vencimiento automático de solicitudes sin respuesta (job programado cada minuto)
- 🔐 La solicitud **bloquea el horario** apenas llega: imposible tener turnos superpuestos
- 📅 Archivo `.ics` para agregar el turno al calendario
- 💬 Botones con el mensaje de WhatsApp ya escrito

**🧱 Por dentro**
- **Anti-overbooking garantizado por la base de datos** (restricción de exclusión sobre rangos de tiempo), no por chequeos en código
- **Máquina de estados** única para el turno: pendiente, confirmado, rechazado, vencido o cancelado
- Cada cambio de estado es **una transacción** con auditoría y eventos; los emails salen después, leyendo una cola (patrón *outbox*)
- **Multi-organización desde el día 1**, con Row Level Security activado en todas las tablas
- Privacidad: el link del paciente es un token aleatorio guardado solo como hash, y no se registran datos personales en los logs
- Arquitectura de **núcleo + canales**, preparada para sumar un canal de **WhatsApp con IA** que use las mismas reglas
- Accesible (**WCAG 2.2 AA**), con onboarding de 4 pasos y modo demo con datos ficticios

![Next.js](https://img.shields.io/badge/Next.js_16-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=flat-square&logo=shadcnui&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![Drizzle](https://img.shields.io/badge/Drizzle_ORM-C5F74F?style=flat-square&logo=drizzle&logoColor=black)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white)
![React Email](https://img.shields.io/badge/React_Email-000000?style=flat-square&logo=react&logoColor=white)
![Sentry](https://img.shields.io/badge/Sentry-362D59?style=flat-square&logo=sentry&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)

---

### 🧁 BrisaSystem
**Sistema de gestión integral para un emprendimiento de elaboración de productos.**
Junta en un solo lugar **insumos y stock, productos y recetas, pedidos y finanzas**, con un dashboard de indicadores. Nació directo de lo que necesitaba la clienta: calcular precios de venta, saber cuánto gana con cada producto y anotar ventas del tipo *"hoy 5 budines"*.

**⚙️ Automatizaciones**
- 💲 Calcula el **costo de cada producto según su receta** y el precio sugerido según el margen de ganancia
- 📦 Al marcar un pedido como *Entregado*, **descuenta solo los insumos del stock** según la receta, y antes valida que alcancen
- 📊 Suma automáticamente ingresos, costos y ganancia del período
- 🧾 Hace el **cierre financiero** del período y lo guarda en un historial
- 🚨 Avisa en el dashboard qué insumos tienen stock bajo y qué pedidos están pendientes de entrega o de pago

**🧱 Por dentro**
- API REST con 5 módulos: insumos, productos, recetas, pedidos y finanzas
- Frontend de una sola página, responsive para usar desde el celular
- Desplegado en Render

**📘 Entrega:** manual de usuario en PDF sin términos técnicos, video del sistema y capacitación.

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap_5-7952B3?style=flat-square&logo=bootstrap&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black)

---

### 🔧 NelsonSystem
**Inventario con escaneo de códigos de barras para una casa de repuestos**, pensado para usarse con una sola mano desde el celular.
Se escanea el código con la cámara para buscar, dar de alta productos y registrar entradas y salidas. Tiene dashboard con estadísticas, historial de movimientos, buscador y modo claro/oscuro.

**⚙️ Automatizaciones**
- 📷 Busca el producto apenas se escanea el código
- 🔢 Si la cámara no lee las barras, **lee los números impresos con OCR**
- 📳 Vibra al detectar un código
- 🗂️ Guarda cada movimiento con el stock anterior y el nuevo
- 🚨 Detecta solo los productos con stock bajo
- 📤 Exporta el inventario a **CSV/Excel** con la hora de Argentina y sin perder los ceros iniciales
- 📶 Avisa cuando no hay conexión

**🧱 Por dentro**
- **Escáner con triple motor:** `BarcodeDetector` nativo del navegador + Quagga2 + OCR con Tesseract.js, con validación del dígito verificador
- Lee EAN-13, UPC e **ITF-14** (los códigos de bultos mayoristas)
- **Cambios de stock atómicos** con funciones en PostgreSQL: nunca se pierde un movimiento aunque dos personas escaneen a la vez
- Borrado lógico: un producto eliminado conserva su historial
- Búsqueda parcial por nombre o código con índices trigram, scroll infinito y búsqueda mientras escribís
- Exportación protegida contra fórmulas maliciosas en Excel
- PWA instalable con service worker; las credenciales de la base nunca llegan al navegador
- Frontend sin frameworks ni build: HTML, CSS y JavaScript puro

**📘 Entrega:** manual de usuario completo (instalación en el celular, escaneo, truco del OCR, preguntas frecuentes) y capacitación.

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Tesseract](https://img.shields.io/badge/Tesseract.js_OCR-3C8FDB?style=flat-square)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=flat-square&logo=pwa&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

---

### 📦 StockHome
**PWA mobile-first para controlar stock por categorías** y saber qué reponer.
Se carga el stock actual y el mínimo de cada producto, y la app muestra al instante cuáles están en stock bajo. Se instala en el celular y pide login.

**⚙️ Automatizaciones**
- 🚨 Marca sola los productos con stock igual o por debajo del mínimo
- 🛡️ No deja que el stock quede negativo (validado en la interfaz y en la base)
- 🔒 No permite borrar una categoría que todavía tiene productos

**🧱 Por dentro**
- Login con Supabase Auth y **Row Level Security**: cada usuario ve solo sus datos
- Capas separadas: páginas → hooks (TanStack Query) → servicios → reglas de negocio puras
- Errores técnicos traducidos a mensajes amigables
- **Modo demo en memoria** para desarrollar y testear sin base de datos
- Tests unitarios (Vitest) y end-to-end en móvil y desktop (Playwright)

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square&logo=reactquery&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=flat-square&logo=pwa&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)

---

### 💜 ARIRANG · ARGENTINA
**Álbum de recuerdos digital con forma de photobook** del concierto de BTS del 21/10/2026 en La Plata.
Portada con cuenta regresiva, agenda del viaje, tickets, collages, una página por integrante, canciones sorpresa y un archivo de cartas. Es privado, se entra con PIN y **todo se edita desde la misma página** con guardado automático.

**⚙️ Automatizaciones**
- ⏳ Cuenta regresiva al concierto y estado del viaje
- 🖼️ **Collages que se arman solos** según la forma de cada foto (y se pueden reordenar a mano)
- 📐 Procesa las fotos **en el celular antes de subirlas**: valida el archivo, corrige la orientación y genera 3 tamaños en WebP
- 💾 Guardado automático ("Guardando…" → "Guardado ✓")
- 🔐 Bloqueo con PIN por dispositivo

**🧱 Por dentro**
- PIN **hasheado con scrypt**, sesiones con cookie `httpOnly` y bloqueos crecientes tras varios intentos fallidos
- Fotos en Storage privado con **URLs firmadas que vencen en minutos**; subida directa en paralelo
- Cada espacio pide **la foto más chica que se vea nítida**: la portada en el celular bajó de 1,3 MB a 0,5 MB
- Funciona **sin conexión**: guarda la app y hasta 400 fotos ya vistas
- Modo local de respaldo para usarlo sin configurar nada

![Next.js](https://img.shields.io/badge/Next.js_16-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind_4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=flat-square&logo=pwa&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)

---

### 📸 G&N
**Diario compartido para dos personas**, donde cada día se guarda como una polaroid con foto, título, fecha y descripción. Tiene vista feed y grilla, contadores de días, cartas y ajustes compartidos.

**⚙️ Automatizaciones**
- 🔄 Sincronización **en tiempo real** entre los dos celulares
- 🔔 **Notificaciones push** cuando el otro sube algo
- 📴 Sin internet, guarda los posts en una cola y **los sube solos** cuando vuelve la conexión
- 🗓️ Separa el feed por meses automáticamente
- 🔐 Pide el PIN una sola vez por dispositivo, con sesión invisible
- 💾 Exportación de respaldo

**🧱 Por dentro**
- Sesión anónima de Supabase + PIN, con **Row Level Security** para que solo los dispositivos autorizados lean o escriban
- Supabase Realtime para los cambios en vivo y Web Push (VAPID) con una función serverless
- Cola offline en IndexedDB y modo local completo sin backend
- **Re-skinneable para otros clientes** cambiando un solo archivo de configuración
- Tests de la base con PostgreSQL embebido (PGlite), unitarios con Vitest y end-to-end con Playwright

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=flat-square&logo=pwa&logoColor=white)
![Web Push](https://img.shields.io/badge/Web_Push-FF6F00?style=flat-square)
![IndexedDB](https://img.shields.io/badge/IndexedDB-555555?style=flat-square)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)

---

## 🌐 Proyecto propio

### GianWeb · [gianweb-tau.vercel.app](https://gianweb-tau.vercel.app)
Mi portfolio, con proyectos, servicios, precios y preguntas frecuentes. Sitio estático, rápido y pensado para SEO.
- 🚀 **Deploy automático** en cada `git push`
- 🗺️ Sitemap generado automáticamente para Google
- 🎞️ Scroll horizontal animado con GSAP (solo en desktop) y smooth scroll con Lenis
- ♿ Respeta *reduced motion* y usa fuentes autohospedadas

![Astro](https://img.shields.io/badge/Astro-BC52EE?style=flat-square&logo=astro&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![GSAP](https://img.shields.io/badge/GSAP-88CE02?style=flat-square&logo=greensock&logoColor=black)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

---

## 🎓 Proyectos académicos

| Proyecto | Qué hace | Tecnologías |
|---|---|---|
| ⚙️ **Automatización CI/CD** (2025) | Pipeline que automatiza build, análisis de calidad y notificaciones | GitHub · CircleCI · SonarCloud · Trello · Slack |
| 🗺️ **Proyecto Integrador GIS** (2025) | Sistema de información geográfica con capas espaciales | GeoServer · OpenLayers · PostgreSQL |
| 🗳️ **Sistema Bienal del Chaco** (2024) | Gestión de eventos con votación por código QR para cientos de asistentes | — |

---

## 🤖 IA y automatización

![Claude](https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![ChatGPT](https://img.shields.io/badge/ChatGPT-74AA9C?style=for-the-badge&logo=openai&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![Copilot](https://img.shields.io/badge/GitHub_Copilot-000000?style=for-the-badge&logo=githubcopilot&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![CircleCI](https://img.shields.io/badge/CircleCI-343434?style=for-the-badge&logo=circleci&logoColor=white)

- 🧠 **Prompt engineering:** diseño, prueba y documentación de prompts reutilizables (rol, contexto, few-shot, salidas estructuradas)
- 🛠️ **Desarrollo con agentes:** especificar, programar, depurar y documentar sistemas completos
- 👥 **Adopción:** manuales sin términos técnicos, videos y capacitación personalizada a cada cliente

## 🛠️ Tecnologías

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Astro](https://img.shields.io/badge/Astro-BC52EE?style=for-the-badge&logo=astro&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

---

<p align="center">
  📫 ¿Querés ver una demo o charlar de un proyecto? Escribime a <b>gianfranconiveiro@hotmail.com</b>
</p>
