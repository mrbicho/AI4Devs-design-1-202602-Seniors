# Prompts utilizados para el diseño de LTI ATS

A continuación se documentan todos los prompts utilizados con Claude (Anthropic) para generar cada uno de los artefactos del documento de diseño.

---

## Prompt 1: Investigación, análisis y requisitos iniciales

```text
Actúa como un Product Manager senior especializado en HR Tech y diseño de productos SaaS B2B.

Estoy definiendo LTI, una startup que quiere construir el ATS del futuro. Antes de diseñar funcionalidades, necesito una fase de investigación y análisis que incluya:

1. Los principales problemas que tienen hoy los ATS tradicionales para recruiters, hiring managers y candidatos
2. Un benchmark breve de soluciones de referencia como Greenhouse, Lever, Workday y BambooHR
3. Oportunidades de diferenciación para una startup nueva
4. Requisitos funcionales iniciales
5. Requisitos no funcionales iniciales
6. Recomendación buy vs build: qué capacidades conviene construir y cuáles integrar

Devuélvelo en formato claro para incorporarlo a una documentación de análisis y diseño de sistema.
```text

---

## Prompt 2: Descripción del software, valor añadido y ventajas competitivas

```text
Actúa como un Product Manager senior especializado en software de recursos humanos (HR Tech).

Estoy creando una startup llamada LTI que quiere desarrollar el ATS (Applicant-Tracking System) del futuro. Necesito que me ayudes a definir:

1. Una descripción breve del software LTI (2-3 párrafos)
2. El valor añadido que aporta frente a soluciones existentes como Greenhouse, Lever, Workday o BambooHR
3. Las ventajas competitivas clave (al menos 5) que harán que LTI destaque en el mercado

Ten en cuenta que queremos enfocarnos en:
- Aumentar la eficiencia para los departamentos de HR
- Mejorar la colaboración en tiempo real entre reclutadores y managers
- Automatizaciones inteligentes del flujo de contratación
- Asistencia de IA en diversas tareas (screening de CVs, generación de descripciones de puesto, análisis predictivo de candidatos)

Sé específico y orientado al mercado actual de 2025-2026.
```text

---

## Prompt 3: Funciones principales del sistema

```text
Continuando con el diseño de LTI (ATS del futuro), necesito que detalles las funciones principales del sistema organizadas por módulos funcionales. Para cada función incluye:

- Nombre de la función
- Descripción breve de qué hace
- Quién es el usuario principal (reclutador, hiring manager, candidato, admin)

Organiza las funciones en estos módulos:
1. Gestión de ofertas de empleo
2. Pipeline de candidatos
3. Colaboración y comunicación
4. Automatización e IA
5. Analítica y reporting
6. Administración y configuración

Quiero entre 3-5 funciones por módulo.
```text

---

## Prompt 4: Diagrama Lean Canvas

```text
Genera un diagrama Lean Canvas en formato Mermaid para LTI, el ATS del futuro. El Lean Canvas debe cubrir los 9 bloques:

1. Problema: Los 3 principales problemas que resuelve LTI
2. Segmento de clientes: A quién va dirigido
3. Propuesta de valor única: Qué nos diferencia
4. Solución: Las 3 características principales que resuelven los problemas
5. Canales: Cómo llegamos a los clientes
6. Flujo de ingresos: Cómo se monetiza
7. Estructura de costes: Principales costes
8. Métricas clave: KPIs del negocio
9. Ventaja injusta: Qué tenemos que no se puede copiar fácilmente

Genera el diagrama en formato tabla Mermaid o en texto estructurado que sea visualmente claro en Markdown.
```text

---

## Prompt 5: Casos de uso principales con diagramas

