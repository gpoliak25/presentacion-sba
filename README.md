# Capa Semántica Ejecutiva — EISPLUS / UEN Strategic Business Advisory

Dos piezas para la misma conversación de producto: el **brief** que define qué construir y la **demo** que lo muestra funcionando.

**En línea:** https://presentacion-sba-eis.vercel.app — portada, `/demo` y `/brief`.

| Archivo | Qué es |
|---|---|
| [`index.html`](index.html) | Portada con los dos accesos. Es lo que se sirve en la raíz del sitio. |
| [`Brief_Producto_Capa_Semantica_Ejecutiva.html`](Brief_Producto_Capa_Semantica_Ejecutiva.html) | Presentación de 15 láminas para el Product Owner: propósito, usuarios, arquitectura, modelo semántico, alcance del MVP, backlog, métricas del piloto y decisiones abiertas. Se navega con las flechas del teclado. |
| [`demo/index.html`](demo/index.html) | Demo interactiva del producto sobre un cliente ficticio con JD Edwards. Un solo archivo, sin dependencias de build. |

## Ver la demo

Abrí `demo/index.html` en el navegador. Si preferís servirla:

```bash
node demo/server.js          # http://localhost:8080
PORT=9000 node demo/server.js
```

Única dependencia externa: las tipografías IBM Plex desde Google Fonts. Sin conexión cae a la tipografía del sistema y funciona igual.

## Qué muestra la demo

Cliente ficticio: **Manufacturas Andes S.A.**, ERP JD Edwards E1 9.2, cierre de septiembre 2026. Todas las cifras son inventadas para la demostración.

- **Panel del directorio** — árbol de KPIs que baja del margen bruto a sus causas, con alertas por umbral y sus playbooks.
- **Preguntar** — seis preguntas guionadas que responden con cifra, explicación causal, evidencia y playbook. Dos de ellas muestran los límites del producto: una consulta operativa que deriva sin responder, y un término que no está en el modelo y que no inventa.
- **Trazabilidad** — cada respuesta es reproducible: pregunta → clasificación → términos resueltos → consulta → datos → texto.
- **Brief semanal** — el documento que recibe el directorio los lunes, incluida la sección de preguntas sin responder.
- **Decisiones** — bitácora que crece cuando el CFO registra una decisión desde una respuesta.
- **Modelo semántico** — el editor del consultor: métricas certificadas con fórmula y dueño, glosario, umbrales, relaciones causales, ranking impacto/esfuerzo y playbooks.
- **Uso y brechas** — las métricas del go / no-go del piloto y el backlog que alimenta la versión siguiente del modelo.

Abajo de todo hay un **guion de demo de siete pasos** que navega solo, pensado para presentarle el producto a un CFO en unos siete minutos.

### Cobertura de los servicios SBA

Cada servicio de la UEN deja una parte del modelo, y la demo muestra las cinco:

| Servicio | Dónde se ve |
|---|---|
| Readiness Assessment | Glosario, vista fuente por métrica, cobertura de dominios, módulo *Uso y brechas* |
| Efficiency & Process Intelligence | Pestaña *Impacto / esfuerzo*, métricas de proceso, relaciones causales |
| Executive Decision Framework | Árbol de KPIs, pestaña *Umbrales*, playbooks |
| Financial Insight Acceleration | Fórmulas certificadas, escenario de flujo a 60 días |
| Governance Blueprint | Dueño por métrica, selector de rol y permisos, versionado con rollback |

Las capas de conectores y vistas certificadas aparecen como referencia (`vw_margen_linea`, `JD Edwards E1 9.2`), no como pantalla propia: son plomería, no producto.

## Estado

Material de trabajo interno. «Capa Semántica Ejecutiva» es el nombre de trabajo; la marca comercial se define aparte.
