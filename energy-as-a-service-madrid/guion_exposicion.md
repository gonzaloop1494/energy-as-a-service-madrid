# Guion de exposición  
## Energy-as-a-Service para viviendas en Madrid: domótica híbrida *edge + cloud* para ahorro energético en climatización

**Autor:** Gonzalo Pacheco Agredano  
**Universidad:** Universidad Rey Juan Carlos (URJC) – EIF  
**Asignatura:** Comunicaciones Sectoriales  

---

## 1. Introducción

Buenos días.  
Soy **Gonzalo Pacheco Agredano** y en este trabajo presento una propuesta de **Energy-as-a-Service para viviendas en Madrid**, basada en una arquitectura domótica híbrida **edge + cloud** orientada al ahorro energético en climatización.

El problema de partida es que, en una vivienda, los sistemas de calefacción y aire acondicionado representan una parte muy importante del consumo energético. Sin embargo, en muchos casos su funcionamiento sigue siendo poco eficiente, porque se basa en horarios fijos, escasa adaptación a la ocupación real de la vivienda y poca visibilidad del consumo.

A partir de esta situación, el trabajo plantea una solución con enfoque técnico de telecomunicaciones: una arquitectura IoT que combine **sensores**, **comunicaciones inalámbricas**, **procesamiento local**, **servicios en la nube** y **monitorización energética**, con el objetivo de reducir el consumo sin perder confort.

---

## 2. Pregunta de investigación

La pregunta de investigación que guía el proyecto es la siguiente:

> **¿Qué arquitectura domótica basada en edge + cloud, y qué conjunto mínimo de sensores y actuadores, permiten maximizar el ahorro energético en HVAC en una vivienda tipo de Madrid, manteniendo la privacidad y un modelo de negocio viable por suscripción?**

Esta pregunta permite abordar el problema desde tres perspectivas complementarias:

- **perspectiva técnica**,  
- **perspectiva económica**,  
- **y perspectiva de comunicaciones y tratamiento de datos**.  

---

## 3. Objetivo del trabajo

El objetivo principal es diseñar una arquitectura IoT doméstica que permita optimizar el funcionamiento del sistema de climatización mediante:

- control inteligente de HVAC,  
- detección de presencia y ocupación,  
- monitorización eléctrica del consumo,  
- procesamiento local de eventos sensibles,  
- y servicios cloud para supervisión, analítica y mantenimiento.

La finalidad es obtener una propuesta que combine:

- **ahorro energético**,  
- **mantenimiento del confort**,  
- **protección de la privacidad**,  
- **resiliencia ante fallos de conectividad**,  
- y **viabilidad como servicio por suscripción**.  

---

## 4. Alcance del proyecto

Para que el trabajo sea realista y defendible, el alcance queda acotado a una **vivienda tipo en Madrid**, considerando un clima templado y centrando el análisis en el ahorro energético asociado a climatización.

### 4.1. Elementos incluidos

Los tres pilares funcionales incluidos en la propuesta son:

1. **HVAC inteligente**  
   Control del sistema de calefacción y/o aire acondicionado mediante termostato o sistema equivalente.

2. **Presencia y ocupación**  
   Uso de sensores para adaptar el funcionamiento del HVAC a la ocupación real de la vivienda, activando modos como *comfort*, *eco* o *away*.

3. **Monitorización eléctrica**  
   Medición del consumo energético total o por circuito para evaluar el impacto real de la automatización.

### 4.2. Elementos no incluidos

Para mantener el foco del proyecto, se excluyen de forma explícita los siguientes aspectos:

- algoritmos avanzados de inteligencia artificial,
- integración con energía fotovoltaica o vehículo eléctrico,
- automatización general de otros sistemas domésticos como iluminación o persianas, salvo como posible ampliación futura.

---

## 5. Enfoque técnico de telecomunicaciones

Aunque el caso de uso se sitúa en el ámbito de la eficiencia energética, el núcleo del proyecto es claramente de **telecomunicaciones**.

