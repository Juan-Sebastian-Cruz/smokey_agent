# Guía de Mejores Prácticas para el Agente de Finanzas "Smokey"

Este documento está diseñado para ayudar a Matías Páez a optimizar su interacción con el **Agente de Finanzas Smokey** y obtener las respuestas y registros más rápidos y precisos.

---

## 1. La Regla de Oro: Claridad y Precisión

El Agente Smokey es un sistema de inteligencia artificial que opera bajo reglas estrictas para garantizar la precisión de tus datos financieros.

**Instrucciones Vagas \-&gt; Respuestas Vagas o Demoras.**

Para una interacción efectiva, evita ser ambiguo. Proporciona el máximo contexto posible:

| En lugar de (Vago) | Usa (Preciso) |
| :--- | :--- |
| "dime mi balance" | "Dime mi flujo de caja neto del mes de octubre." |
| "registra un gasto" | "Registra un egreso de **$15.000** en la categoría **Entretenimiento** con la **Tarjeta Débito Santander**, fue el **25/10/2025**." |
| "¿cuánto me queda de presupuesto?" | "¿Cuánto presupuesto me queda disponible para **Transporte** este mes?" |

---

## 2. Recomendación de Velocidad: Audio (Mensajes de Voz)

El agente está configurado para **transcribir automáticamente tus mensajes de voz**. Esto es a menudo **más rápido** que escribir, especialmente para registros con múltiples datos.

> **Práctica Recomendada:** En lugar de escribir un mensaje largo, simplemente envía una nota de voz con todos los detalles.

| Función | Ejemplo de Audio/Voz |
| :--- | :--- |
| **Registro de Egreso** | "Smokey, gasté 30.000 pesos en **Gas** con la **Débito Santander** hoy." |
| **Consulta** | "Necesito un resumen de mi gasto en **Alimentación** de los últimos 7 días." |

---

## 3. Protocolo de Interacción para Registros

El Agente *Registrador-Smokey* te guiará de forma interactiva si falta algún dato. Para evitar la conversación de ida y vuelta, intenta incluir toda la información requerida en tu primer mensaje de registro.

### A. Categorías Oficiales (Máxima Precisión)

Para garantizar la consistencia de tus datos, los valores para **Categoría**, **Cuenta Bancaria** y **Fuente de Ingreso** deben coincidir **exactamente** con las listas. Si el valor proporcionado es similar, el agente intentará usar la versión oficial (Ej: "Santander Débito" $\to$ "Débito Santander"), pero usar el nombre oficial garantiza la rapidez.

| Tipo de Dato | Listado de Valores Oficiales |
| :--- | :--- |
| **Categorías Válidas** (Para Egresos) | `Inversiones`, `Gastos Domésticos`, `Gas`, `Compromisos Financieros`, `Suscripciones`, `Artículos personales`, `Entretenimiento`, `Regalos` |
| **Cuentas Bancarias** | `Crédito Santander`, `Débito Santander`, `Crédito Falabella`, `Crédito Banco de Chile` |
| **Fuentes de Ingreso** | `Uber`, `Sence` |
| **Deudas Válidas** | `Tarjeta de Crédito Falabella`, `Tarjeta de Crédito Santander`, `Tarjeta de Crédito Banco de Chile`, `Línea de Crédito Banco de Chile`, `Cae` |

### B. Datos Requeridos

| Tipo de Registro | Parámetros Mínimos Requeridos |
| :--- | :--- |
| **Ingreso** | Fuente de Ingreso, Monto, Cuenta Bancaria, Fecha (DD/MM/AAAA) |
| **Egreso** | Detalle, Monto gastado, Categoría, Fecha (DD/MM/AAAA), Cuenta Bancaria |
| **Pago de Deuda** | Monto, Fecha (DD/MM/AAAA), Deuda (Nombre oficial) |
| **Emisión de Deuda** | Detalle, Cuotas, Monto Total, Interés Mensual, Deuda (Nombre oficial) |

> **Nota sobre Formato:** El agente formateará automáticamente los montos a **numérico** y las fechas a **DD/MM/AAAA**. Si no proporcionas una fecha, usará la fecha actual.

---

## 4. Protocolo de Interacción para Consultas

El Agente *Consultor-Smokey* está especializado en análisis. Para obtener la mejor respuesta, sé específico sobre el **período** y la **métrica**.

### A. Para Consultas (Análisis y Resúmenes)

1.  **Especifica el tiempo:** Si no mencionas una fecha o período, el agente **asumirá el mes calendario actual**.
    *   *Ej:* "Analiza mis gastos de **septiembre**" o "dame mi flujo de caja de **este mes**".
2.  **Pide la métrica clave:** El agente puede calcular métricas avanzadas (Net Worth, Ratio de Ahorro, DTI).
    *   *Ej:* "¿Cuál es mi **Debt-to-Income Ratio** de este trimestre?"

### B. Aprovechando la Memoria

El agente tiene una **Memoria a Largo Plazo** (Google Docs) que usa para recordar tus patrones y tendencias financieras.

> **Importante:** Solicitar un análisis profundo o un resumen periódico (Ej: Resumen Mensual) activa el protocolo de actualización de memoria del agente, mejorando el contexto para futuras recomendaciones.

---

## 5. Gestión de Expectativas (Tiempos de Respuesta)

El flujo de trabajo es complejo (transcripción de audio, enrutamiento, análisis de IA y registro/consulta en bases de datos). Por ello, los tiempos de respuesta varían:

| Tipo de Solicitud | Tiempo Estimado |
| :--- | :--- |
| **Registro Sencillo** (con todos los datos) | 5 - 15 segundos |
| **Consulta Simple** (Ej: "¿Cuánto gasté en Gas?") | 10 - 20 segundos |
| **Consulta o Análisis Complejo** (Ej: "Resumen Mensual" o DTI) | 20 - 30 segundos |
| **Interacción** (Respondiendo a una pregunta de Smokey) | < 10 segundos |

---

## 6. Proceso Automático: Apple Wallet

El agente está configurado para recibir notificaciones automáticas de transacciones (Apple Wallet) y registrar los egresos de forma pasiva.

*   **Tu Rol:** Ninguno. El registro es automático. En caso de requerir una clasificación o detalle adicional, el agente iniciará una conversación contigo.
