# Energy-as-a-Service para viviendas en Madrid  
## Domótica híbrida *edge + cloud* para ahorro energético en climatización

**Autor:** Gonzalo Pacheco Agredano  
**Universidad:** Universidad Rey Juan Carlos (URJC) – EIF  
**Asignatura:** Comunicaciones Sectoriales  

---

## Descripción del proyecto

Este repositorio recoge el desarrollo de un trabajo académico con formato de **póster científico** centrado en el diseño de una solución de **Energy-as-a-Service** para viviendas en Madrid. La propuesta plantea una arquitectura domótica híbrida **edge + cloud** orientada al ahorro energético en sistemas de climatización (**HVAC**), manteniendo al mismo tiempo criterios de **privacidad, resiliencia, eficiencia operativa y viabilidad económica**.

El proyecto se aborda desde una perspectiva técnica de **telecomunicaciones**, poniendo el foco en la selección de protocolos de comunicación, la topología de red doméstica, el reparto funcional entre procesamiento local y servicios en la nube, la seguridad de las comunicaciones y la continuidad de servicio ante fallos de conectividad.

---

## Pregunta de investigación

> **¿Qué arquitectura domótica basada en edge + cloud, y qué conjunto mínimo de sensores y actuadores, permiten maximizar el ahorro energético en HVAC en una vivienda tipo de Madrid, manteniendo la privacidad y un modelo de negocio viable por suscripción?**

---

## Objetivo

Diseñar una arquitectura IoT doméstica que permita optimizar el funcionamiento de la climatización mediante:

- **control inteligente de HVAC**,  
- **detección de presencia y ocupación**,  
- **monitorización eléctrica del consumo**,  
- **procesamiento local de eventos sensibles**,  
- y **servicios cloud complementarios** para analítica, soporte y mantenimiento.

El objetivo final es plantear una solución técnica defendible que combine **ahorro energético**, **confort del usuario**, **protección de datos** y **escalabilidad como servicio**.

---

## Alcance del trabajo

El caso de uso se limita a una **vivienda tipo en Madrid**, en un entorno climático templado, con el propósito de reducir el consumo asociado a climatización sin degradar la experiencia del usuario.

### Incluido en la propuesta
- HVAC inteligente mediante termostato o sistema de control compatible.
- Sensores de presencia/ocupación para activación de modos de funcionamiento.
- Monitorización eléctrica para evaluar el impacto real de la automatización.
- Arquitectura híbrida con funciones distribuidas entre **edge** y **cloud**.
- Definición de KPIs técnicos y económicos.

### No incluido
- Algoritmos avanzados de inteligencia artificial o aprendizaje automático complejo.
- Integración con fotovoltaica, vehículo eléctrico o gestión energética global del hogar.
- Automatización general de otros subsistemas domésticos como iluminación o persianas, salvo como posible línea futura.

---

## Arquitectura propuesta

La solución se basa en una arquitectura **híbrida edge + cloud**.

### Capa edge (local, en la vivienda)
En el hogar se despliega un **hub local** encargado de:
- recibir datos de sensores,
- aplicar reglas de control,
- tomar decisiones inmediatas sobre el sistema HVAC,
- y mantener operativas las funciones críticas aunque se pierda la conexión a Internet.

Esta capa aporta:
- **baja latencia**,  
- **mayor privacidad**,  
- **autonomía local**,  
- y **resiliencia ante fallos de conectividad**.

### Capa cloud (servicios remotos)
La nube se reserva para tareas no críticas en tiempo real, como:
- visualización de datos y dashboards,
- analítica agregada,
- mantenimiento remoto,
- actualizaciones,
- generación de informes,
- alertas avanzadas,
- y benchmarking anonimizado.

Esta separación funcional permite equilibrar **eficiencia operativa**, **seguridad**, **escalabilidad** y **experiencia de usuario**.

---

## Tecnologías y comunicaciones

Uno de los ejes principales del proyecto es la definición de una solución coherente desde el punto de vista de **telecomunicaciones**.

### Sensores de presencia y variables ambientales
Se propone el uso de **Zigbee** o **Thread**, por tratarse de tecnologías adecuadas para entornos IoT de bajo consumo, con capacidad de operar en **topologías malladas**, mejorando la cobertura y robustez dentro de la vivienda.

### Monitorización eléctrica
Para la monitorización energética se considera el uso de **Wi-Fi** o **Ethernet**, ya que en este caso prima la **fiabilidad**, la **disponibilidad continua** y la facilidad de integración con sistemas de visualización y registro.

