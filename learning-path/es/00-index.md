# Ruta de Aprendizaje de ASP.NET Core — Índice General

> 🌐 [English version](../en/00-index.md)

## Cómo usar esta ruta de aprendizaje

Esta ruta está organizada en **cinco niveles progresivos**, donde cada uno se construye sobre el anterior. No necesitás empezar en el Nivel 1 — de hecho, la mayoría de los desarrolladores en actividad no lo hacen. Los niveles están diseñados para que puedas saltar directamente al punto donde tu conocimiento actual termina y tu curiosidad empieza. El Nivel 1 cubre los fundamentos para quienes recién arrancan, el Nivel 2 desarrolla habilidades prácticas para el día a día, el Nivel 3 aborda las preguntas de "¿por qué funciona así?", el Nivel 4 te guía a través del código fuente real del framework, y el Nivel 5 te prepara para contribuir de vuelta al proyecto.

**Usá la autoevaluación de abajo para encontrar tu punto de partida.** Respondé cada pregunta con honestidad — nadie te está evaluando. Si respondés "no" a alguna pregunta, ese es tu nivel. Empezá ahí, avanzá por los módulos en orden, y pasá al siguiente nivel cuando te sientas listo. Cada módulo indica un tiempo estimado, pero tomate el que necesites. Entender siempre le gana a la velocidad.

Cada módulo está estructurado alrededor de una pregunta central — el tipo de pregunta que, cuando la podés responder con confianza, significa que realmente entendés el tema. Los módulos te llevan directamente al código fuente de ASP.NET Core en este repositorio (`dotnet/aspnetcore`), así que vas a estar leyendo código real de producción, no ejemplos simplificados. Eso es intencional. La mejor manera de entender un framework es leer cómo está construido de verdad.

---

## Autoevaluación: Encontrá tu nivel

Recorré estas preguntas en orden. **La primera respuesta "no" te indica dónde empezar.**

