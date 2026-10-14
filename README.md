# Brief estratégico · Leasing Empresas BTG Pactual Chile

Taller "Del objetivo de negocio al sitio medible" · Marketing Analytics

> Trabajo académico. BTG Pactual es un negocio real, pero el producto de leasing, las metas y las cifras proyectadas son supuestos del ejercicio. No es un sitio oficial del banco.

## 0. Equipo y proyecto

| Campo | Respuesta |
|---|---|
| Integrantes | Martina Figueroa |
| Nombre del proyecto | Leasing Empresas BTG Pactual |
| Negocio (real o ficticio) | Real (BTG Pactual Chile, área Corporate Lending); producto de leasing ficticio |
| URL final del sitio | https://martinajesusfigueroacross-droid.github.io/marketinganaitycs/ |

## 1. Contexto de negocio

**¿Qué vende u ofrece la organización?**
BTG Pactual Chile es un banco de inversión. Su área de Corporate Lending ofrece créditos bilaterales y sindicados, boletas y pólizas de garantía, project finance, confirming y factoring. Este proyecto supone el lanzamiento de un nuevo producto: **leasing financiero para empresas**.

**¿Qué problema del cliente resuelve?**
Permite a las empresas usar maquinaria, vehículos o inmuebles sin inmovilizar capital, pagando en cuotas ajustadas a sus flujos, con opción de compra al final.

**¿Por qué existe este sitio? ¿Qué cambia si funciona bien?**
El leasing es un producto nuevo y los clientes aún no saben que BTG lo ofrece. El sitio genera los primeros contactos comerciales (leads) para un ejecutivo de Corporate Lending. Si funciona, acelera la meta SMART del producto: **una cartera de US$100 millones en leasing al 31 de diciembre de 2027, con al menos 30% de las operaciones originadas por cross-selling y morosidad bajo 1,5%**.

## 2. Modelo de medición

| Nivel | Respuesta |
|---|---|
| Objetivo de negocio | Captar leads de empresas interesadas en leasing para alimentar la cartera del nuevo producto. |
| Meta del sitio | Que el visitante pida contacto con un ejecutivo (clic en "Hablar con un ejecutivo"). |
| KPI | Tasa de sesiones con el evento clave `clic_cta_principal` (tasa de eventos clave de la sesión en GA4). |
| Target | 5% de las sesiones con clic en el CTA en una semana. Fundamento: las landing pages B2B suelen convertir entre 2% y 5%; al difundir a contactos cercanos, apuntamos al extremo alto (supuesto). |
| Segmentos | Canal de adquisición (WhatsApp, Instagram, LinkedIn, vía UTM), dispositivo (móvil vs. escritorio) y fuente de campaña (`taller_ma`). |

**Hipótesis:** LinkedIn traerá menos sesiones que WhatsApp, pero con mayor tasa de clic en el CTA, porque llega a un público profesional más cercano al cliente objetivo.

## 3. Audiencia

| Campo | Respuesta |
|---|---|
| ¿Quién es el visitante principal? | Gerente de finanzas, CFO o dueño de una empresa mediana o grande en Chile. Conoce el financiamiento tradicional, pero no sabe que BTG ofrece leasing. |
| ¿Qué tarea intenta resolver? | Financiar un activo (maquinaria, flota, inmueble) sin descapitalizar la empresa, y comparar condiciones. |
| ¿Desde dónde llega? | LinkedIn, WhatsApp (recomendación) e Instagram. En un caso real, también por su ejecutivo de BTG y búsqueda en Google. |
| ¿Qué dispositivo usará? | Móvil para el primer contacto desde redes; escritorio para evaluar en detalle. |
| Principales objeciones | ¿Tiene BTG experiencia en leasing si recién lo lanza? ¿Cuánto me costará la cuota? ¿Cuánto tarda la aprobación? ¿Qué pasa con el activo al final? |

## 4. Mensaje

**Propuesta de valor:** Leasing para que tu empresa crezca sin inmovilizar capital, con estructuras a la medida y el respaldo del equipo de Corporate Lending de BTG Pactual.

