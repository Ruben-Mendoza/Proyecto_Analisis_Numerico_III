# Solución Numérica de la Ecuación de McKendrick–Von Foerster

> Proyecto final — **Análisis Numérico III**  
> Licenciatura en Matemática Aplicada · FAMAF, Universidad Nacional de Córdoba  

---

## Descripción

Implementación de un esquema de **diferencias finitas** para resolver la ecuación de McKendrick–Von Foerster, una ecuación diferencial parcial que modela la evolución temporal de una población estructurada por edades:

$$\frac{\partial P(a,t)}{\partial t} + \frac{\partial P(a,t)}{\partial a} = -\mu(a) P(a,t)$$

El modelo se aplica para **estimar las densidades poblacionales por edades en la República Argentina** entre 2010 y 2022, comparando las proyecciones contra los datos reales del INDEC.

### Experimentos realizados

- **Escenario 1:** tasas de natalidad y mortalidad constantes en el tiempo (valor medio del período 2010–2022).
- **Escenario 2:** tasas de mortalidad variables año a año (recálculo de la matriz de evolución en cada paso temporal).
- **Selección del paso óptimo:** se evaluaron distintos valores de $h$ (paso de tiempo), determinando que $h = 1$ día minimiza el error sin aumentar innecesariamente el costo computacional.

---

## Tecnologías y herramientas

- **Lenguaje:** Python 3
- **Bibliotecas:** `numpy`, `scipy` (interpolación spline lineal), `matplotlib`
- **Fuentes de datos:**
  - [INDEC](https://www.indec.gob.ar/) — densidades poblacionales por edad (2010 y 2022)
  - [DEIS](https://www.deis.msal.gov.ar/) — tasas de natalidad y mortalidad por edad y año
- **Documentación:** LaTeX

---