El diseño se apoya en decisiones técnicas relacionadas con:

- selección de **protocolos de comunicación**,
- definición de **topologías de red doméstica**,
- reparto funcional entre **edge** y **cloud**,
- control de **latencia**,
- **seguridad de las comunicaciones**,
- **privacidad de los datos**,
- y **disponibilidad del sistema** ante fallos de conectividad.

Por tanto, el valor técnico del trabajo no está solo en automatizar una vivienda, sino en diseñar una **arquitectura de comunicaciones doméstica robusta, segura y eficiente**.

---

## 6. Arquitectura propuesta

La solución propuesta se basa en una arquitectura **híbrida edge + cloud**.

### 6.1. Capa edge

En el interior de la vivienda se plantea un **hub local** o controlador doméstico encargado de:

- recibir información de sensores,
- ejecutar reglas de control,
- tomar decisiones rápidas,
- almacenar de forma local datos sensibles,
- y garantizar el funcionamiento básico del sistema aunque falle Internet.

Este enfoque local permite:

- reducir la latencia,
- proteger mejor la privacidad,
- y mantener la operatividad del sistema en caso de pérdida de conectividad externa.

### 6.2. Capa cloud

La nube se utiliza para funciones complementarias no críticas en tiempo real, como por ejemplo:

- dashboards y visualización de datos,
- analítica agregada,
- mantenimiento remoto,
- actualizaciones de la plataforma,
- generación de informes,
- alertas avanzadas,
- y benchmarking anónimo.

De este modo, la arquitectura combina:

- **edge** para decisiones inmediatas, privacidad y resiliencia,
- y **cloud** para escalabilidad, supervisión y servicios avanzados.

---

## 7. Tecnologías de comunicación

Uno de los apartados más importantes del trabajo es justificar la elección de tecnologías desde el punto de vista teleco.

### 7.1. Sensores de presencia y variables ambientales

Para los sensores de presencia y variables ambientales, la propuesta prioriza el uso de **Zigbee** o **Thread**.

La elección se basa en que estas tecnologías:

- están orientadas a entornos IoT,
- tienen **bajo consumo energético**,
- y permiten una **topología mallada**, mejorando la cobertura y la robustez dentro de la vivienda.

Además, resultan adecuadas para sensores que transmiten poco tráfico y que, en muchos casos, deben funcionar durante largos periodos con bajo consumo.

### 7.2. Monitorización eléctrica

Para la monitorización eléctrica se plantea el uso de **Wi-Fi** o **Ethernet**, ya que en este caso prima más la **fiabilidad**, la continuidad del servicio y la facilidad de integración que el ultra bajo consumo.

Se trata normalmente de dispositivos alimentados desde la red eléctrica, por lo que tiene sentido priorizar una conectividad más estable y con mayor capacidad.

### 7.3. Control HVAC

El control del sistema HVAC puede realizarse mediante:

- una API del termostato,
- una pasarela local,
- o una integración compatible con el sistema ya instalado.

Aquí el criterio técnico principal es la **interoperabilidad**, para evitar depender de soluciones cerradas y facilitar la integración en una arquitectura híbrida.

---

## 8. Seguridad, privacidad y resiliencia

Un aspecto especialmente importante del trabajo es que la propuesta no solo persigue ahorrar energía, sino hacerlo con criterios de **seguridad**, **protección de datos** y **continuidad de servicio**.

Los principales elementos de este enfoque son:

- procesamiento local de eventos sensibles, como la presencia en la vivienda,
- minimización de los datos enviados a la nube,
- cifrado de comunicaciones,
- autenticación de dispositivos,
- control del usuario sobre la información compartida,
- y mantenimiento de las funciones esenciales aunque no haya acceso a Internet.

Esto permite reforzar uno de los principales argumentos del proyecto:  
la nube aporta valor, pero la funcionalidad crítica del sistema debe mantenerse en local.

---

## 9. Modelo de negocio

El modelo planteado es un servicio de **Energy-as-a-Service**, basado en una combinación de:

