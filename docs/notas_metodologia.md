# Notas de metodologia

## Alcance

El trabajo se centra en una vivienda tipo en Madrid y en el consumo asociado a climatizacion residencial. La propuesta no aborda fotovoltaica, vehiculo electrico ni automatizacion general de otros subsistemas domesticos.

## Arquitectura

La solucion se plantea como una arquitectura hibrida:

- **Edge local:** hub domestico para decisiones rapidas, reglas HVAC, privacidad y continuidad si falla Internet.
- **Cloud:** historicos, dashboards, informes, alertas, mantenimiento y actualizaciones.

El criterio principal es mantener en local las funciones criticas y enviar a la nube solo datos agregados o no sensibles.

## Tecnologias consideradas

- **Matter sobre Thread / Zigbee:** sensorizacion de bajo consumo, red mallada y buena cobertura interior.
- **Wi-Fi / Ethernet:** monitorizacion electrica y equipos alimentados por red.
- **OpenTherm / rele / pasarela local:** integracion con el sistema HVAC existente.
- **IP / Cloud:** informes, analitica, mantenimiento y actualizaciones.

## Indicadores

Los KPIs utilizados en el poster son:

- ahorro estimado en HVAC,
- payback orientativo,
- consumo propio del sistema,
- latencia local,
- disponibilidad,
- privacidad.

## Supuestos

Los rangos de ahorro son indicativos y se apoyan en referencias externas como DOE, ENERGY STAR y Turley et al. (Energies, 2020). No corresponden a medidas experimentales propias.

El modelo economico combina:

- coste inicial de kit e instalacion,
- cuota mensual de plataforma, soporte e informes,
- ahorro esperado,
- y payback variable segun escenario.
