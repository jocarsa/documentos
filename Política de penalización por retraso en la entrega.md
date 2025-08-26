# Política de penalización por retraso en la entrega

La entrega puntual es un criterio esencial de evaluación. Para garantizar la equidad, se aplicará una **penalización progresiva diaria** sobre la nota en función del tiempo transcurrido desde la **fecha y hora límite (deadline)** hasta la **fecha y hora de entrega efectiva**.

---

## Definiciones

- **Deadline:** fecha y hora límite oficiales publicadas para la actividad.
- **Tiempo de retraso (T):** horas transcurridas desde el deadline hasta la entrega.
- **Días de retraso (D):** número de **días completos** de retraso. Se calcula como  
  \[
  D=\left\lfloor \frac{T}{24\ \text{h}} \right\rfloor
  \]
  (si \(T<0\), se toma \(D=0\)).

> **Nota:** Un retraso de 0–23:59:59 h cuenta como **D = 0** (no hay penalización).

---

## Regla de penalización

- **Multiplicador por retraso:**  
  \[
  \text{mult}(D) = \max\big(0,\ 1 - 0.01 \times D\big)
  \]
- **Nota final:**  
  \[
  \text{Nota Final} = \text{Nota Obtenida} \times \text{mult}(D)
  \]
- **Límite:** si \(D \ge 100\), la actividad **no puntúa** (\(\text{mult}=0\)).

---

## Tabla visual (referencia rápida)

| Días de retraso (D) | Ventana de retraso desde el deadline | Multiplicador | Nota máxima (sobre 10) |
|---:|---|---:|---:|
| 0  | < 24 h                               | 1.00 | 10.00 |
| 1  | ≥ 24 h y < 48 h                      | 0.99 | 9.90 |
| 2  | ≥ 48 h y < 72 h                      | 0.98 | 9.80 |
| 3  | ≥ 72 h y < 96 h                      | 0.97 | 9.70 |
| 4  | ≥ 96 h y < 120 h                     | 0.96 | 9.60 |
| 5  | ≥ 120 h y < 144 h                    | 0.95 | 9.50 |
| 6  | ≥ 144 h y < 168 h                    | 0.94 | 9.40 |
| 7  | ≥ 168 h y < 192 h                    | 0.93 | 9.30 |
| 8  | ≥ 192 h y < 216 h                    | 0.92 | 9.20 |
| 9  | ≥ 216 h y < 240 h                    | 0.91 | 9.10 |
| 10 | ≥ 240 h y < 264 h                    | 0.90 | 9.00 |
| 11 | ≥ 264 h y < 288 h                    | 0.89 | 8.90 |
| 12 | ≥ 288 h y < 312 h                    | 0.88 | 8.80 |
| 13 | ≥ 312 h y < 336 h                    | 0.87 | 8.70 |
| 14 | ≥ 336 h y < 360 h                    | 0.86 | 8.60 |
| 15 | ≥ 360 h y < 384 h                    | 0.85 | 8.50 |
| 20 | ≥ 480 h y < 504 h                    | 0.80 | 8.00 |
| 25 | ≥ 600 h y < 624 h                    | 0.75 | 7.50 |
| 30 | ≥ 720 h y < 744 h                    | 0.70 | 7.00 |
| 40 | ≥ 960 h y < 984 h                    | 0.60 | 6.00 |
| 50 | ≥ 1200 h y < 1224 h                  | 0.50 | 5.00 |
| 60 | ≥ 1440 h y < 1464 h                  | 0.40 | 4.00 |
| 70 | ≥ 1680 h y < 1704 h                  | 0.30 | 3.00 |
| 80 | ≥ 1920 h y < 1944 h                  | 0.20 | 2.00 |
| 90 | ≥ 2160 h y < 2184 h                  | 0.10 | 1.00 |
| 99 | ≥ 2376 h y < 2400 h                  | 0.01 | 0.10 |
| ≥100 | ≥ 2400 h                             | 0.00 | 0.00 |

> **Lectura de la tabla:** “D = 3” significa entre 72 h y 96 h de retraso. La nota final se obtiene multiplicando la nota obtenida por **0.97**.

---

## Ejemplos prácticos

- **Retraso de 10 horas** → \(D=0\) → multiplicador **1.00**  
  - Nota obtenida 8.4 → Nota final **8.40**
- **Retraso de 30 horas** → \(D=1\) → multiplicador **0.99**  
  - Nota obtenida 10 → Nota final **9.90**
- **Retraso de 75 horas** → \(D=3\) → multiplicador **0.97**  
  - Nota obtenida 7.5 → Nota final **7.275** (≈ **7.28** si se redondea a 2 decimales)
- **Retraso de 20 días** → \(D=20\) → multiplicador **0.80**  
  - Nota obtenida 9.0 → Nota final **7.20**
- **Retraso de 100 días** → \(D\ge100\) → multiplicador **0.00**  
  - Nota final **0**

> **Redondeo:** salvo que la normativa del centro indique otra cosa, se redondeará la **nota final** a 2 decimales.

---

## Recomendaciones y aclaraciones

- La hora de referencia será la **hora oficial de la plataforma** donde se entrega la actividad.  
- Asegúrate de **publicar o consultar el deadline exacto** (fecha y hora) y considerar festivos si el centro así lo contempla.  
- En caso de **incidencias técnicas documentadas** o **causas justificadas**, se aplicarán las medidas excepcionales que establezca la coordinación académica (si procede).

---

## Anexo: Fórmulas y cálculo operativo

- **Cálculo de \(D\)** (conceptual):  
  1. Calcula \(T\) = horas(Entrega) − horas(Deadline).  
  2. Si \(T \le 0\) ⇒ \(D = 0\).  
  3. Si \(T > 0\) ⇒ \(D = \left\lfloor \dfrac{T}{24} \right\rfloor\).

- **Multiplicador:** \(\text{mult}(D) = \max(0,\ 1 - 0.01D)\).

---

## Código de referencia (opcional)

> Estos ejemplos ilustran cómo implementar la regla en sistemas automáticos de corrección.

**JavaScript**
```js
function multiplicadorRetraso(deadlineISO, entregaISO) {
  const deadline = new Date(deadlineISO).getTime();
  const entrega  = new Date(entregaISO).getTime();
  const diffMs   = Math.max(0, entrega - deadline);
  const dias     = Math.floor(diffMs / (24 * 60 * 60 * 1000)); // D
  return Math.max(0, 1 - 0.01 * dias);
}

// Ejemplo:
const mult = multiplicadorRetraso("2025-10-01T23:59:59+02:00", "2025-10-04T01:00:00+02:00"); // ~D=2
const notaFinal = 8.75 * mult;