**Argumentos de apoyo (en orden de importancia):**
1. Sin inmovilizar capital: usas el activo desde el primer día y pagas en cuotas.
2. Flexibilidad y agilidad: estructuración a la medida y aprobación eficiente.
3. Un solo banco: coordinación con Investment Banking, Sales & Trading y Wealth Management.

**Evidencia que reduce el riesgo percibido:** cifras reales de Corporate Lending publicadas por BTG Pactual Chile (aumento de 19,6% en colocaciones comerciales respecto de 2024 y cartera de créditos de US$3.868 MM en 2025) y aprobación de riesgo con participación del senior management. El producto de leasing en sí es un supuesto del ejercicio.

## 5. Acción y medición

| Campo | Respuesta |
|---|---|
| CTA principal (texto exacto) | Hablar con un ejecutivo |
| ¿Qué ocurre al hacer clic? | Lleva a la sección interna de contacto (formulario) en la misma página. |
| URL de destino del CTA | `#contacto` (sección interna de `index.html`) |
| CTA secundario | "Simular mi leasing" (lleva al simulador, `#simula`) |
| Nombre del evento en GA4 | `clic_cta_principal` |
| Relación con el KPI | Cada clic en el CTA (header, "Solicitar evaluación" del simulador y "Enviar solicitud" del formulario) envía `clic_cta_principal` con el parámetro `ubicacion`. El evento está marcado como evento clave, y su tasa por sesión es el KPI de la sección 2. |

Medición: GA4, ID `G-TDN87RHB47`, etiqueta en el `<head>` de `index.html` y script del evento antes de `</body>`.

## 6. Arquitectura de información

| Orden | Sección | Propósito | Contenido principal | ¿CTA? |
|---|---|---|---|---|
| 1 | Hero / encabezado | Que entienda en segundos qué es y para quién | Logo, menú, título, bajada, imagen del activo | Sí ("Hablar con un ejecutivo", "Simular mi leasing") |
| 2 | Tipos de leasing | Mostrar que el producto calza con su necesidad | Maquinaria, vehículos, inmobiliario, leaseback | Enlaces "Ver más" |
| 3 | Cómo funciona | Reducir la duda sobre el proceso y los plazos | 4 pasos: necesidad, evaluación, propuesta, firma | No |
| 4 | Beneficios | Responder "¿por qué BTG?" | Sin inmovilizar capital, flexibilidad, un solo banco, opción de compra | No |
| 5 | Cifras | Dar credibilidad a un producto nuevo | Cifras reales de Corporate Lending | No |
| 6 | Simulador | Resolver la objeción del costo | Tipo de activo, valor, plazo, pie, cuota estimada | Sí ("Solicitar evaluación") |
| 7 | Contacto | Concretar la conversión | Formulario de contacto empresarial | Sí ("Enviar solicitud") |
| 8 | Pie de página | Cierre e información legal | Dirección, enlaces, texto legal | No |

El CTA principal aparece al inicio (header) y al final (simulador y contacto). Las secciones 3 a 6 responden las objeciones de la audiencia antes de pedir la acción.

## 7. Restricciones del ejercicio

- El sitio es una sola página (`index.html`) con HTML, CSS y JavaScript en el mismo archivo. `panel.html` es un anexo: el panel interno que mide el objetivo SMART.
- No se envían datos personales (nombre, correo, RUT) a GA4 ni en las URL.

## Difusión con UTM

| Canal | URL |
|---|---|
| WhatsApp | https://martinajesusfigueroacross-droid.github.io/marketinganaitycs/?utm_source=whatsapp&utm_medium=mensajeria&utm_campaign=taller_ma |
| Instagram | https://martinajesusfigueroacross-droid.github.io/marketinganaitycs/?utm_source=instagram&utm_medium=social&utm_campaign=taller_ma |
| LinkedIn | https://martinajesusfigueroacross-droid.github.io/marketinganaitycs/?utm_source=linkedin&utm_medium=social&utm_campaign=taller_ma |

### Registro de difusión

| Canal | Fecha | Audiencia aproximada | URL con UTM |
|---|---|---|---|
| | | | |
| | | | |

Nota: los 3 clics registrados el 14-10-2026 fueron pruebas de instalación y no se consideran en el análisis.