### Control HVAC
El control de climatización se plantea mediante:
- API del termostato,
- integración con una pasarela local,
- o interfaz compatible con el sistema existente.

El criterio técnico clave en este punto es la **interoperabilidad**.

---

## Enfoque técnico de telecomunicaciones

Aunque la aplicación final está orientada al ahorro energético, el proyecto se construye sobre decisiones propias del ámbito teleco, entre ellas:

- selección de **protocolos IoT** según requisitos de consumo, cobertura y tráfico,
- diseño de **topologías de red doméstica**,
- reparto funcional entre **procesamiento local** y **servicios cloud**,
- análisis de **latencia**, **disponibilidad** y **continuidad de servicio**,
- medidas de **seguridad y cifrado** en las comunicaciones,
- y criterios de **privacidad** y **minimización de datos**.

Por tanto, la propuesta no se limita a una automatización doméstica genérica, sino que se formula como una **arquitectura de comunicaciones aplicada a eficiencia energética residencial**.

---

## Seguridad, privacidad y resiliencia

La propuesta incorpora criterios de diseño orientados a la protección del usuario y a la robustez del servicio:

- **procesamiento local** de eventos sensibles, como presencia u ocupación,
- **minimización de los datos** enviados a la nube,
- **cifrado de comunicaciones** y autenticación de dispositivos,
- control del usuario sobre la información compartida,
- y mantenimiento de las funciones críticas de climatización aunque falle la conexión a Internet.

Este último punto justifica especialmente el uso de una arquitectura **edge + cloud**, donde la nube complementa, pero no sustituye, el control local.

---

## Modelo de negocio

El proyecto plantea un modelo de **Energy-as-a-Service** basado en:

- **instalación inicial** del sistema,
- y una **cuota mensual** que cubra plataforma, soporte, mantenimiento y actualizaciones.

### Propuesta de valor
- ahorro energético,
- mantenimiento del confort,
- visibilidad del consumo,
- soporte técnico,
- y privacidad como elemento diferenciador.

### Posibles niveles de servicio

**Basic**
- reglas de automatización,
- dashboard básico,
- soporte estándar.

**Plus**
- optimización por hábitos,
- alertas avanzadas,
- informes mensuales,
- analítica ampliada.

---

## KPIs del proyecto

Para evaluar la viabilidad técnica y económica de la propuesta, se definen los siguientes indicadores:

1. **Ahorro energético en HVAC (%)**  
   Estimación del ahorro obtenido frente a una operación convencional.

2. **Payback**  
   Tiempo necesario para recuperar la inversión inicial en función del ahorro estimado y de la cuota del servicio.

3. **Consumo propio del sistema domótico**  
   Energía consumida por sensores, hub y comunicaciones, para verificar que el ahorro neto sigue siendo positivo.

4. **Privacidad**  
   Tipo y volumen de datos que salen de la vivienda, así como el nivel de procesamiento local de información sensible.

5. **Disponibilidad del servicio**  
   Capacidad del sistema para seguir funcionando localmente en ausencia de conectividad con la nube.

---

## Figuras principales del póster

El póster asociado a este proyecto se apoya en varias figuras clave:

- **Diagrama de arquitectura end-to-end**  
  Sensores → hub local → HVAC → cloud/app

- **Comparativa edge vs cloud**  
  Reparto funcional, privacidad, latencia y resiliencia

- **Tabla BOM + CAPEX/OPEX**  
  Componentes principales y estimación económica

- **Gráfico de escenarios de ahorro**  
  Escenario conservador, medio y optimista

- **Customer journey del servicio**  
  Instalación → operación → informes → soporte

---

## Resultados esperados

A través de este trabajo se espera demostrar que:

- una arquitectura híbrida bien diseñada puede reducir el consumo energético de climatización sin necesidad de recurrir a soluciones excesivamente complejas;
- el uso combinado de **edge computing**, protocolos IoT adecuados y servicios cloud complementarios permite construir una solución doméstica robusta y escalable;
- y el modelo puede sostenerse como servicio de suscripción si existe equilibrio entre ahorro, confort, privacidad y coste.

---

## Estructura del repositorio

```text
.
├── README.md
├── poster/
│   ├── poster.tex
│   ├── poster.pdf
│   └── figures/
├── docs/
│   ├── guion_exposicion.md
│   ├── notas_metodologia.md
│   └── referencias.bib
└── assets/
    ├── logo_urjc.png
    └── qr_repo.png