> **P1: ¿Podés explicar qué son los códigos de estado HTTP, los headers y los cuerpos de request/response?**
> - ✅ Sí → seguí a la P2
> - ❌ No → **Empezá en el [Nivel 1 — Fundamentos](#nivel-1--fundamentos)**

> **P2: ¿Podés describir qué hace el middleware en ASP.NET Core y por qué el orden importa?**
> - ✅ Sí → seguí a la P3
> - ❌ No → **Empezá en el [Nivel 1 — Fundamentos](#nivel-1--fundamentos)**, módulo 1.3

> **P3: ¿Construiste alguna vez una API REST con ASP.NET Core usando controllers o minimal APIs?**
> - ✅ Sí → seguí a la P4
> - ❌ No → **Empezá en el [Nivel 2 — Practicante](#nivel-2--practicante)**

> **P4: ¿Podés explicar la diferencia entre los ciclos de vida `Transient`, `Scoped` y `Singleton` — y describir un bug real causado por usar el incorrecto?**
> - ✅ Sí → seguí a la P5
> - ❌ No → **Empezá en el [Nivel 2 — Practicante](#nivel-2--practicante)**, módulo 2.3

> **P5: ¿Escribiste alguna vez una implementación personalizada de `IMiddleware` y configuraste Kestrel para producción?**
> - ✅ Sí → seguí a la P6
> - ❌ No → **Empezá en el [Nivel 3 — Avanzado](#nivel-3--avanzado)**

> **P6: ¿Podés rastrear cómo `DfaMatcher` selecciona un endpoint, o explicar cómo `ControllerActionInvoker` orquesta los filtros?**
> - ✅ Sí → seguí a la P7
> - ❌ No → **Empezá en el [Nivel 4 — Internos](#nivel-4--internos)**

> **P7: ¿Leíste el código fuente de `IApplicationBuilder.Build()` y entendés cómo se compila la cadena de delegados de middleware?**
> - ✅ Sí → seguí a la P8
> - ❌ No → **Empezá en el [Nivel 4 — Internos](#nivel-4--internos)**

> **P8: ¿Compilaste `dotnet/aspnetcore` desde el código fuente, corriste su suite de tests, y enviaste (o consideraste enviar) un pull request?**
> - ✅ Sí → **Estás en el [Nivel 5 — Experto / Contribuidor](#nivel-5--experto--contribuidor)**. Elegí el módulo que más te interese.
> - ❌ No → **Empezá en el [Nivel 5 — Experto / Contribuidor](#nivel-5--experto--contribuidor)**

---

## Vista General de la Ruta

### Nivel 1 — Fundamentos

*Sos nuevo en ASP.NET Core o en desarrollo web. Estos módulos te dan el modelo mental sobre el que se construye todo lo demás.*

| Módulo | Tema | Esfuerzo Est. | Pregunta Clave que Responde |
|--------|------|:-------------:|----------------------------|
| 1.1 | HTTP y Fundamentos de Servidores Web | 2 h | ¿Qué es HTTP y cómo maneja un servidor web las requests? |
| 1.2 | Tu Primera Aplicación ASP.NET Core | 3 h | ¿Qué pasa cuando ejecutás `dotnet new web` y `dotnet run`? |
| 1.3 | El Pipeline de Middleware | 2 h | ¿Cómo viaja una request a través de tu aplicación? |
| 1.4 | Fundamentos de Routing | 2 h | ¿Cómo mapea ASP.NET Core las URLs a código? |
| 1.5 | Fundamentos de Dependency Injection | 2 h | ¿Qué es dependency injection y por qué ASP.NET Core lo usa en todos lados? |
| 1.6 | Configuración y Entornos | 1.5 h | ¿Cómo lee tu app la configuración y se adapta a dev/prod? |

**Esfuerzo total estimado: ~12.5 horas**

---

### Nivel 2 — Practicante

*Entendés los fundamentos y querés construir aplicaciones reales. Estos módulos cubren las habilidades cotidianas de un desarrollador ASP.NET Core productivo.*

| Módulo | Tema | Esfuerzo Est. | Pregunta Clave que Responde |
|--------|------|:-------------:|----------------------------|
| 2.1 | Construyendo APIs con Controllers y Minimal APIs | 3 h | ¿Cuáles son los dos modelos de programación y cuándo conviene usar cada uno? |
| 2.2 | Model Binding y Validación | 2 h | ¿Cómo convierte ASP.NET Core datos HTTP en objetos C#? |
| 2.3 | Escribiendo Middleware Personalizado | 2 h | ¿Cómo agrego mi propia lógica al pipeline de requests? |
| 2.4 | Fundamentos de Autenticación y Autorización | 3 h | ¿Cómo protejo mis endpoints? |
| 2.5 | Manejo de Errores y Logging | 2 h | ¿Cómo manejo errores de forma elegante y monitoreo lo que pasa? |
| 2.6 | Integración con Entity Framework Core | 3 h | ¿Cómo me conecto a una base de datos y gestiono los datos? |

**Esfuerzo total estimado: ~15 horas**

---

### Nivel 3 — Avanzado

*Te sentís cómodo construyendo aplicaciones y ahora querés entender la mecánica más profunda. Estos módulos transforman el "funciona" en "sé exactamente por qué funciona".*

| Módulo | Tema | Esfuerzo Est. | Pregunta Clave que Responde |
|--------|------|:-------------:|----------------------------|
| 3.1 | Pipeline de Middleware en Profundidad | 3 h | ¿Cómo afecta el orden del middleware al comportamiento, y cómo lo depuro? |
| 3.2 | Internos del Motor de Routing | 3 h | ¿Cómo matchea ASP.NET Core URLs a endpoints de forma eficiente? |
| 3.3 | Scopes de DI y Ciclos de Vida de Servicios | 2 h | ¿Por qué las incompatibilidades de ciclo de vida causan bugs, y cómo los corrijo? |
| 3.4 | Configuración de Kestrel Server | 2 h | ¿Cómo configuro el servidor web para producción? |
| 3.5 | Optimización de Rendimiento | 3 h | ¿Dónde están los hot paths y cómo los optimizo? |
| 3.6 | Patrones Avanzados de Autenticación | 2 h | ¿Cómo funcionan los policy schemes, la transformación de claims y la autenticación multi-scheme? |

**Esfuerzo total estimado: ~15 horas**

---

### Nivel 4 — Internos

*Querés leer y entender el código fuente de ASP.NET Core. Estos módulos te guían por los internos más importantes del framework, archivo por archivo.*

| Módulo | Tema | Esfuerzo Est. | Pregunta Clave que Responde |
|--------|------|:-------------:|----------------------------|
| 4.1 | IApplicationBuilder y Construcción del Pipeline | 3 h | ¿Cómo se construye y compila realmente el pipeline de middleware? |
| 4.2 | DFA Matcher y Selección de Endpoints | 4 h | ¿Cómo construye routing una máquina de estados para matchear URLs? |
| 4.3 | Pipeline de Ejecución de Acciones MVC | 4 h | ¿Cómo funcionan internamente los filtros, el model binding y la invocación de acciones? |
| 4.4 | Mecánica de Resolución del ServiceProvider | 3 h | ¿Cómo resuelve dependency injection los grafos de servicios y gestiona los scopes? |
| 4.5 | HttpContext y el Patrón Features | 3 h | ¿Cómo abstrae ASP.NET Core las diferencias entre servidores? |
| 4.6 | Internos de WebApplicationBuilder | 2 h | ¿Cómo compone el builder el hosting, dependency injection y el middleware? |

**Esfuerzo total estimado: ~19 horas**

---

### Nivel 5 — Experto / Contribuidor

*Estás listo para extender, modificar y contribuir al framework. Estos módulos te enseñan cómo trabaja el equipo y cómo participar.*

| Módulo | Tema | Esfuerzo Est. | Pregunta Clave que Responde |
|--------|------|:-------------:|----------------------------|
| 5.1 | Compilar ASP.NET Core desde el Código Fuente | 4 h | ¿Cómo clono, compilo y testeo el framework localmente? |
| 5.2 | Extender el Sistema de Routing | 4 h | ¿Cómo escribo `MatcherPolicy`, route constraints y link generators personalizados? |
| 5.3 | Escribir Middleware con Calidad de Framework | 3 h | ¿Qué patrones usa el framework internamente para su middleware? |
| 5.4 | Authentication Handlers Personalizados | 3 h | ¿Cómo implemento un esquema de autenticación personalizado desde cero? |
| 5.5 | Contribuir a dotnet/aspnetcore | 3 h | ¿Cuál es el flujo de contribución, la infraestructura de tests y el proceso de review? |
| 5.6 | Diseñar Modelos de Hosting Personalizados | 3 h | ¿Cómo creo hosts especializados para escenarios que no son HTTP? |

**Esfuerzo total estimado: ~20 horas**

---

## Áreas Temáticas (organizadas por línea de especialización)

Usá estas referencias cruzadas para seguir un tema a lo largo de los cinco niveles — desde el primer contacto hasta la especialización profunda.

### 🏗️ Hosting y Arranque

- [Nivel 1: Tu Primera Aplicación ASP.NET Core](01-foundations-aspnet-core.md#lesson-12) — qué hace `dotnet run` internamente
- [Nivel 2: Configuración y Entornos](02-practitioner-aspnet-core.md) — `appsettings.json`, variables de entorno y el patrón de opciones
- [Nivel 3: Configuración de Kestrel Server](03-advanced-aspnet-core.md) — endpoints, límites, HTTPS y ajustes para producción
- [Nivel 4: Internos de WebApplicationBuilder](04-internals-aspnet-core.md) — cómo `WebApplicationBuilder` compone el host
- [Nivel 5: Diseñar Modelos de Hosting Personalizados](05-expert-aspnet-core.md) — construir hosts especializados para cargas de trabajo que no son HTTP

### 🔗 Pipeline de Middleware

- [Nivel 1: El Pipeline de Middleware](01-foundations-aspnet-core.md#lesson-13) — la cadena de request delegates y `Use`/`Map`/`Run`
- [Nivel 2: Escribir Middleware Personalizado](02-practitioner-aspnet-core.md) — enfoque por convención y con `IMiddleware`
- [Nivel 3: Pipeline de Middleware en Profundidad](03-advanced-aspnet-core.md) — orden, ramificación y depuración con diagnósticos
- [Nivel 4: IApplicationBuilder y Construcción del Pipeline](04-internals-aspnet-core.md) — cómo `Build()` compila la cadena de delegados
- [Nivel 5: Escribir Middleware con Calidad de Framework](05-expert-aspnet-core.md) — patrones del propio middleware del framework

### 🗺️ Routing

- [Nivel 1: Fundamentos de Routing](01-foundations-aspnet-core.md#lesson-14) — route templates, parámetros y constraints
- [Nivel 2: Controllers y Minimal APIs](02-practitioner-aspnet-core.md) — los dos modelos de programación y su routing
- [Nivel 3: Internos del Motor de Routing](03-advanced-aspnet-core.md) — cómo cooperan `EndpointRoutingMiddleware` y `EndpointMiddleware`
- [Nivel 4: DFA Matcher y Selección de Endpoints](04-internals-aspnet-core.md) — la máquina de estados detrás del matcheo de URLs
- [Nivel 5: Extender el Sistema de Routing](05-expert-aspnet-core.md) — `MatcherPolicy` personalizados, constraints y link generators

### 💉 Dependency Injection

- [Nivel 1: Fundamentos de DI](01-foundations-aspnet-core.md#lesson-15) — registrar y resolver servicios
- [Nivel 2: Patrones de Registro de Servicios](02-practitioner-aspnet-core.md) — factory registrations, `TryAdd` y keyed services
- [Nivel 3: Scopes de DI y Ciclos de Vida de Servicios](03-advanced-aspnet-core.md) — captive dependencies y validación de scopes
- [Nivel 4: Mecánica de Resolución del ServiceProvider](04-internals-aspnet-core.md) — cómo el contenedor construye y cachea grafos de servicios
- [Nivel 5: Contribuir Extensiones de DI Personalizadas](05-expert-aspnet-core.md) — escribir métodos de extensión `Add*` al estilo del framework

### 🔒 Seguridad

- [Nivel 1: Conceptos de Seguridad](01-foundations-aspnet-core.md) — HTTPS, CORS y por qué la seguridad importa desde el día uno
- [Nivel 2: Fundamentos de Autenticación y Autorización](02-practitioner-aspnet-core.md) — cookies, JWT, `[Authorize]` y policies
- [Nivel 3: Patrones Avanzados de Autenticación](03-advanced-aspnet-core.md) — policy schemes, transformación de claims y autenticación multi-scheme
- [Nivel 4: Internos del Pipeline de Autorización](04-internals-aspnet-core.md) — cómo `AuthorizationMiddleware` evalúa las policies
- [Nivel 5: Authentication Handlers Personalizados](05-expert-aspnet-core.md) — implementar `AuthenticationHandler<T>` desde cero

### 🎯 MVC y Diseño de APIs

- [Nivel 2: Controllers y Minimal APIs](02-practitioner-aspnet-core.md) — construir APIs con ambos modelos de programación
- [Nivel 2: Model Binding y Validación](02-practitioner-aspnet-core.md) — convertir requests HTTP en objetos C# validados
- [Nivel 3: Optimización de Rendimiento](03-advanced-aspnet-core.md) — output caching, compresión de respuestas y patrones async
- [Nivel 4: Pipeline de Ejecución de Acciones MVC](04-internals-aspnet-core.md) — `ControllerActionInvoker`, filtros y el resource pipeline
- [Nivel 5: Contribuir a dotnet/aspnetcore](05-expert-aspnet-core.md) — el flujo completo de contribución e infraestructura de tests



PS C:\Repos\GitH\aspnetcore> copilot --banner

  ╭─╮╭─╮   Changes   +507 -0
  ╰─╯╰─╯   Requests  6.66 Premium (1h 12m 1s)
  █ ▘▝ █   Tokens    ↑ 9.6m • ↓ 210.8k • 8.7m (cached)
   ▔▔▔▔    Resume    copilot --resume=2fdc722f-10ad-4190-976b-5b8ebd05947b