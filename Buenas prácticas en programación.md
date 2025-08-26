# Buenas prácticas en programación

> Guía breve y accionable para escribir software **claro, correcto, seguro y mantenible**. Diseñada para proyectos educativos y profesionales.  
> Licencia: MIT (puedes reutilizarla en tus repositorios).

---

## Índice

1. [Principios fundamentales](#principios-fundamentales)
2. [Legibilidad y estilo](#legibilidad-y-estilo)
3. [Diseño y arquitectura](#diseño-y-arquitectura)
4. [Control de versiones](#control-de-versiones)
5. [Pruebas (Testing)](#pruebas-testing)
6. [Documentación](#documentación)
7. [Gestión de errores y logging](#gestión-de-errores-y-logging)
8. [Seguridad](#seguridad)
9. [Rendimiento](#rendimiento)
10. [Concurrencia y paralelismo](#concurrencia-y-paralelismo)
11. [Datos y persistencia](#datos-y-persistencia)
12. [APIs y contratos](#apis-y-contratos)
13. [CI/CD y DevOps](#cicd-y-devops)
14. [Gestión de dependencias](#gestión-de-dependencias)
15. [Accesibilidad, i18n y l10n](#accesibilidad-i18n-y-l10n)
16. [Ética y cumplimiento](#ética-y-cumplimiento)
17. [Checklist rápida](#checklist-rápida)
18. [Recursos y herramientas](#recursos-y-herramientas)

---

## Principios fundamentales

- **KISS**: mantén las soluciones simples; evita la complejidad accidental.  
- **DRY**: no repitas lógica; extrae funciones/módulos reutilizables.  
- **YAGNI**: no implementes lo que no necesitas hoy.  
- **Single Responsibility**: cada unidad de código con una sola razón de cambio.  
- **SOLID** (OO): guía para clases y componentes flexibles y testeables.  
- **Fail Fast**: detecta y comunica errores lo antes posible.  
- **Defensive Programming**: valida entradas y estados.  
- **Observability first**: registra métricas y trazas desde el inicio.

---

## Legibilidad y estilo

- **Nombres claros**: `totalConIVA`, `fetchUserById`, `MAX_RETRIES`.  
- **Funciones cortas** (ideal < 30–40 líneas) con un nivel lógico de abstracción.  
- **Comentarios** explican *por qué*, no *qué* (el código ya dice qué).  
- **Convención de estilo**: usa linters/formatters (ej.: ESLint/Prettier, Black/Flake8, clang-format).  
- **Estructura consistente**: ordena imports, constantes, tipos, funciones públicas y privadas.  
- **Evita “magical numbers”**: usa constantes con nombre.

**Ejemplo (mal → bien):**
```js
// ❌
if (x > 86400000) alert("too old");

// ✅
const ONE_DAY_MS = 24 * 60 * 60 * 1000;
if (ageMs > ONE_DAY_MS) showStaleDataWarning();
```

---

## Diseño y arquitectura

- **Capas**: separación de dominios (UI, aplicación, dominio, infraestructura).  
- **Interfaces/puertos**: desacopla dominio de detalles (DB, red, FS).  
- **Inyección de dependencias**: facilita testeo y reemplazo.  
- **Modularidad**: paquetes con límites claros y API pequeña.  
- **Eventos/colas** cuando haya acoplamiento temporal bajo.  
- **Feature flags** para despliegues graduales.  
- **Documenta decisiones** (ADR: Architecture Decision Records).

---

## Control de versiones

- **Commits atómicos** y descriptivos (Conventional Commits recomendado):
  - `feat:`, `fix:`, `docs:`, `refactor:`, `test:`, `chore:`, `perf:`
- **Ramas**: *trunk-based* o *GitFlow* según equipo.  
- **PRs pequeños** y con revisión por pares.  
- **No subas secretos** ni binarios grandes; usa `.gitignore` y *secrets manager*.

---

## Pruebas (Testing)

- **Pirámide de pruebas**: unitarias (muchas), integración (algunas), e2e (pocas).  
- **Testables por diseño**: código puro, dependencias inyectadas, efectos aislados.  
- **Cobertura útil** (>80% orientativo), pero evita perseguir % sin sentido.  
- **TDD** cuando aporte claridad en dominios complejos.  
- **Datos de prueba realistas** y *fixtures* reutilizables.

**Ejemplo (unit test expressivo):**
```python
def test_total_con_descuento_aplica_redondeo():
    assert total_con_descuento(100.0, 0.15) == 85.00
```

---

## Documentación

- **README** con: propósito, instalación, uso, ejemplos y troubleshooting.  
- **Docstrings** y comentarios *por qué*/*decisiones*.  
- **Esquemas** (diagramas simples) para flujos clave.  
- **Changelog** y **Versionado Semántico** (SemVer).  
- **Guías de contribución** (CONTRIBUTING.md) y **código de conducta**.

---

## Gestión de errores y logging

- **Errores tipificados**: crea tipos/excepciones significativas (`ValidationError`).  
- **No silencies excepciones**; añade contexto y re-lanza cuando proceda.  
- **Logs estructurados** (JSON si es posible) con niveles: trace/debug/info/warn/error.  
- **No loguees PII/secretos**.  
- **Correlación**: incluye *request-id/trace-id*.

```ts
try {
  await service.process(orderId);
} catch (e) {
  logger.error({ orderId, err: serializeError(e) }, "process failed");
  throw new ProcessingError("Processing failed", { cause: e });
}
```

---

## Seguridad

- **Entrada**: valida y sanitiza (evita inyección).  
- **Autenticación/Autorización**: principios de mínimo privilegio; roles/atributos.  
- **Secretos**: nunca en repos; usa *vault/parameter store*.  
- **Dependencias**: auditadas y actualizadas (SCA).  
- **HTTPS** siempre; cabeceras de seguridad (CSP, HSTS).  
- **Criptografía estándar**: no inventes algoritmos.  
- **Backups y planes de recuperación** probados.

---

## Rendimiento

- **Mide antes de optimizar** (perfiladores y métricas).  
- **Complejidad**: elige algoritmos/estructuras adecuadas.  
- **Caching**: por capa (app, CDN, DB) con invalidación clara.  
- **Batching y paginación** para I/O.  
- **Lazy loading** y *streaming* donde aplique.

---

## Concurrencia y paralelismo

- **Inmutabilidad** y estructuras thread-safe.  
- **Evita condiciones de carrera**: locks, colas, transacciones.  
- **Idempotencia** en operaciones reintentables.  
- **Límites**: *timeouts*, *circuit breakers*, *bulkheads*.

---

## Datos y persistencia

- **Modelado explícito** (normalización vs desnormalización consciente).  
- **Índices** y claves correctas.  
- **Transacciones** donde haya integridad crítica.  
- **Migraciones versionadas** y reversibles.  
- **Política de retención** y GDPR/privacidad.

---

## APIs y contratos

- **Diseño primero** (OpenAPI/GraphQL schema).  
- **Versionado** y compatibilidad hacia atrás.  
- **Errores consistentes** (códigos/formatos).  
- **Rate limiting** y *throttling*.  
- **Idempotency keys** para POST críticos.  
- **Pruebas de contrato** entre servicios.

---

## CI/CD y DevOps

- **CI**: lint + test + build en cada PR.  
- **CD**: despliegues automatizados, *blue/green* o *canary*.  
- **Infra como código** (IaC: Terraform/Ansible).  
- **Observabilidad**: métricas (SLI/SLO), trazas, alertas accionables.  
- **Rollbacks** rápidos; *feature flags*.

---

## Gestión de dependencias

- **Bloqueo de versiones** (`lockfiles`).  
- **Actualizaciones regulares** (bots como Renovate/Dependabot).  
- **Mínimas necesarias**; elimina *bloat* y *supply chain risk*.  
- **Builds reproducibles** (contenedores).

---

## Accesibilidad, i18n y l10n

- **A11y**: etiquetas, contraste, foco, navegación por teclado, ARIA.  
- **i18n**: separa textos/culturas de la lógica.  
- **l10n**: formatos de fecha/número y pluralización.

---

## Ética y cumplimiento

- **Privacidad por diseño** y minimización de datos.  
- **Transparencia** en el uso de IA/automatizaciones.  
- **No discriminación**; evalúa sesgos y explicabilidad.  
- **Cumplimiento**: licencias, GDPR, propiedad intelectual.

---

## Checklist rápida

- [ ] Nombres claros y consistentes  
- [ ] Sin duplicación de lógica (DRY)  
- [ ] Funciones/clases pequeñas y con SRP  
- [ ] Linters/formatters sin errores  
- [ ] Tests unitarios y de integración pasan en CI  
- [ ] Manejo de errores con contexto y logs útiles  
- [ ] Secretos fuera del repo  
- [ ] Dependencias auditadas/actualizadas  
- [ ] Documentación mínima (README + ejemplos)  
- [ ] Métricas y alertas básicas configuradas

---

## Recursos y herramientas

- **Estilo**: EditorConfig, Prettier, ESLint, Black, Clang-Format  
- **Testing**: Jest, Vitest, PyTest, JUnit, pytest-django, Cypress, Playwright  
- **Seguridad**: Snyk, Trivy, Semgrep, OWASP ZAP, Dependabot  
- **CI/CD**: GitHub Actions, GitLab CI, CircleCI, ArgoCD  
- **Observabilidad**: OpenTelemetry, Prometheus, Grafana, ELK/EFK  
- **Docs**: MkDocs, Docusaurus, Swagger UI, Redoc

---

### Apéndice: patrón de función pequeña y testeable

```ts
// Dominio puro: fácil de testear
export function calcularTotalConIVA(base: number, iva: number): number {
  if (base < 0 || iva < 0) throw new RangeError("Valores no válidos");
  const total = base * (1 + iva);
  return Math.round(total * 100) / 100;
}

// Orquestación/infra: validación de entrada + logging + manejo de errores
export async function endpointCalcular(req, res, logger) {
  try {
    const base = Number(req.query.base);
    const iva = Number(req.query.iva ?? 0.21);
    const total = calcularTotalConIVA(base, iva);
    res.json({ total });
  } catch (e) {
    logger.warn({ err: e?.message }, "Petición inválida");
    res.status(400).json({ error: "Solicitud incorrecta" });
  }
}
```