```
Define los 3 casos de uso principales del sistema LTI ATS. Para cada caso de uso necesito:

1. **Nombre del caso de uso**
2. **Actores involucrados** (primarios y secundarios)
3. **Descripción** detallada del flujo
4. **Precondiciones** y **postcondiciones**
5. **Flujo principal** (paso a paso numerado)
6. **Flujos alternativos** (al menos 1 por caso de uso)
7. **Diagrama de caso de uso en formato PlantUML** (sintaxis @startuml/@enduml, usando relaciones <<include>> y <<extend>> cuando corresponda)

Los 3 casos de uso deben ser los más representativos del sistema:
- Uno relacionado con la publicación y gestión de ofertas
- Uno relacionado con el proceso de screening/evaluación de candidatos con IA
- Uno relacionado con la colaboración entre reclutadores y hiring managers

Usa la notación UML estándar para los diagramas.
```

---

## Prompt 6: Modelo de datos

```
Diseña el modelo de datos para el sistema LTI ATS. Necesito:

1. **Lista de entidades principales** (al menos 10 entidades)
2. Para cada entidad:
   - Nombre de la entidad
   - Atributos con nombre y tipo de dato (varchar, int, boolean, timestamp, uuid, text, enum, etc.)
   - Clave primaria y claves foráneas
3. **Relaciones entre entidades** con cardinalidad (1:1, 1:N, N:M)
4. **Diagrama Entidad-Relación en formato Mermaid** usando la sintaxis erDiagram

Las entidades deben cubrir como mínimo:
- Usuarios (reclutadores, managers, admins)
- Candidatos
- Ofertas de empleo (Job Positions)
- Aplicaciones/Candidaturas
- Etapas del pipeline
- Evaluaciones/Scorecards
- Entrevistas
- Comentarios/Notas
- Empresas/Departamentos
- Notificaciones

Asegúrate de que el modelo soporte los casos de uso definidos anteriormente.
```

---

## Prompt 7: Diseño del sistema a alto nivel

```
Diseña la arquitectura de alto nivel del sistema LTI ATS. Necesito:

1. **Descripción de la arquitectura** elegida (microservicios, monolito modular, etc.) y justificación
2. **Componentes principales** del sistema con su responsabilidad
3. **Tecnologías sugeridas** para cada capa (frontend, backend, base de datos, infraestructura)
4. **Patrones de diseño** utilizados (API Gateway, Event-Driven, CQRS, etc.)
5. **Diagrama de arquitectura de alto nivel en formato Mermaid** usando flowchart o graph

El sistema debe considerar:
- Escalabilidad para soportar desde startups hasta grandes empresas
- Alta disponibilidad
- Seguridad (GDPR, protección de datos de candidatos)
- Integración con servicios externos (LinkedIn, job boards, email, calendarios)
- Módulo de IA/ML para las funcionalidades inteligentes

Incluye en el diagrama: frontend, API Gateway, servicios backend, bases de datos, servicios de IA, integraciones externas, y sistemas de mensajería/eventos.
```

---

## Prompt 8: Diagrama C4 en profundidad

```
Genera un diagrama C4 completo para el sistema LTI ATS, profundizando en el componente de "AI Service" y mostrando claramente su relación con el motor de automatización. Necesito los 3 niveles del modelo C4:

**Nivel 1 - Contexto del Sistema:**
- Diagrama que muestre LTI ATS y sus actores externos (usuarios, sistemas externos)
- Formato: diagrama Mermaid C4Context o flowchart

**Nivel 2 - Contenedores:**
- Diagrama que muestre los contenedores principales (aplicación web, API, bases de datos, servicios)
- Formato: diagrama Mermaid

**Nivel 3 - Componentes (del Servicio de IA):**
- Profundiza en el servicio de IA mostrando sus componentes internos:
  - Motor de screening de CVs
  - Generador de descripciones de puesto
  - Sistema de matching candidato-puesto
  - Análisis predictivo de candidatos
  - Componente que traduzca hallazgos de IA en automatizaciones o recomendaciones de workflow
- Formato: diagrama Mermaid

Usa la notación C4 estándar y asegúrate de que los diagramas sean claros y legibles en Markdown.
```
