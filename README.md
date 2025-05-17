# Sistema Tunomático

**Nombre:** Hilary Varela

**Fecha:** 16 de mayo de 2025  

# Sistema De Gestion De Turnos 

## Descripción General del Sistema

El Sistema Tunomático es una solución integral para la gestión automatizada de turnos en entornos de alta demanda como hospitales, bancos o instituciones públicas. Su arquitectura se basa en patrones de diseño que garantizan escalabilidad, mantenibilidad y adaptabilidad a diversos entornos tecnológicos. El sistema incluye funcionalidades clave como generación de turnos categorizados, notificaciones inteligentes, integración con sistemas externos y visualización en tiempo real.

##  Aspectos Clave del Sistema Tunomático:
- Arquitectura Basada en Patrones de Diseño

  * **Singleton:** Garantiza una única instancia global para la gestión centralizada de turnos, evitando conflictos en entornos multiusuario.
  * **Prototype:** Permite clonar plantillas de turnos preconfigurados (ej: consulta médica, trámite prioritario), acelerando su creación.
  * **Adapter:**   Facilita la integración con tecnologías heterogéneas (pantallas LED, sistemas legacy) mediante interfaces estandarizadas.
  * **Bridge:**    Separa la lógica de notificaciones de los canales concretos (SMS, email, app), permitiendo extensibilidad sin modificar el núcleo del sistema.

## Funcionalidades Esenciales

### Generación de Turnos Categorizados:

- Asignación automática basada en tipo de servicio (urgente, preferencial, estándar).
- Personalización de parámetros (duración, prioridad, recursos asignados).

### Notificaciones Inteligentes:

- Adaptación al historial de preferencias del usuario.

### Visualización en Tiempo Real:

- Información contextual: tiempo estimado de espera, estación asignada.

## Escalabilidad y Mantenibilidad

- Diseño modular que permite añadir nuevos servicios sin afectar el sistema existente.
- Gestión eficiente de recursos en escenarios de alta concurrencia (ej: horas pico en bancos).
- Capacidad de distribuir carga entre múltiples estaciones de atención.

## Gestión de Datos y Reportes

- Registro automático de métricas operativas: tiempos de espera, tasa de abandono, eficiencia por estación.

## Diagrama de caso de uso

Un sistema de gestión de turnos donde clientes solicitan servicios, operadores los atienden y administradores configuran y monitorean el proceso, con funcionalidades clave como notificaciones automáticas, registro de estadísticas y reasignación de turnos no atendidos.

![Captura de pantalla 2025-05-16 213633](https://github.com/user-attachments/assets/024bc419-cd9c-4611-ade0-9609736bbc19)

## Diagrama de clases 

Diseñado con patrones de diseño como Singleton, Prototype, Adapter y Bridge para asegurar una arquitectura flexible y mantenible. El componente central, GestorTurnos, controla la creación, modificación y seguimiento de los turnos, garantizando una única instancia del sistema. Los turnos pueden clonarse fácilmente mediante plantillas (Prototype), mientras que las notificaciones a los usuarios se gestionan de forma desacoplada gracias al patrón Bridge, permitiendo el envío por distintos canales como SMS, email o app. Además, el sistema puede integrarse con diferentes tecnologías de visualización mediante Adapter, y ofrece funcionalidades adicionales como reasignación de turnos no atendidos y registro de estadísticas para análisis posterior, cubriendo así todo el ciclo operativo desde la solicitud hasta la atención y monitoreo.

![clasesssssss](https://github.com/user-attachments/assets/ee0d4a91-8955-48c3-8313-e5b60d5434fa)

## Diagrama de implementacion

El diagrama de implementación del Sistema Tunomático muestra una arquitectura modular donde el GestorTurnos central, ubicado en el servidor principal, coordina la generación y gestión de turnos. Los operadores y administradores acceden desde terminales separados, mientras que las notificaciones se envían desde un servidor dedicado utilizando distintos canales (SMS, email, app) mediante el patrón Bridge. La visualización de turnos se realiza a través de un adaptador que conecta con pantallas externas, y la base de datos se encuentra en un servidor independiente para un manejo seguro y centralizado de la información.

![implementacion](https://github.com/user-attachments/assets/6f1cf211-4fdc-4137-b429-1db018db23ce)

## Reflexiones Finales del Modelado

El modelado del Sistema Tunomático permitió identificar cómo los patrones de diseño no solo mejoran la organización del software, sino que también resuelven problemas concretos en contextos reales. El uso de Singleton garantizó un control unificado y seguro sobre los turnos, evitando conflictos en entornos multiusuario. Prototype optimizó la generación de turnos reutilizando configuraciones, mientras que Adapter y Bridge facilitaron la integración con sistemas externos y canales de comunicación variados sin necesidad de modificar el núcleo del sistema. Estas decisiones arquitectónicas demostraron ser claves para lograr un sistema flexible, mantenible y preparado para escalar. El modelado también evidenció oportunidades de mejora, como implementar Observer para notificaciones en tiempo real y Factory Method para adaptadores dinámicos, lo que reafirma que el diseño bien estructurado es un pilar esencial para la evolución tecnológica continua.