- **coste inicial de instalación**,  
- y **cuota mensual** por uso de la plataforma y soporte.  

La propuesta de valor se apoya en cuatro elementos principales:

- ahorro energético,
- confort,
- seguimiento del consumo,
- y privacidad como factor diferencial.

### 9.1. Posibles niveles de servicio

**Basic**
- reglas de automatización,
- dashboard básico,
- soporte estándar.

**Plus**
- optimización basada en hábitos,
- alertas avanzadas,
- informes mensuales,
- analítica ampliada.

De esta manera, el proyecto no solo tiene una dimensión técnica, sino también una dimensión de servicio y explotación económicamente defendible.

---

## 10. KPIs del proyecto

Para evaluar la propuesta, el trabajo se apoya en una serie de indicadores clave.

### 10.1. Ahorro energético en HVAC

Permite cuantificar la reducción del consumo respecto a una operación convencional del sistema de climatización.

### 10.2. Payback

Indica el tiempo necesario para recuperar la inversión inicial a partir del ahorro energético conseguido.

### 10.3. Consumo propio del sistema domótico

Mide la energía consumida por sensores, hub y comunicaciones, para comprobar que el ahorro neto sigue siendo positivo.

### 10.4. Privacidad

Evalúa qué tipo de datos salen de la vivienda, en qué volumen y con qué grado de tratamiento local.

### 10.5. Disponibilidad

Analiza qué funciones siguen operativas cuando falla la conectividad con la nube, lo que permite justificar la ventaja del enfoque edge.

---

## 11. Figuras clave del póster

El póster debe apoyarse en un número reducido de figuras, pero muy explicativas. Las más importantes son las siguientes:

### 11.1. Arquitectura end-to-end

Diagrama del flujo completo del sistema:

**sensores → hub local → HVAC → cloud/app**

Esta figura permitirá explicar de forma visual la topología del sistema y la relación entre sus elementos.

### 11.2. Comparativa edge vs cloud

Figura orientada a mostrar qué funciones se realizan localmente y cuáles se delegan a la nube, destacando latencia, privacidad y resiliencia.

### 11.3. Tabla BOM + CAPEX/OPEX

Tabla con los componentes principales del sistema y su estimación económica, vinculando arquitectura técnica con viabilidad de negocio.

### 11.4. Gráfico de escenarios de ahorro

Comparativa visual entre un escenario conservador, uno medio y uno optimista en términos de ahorro energético.

### 11.5. Customer journey

Representación del ciclo de servicio:

**instalación → operación → reportes → soporte**

Esta figura ayuda a mostrar cómo se traduce la solución técnica en una experiencia real de servicio.

---

## 12. Qué se espera demostrar

Con este trabajo se espera demostrar tres ideas principales:

1. Que una arquitectura domótica híbrida bien diseñada puede reducir el consumo energético en climatización sin necesidad de recurrir a soluciones excesivamente complejas.

2. Que desde el punto de vista de telecomunicaciones, la combinación de protocolos IoT adecuados, procesamiento local y servicios cloud complementarios permite construir una solución doméstica robusta, escalable y eficiente.

3. Que el modelo puede ser viable como servicio por suscripción si existe equilibrio entre ahorro, confort, privacidad y coste.

---

## 13. Conclusión

En conclusión, este trabajo desarrolla una propuesta de **domótica híbrida para viviendas en Madrid** centrada en el ahorro energético en climatización mediante una arquitectura IoT con enfoque de telecomunicaciones.

La solución combina:

- sensores de presencia,
- monitorización eléctrica,
- control HVAC,
- procesamiento distribuido entre edge y cloud,
- y criterios de seguridad, privacidad y disponibilidad.

Como resultado, se obtiene una propuesta técnicamente defendible, escalable y compatible con un modelo **Energy-as-a-Service** basado en suscripción, donde el valor no solo está en el ahorro energético, sino también en la robustez de la arquitectura de comunicaciones y en la gestión segura de los datos.

---

## 14. Cierre oral

Muchas gracias.