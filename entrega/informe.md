# 📄 Informe Técnico del Taller

## 🔖 Nombre del Taller
_Taller 4 - Mapa de Infraestructura y Diagnóstico Técnico_

## 👥 Integrantes del equipo
- Jonatan David Vergara Suárez (github.com/JonatnV)
- Carlos David Bello Ortiz
- Jhojan Camilo Jiménez Amaya

## 🧠 Descripción general del trabajo
Construir el mapa lógico y/o físico de la infraestructura tecnológica del sistema base y realizar un diagnóstico de debilidades, cuellos de botella y oportunidades de mejora.

## 🔧 Proceso de desarrollo
Primero se identificó la infraestructura actual que tiene la empresa, despues de eso se evaluó esta misma y se definieron puntos de debilidad y cuellos de botella dentro de el mismo.

Despues, realizamos la investigación complementaria, asegurandonos de tener información de fuentes confiables y poder redactar un buen resumen del tema investigado

Finalmente, consolidamos todo en un solo archivo tipo markdown para su posterior entrega.

## 🧩 Análisis del mapa
La infraestructura es muy básica y se apoya en un único servidor local, en un ERP en la nube (Zoho) y en Google Drive, sin integración entre estos componentes. Esto crea un claro punto único de fallo en el servidor y una dependencia fuerte de la conexión a internet para acceder al ERP, lo que puede afectar de forma directa la operación si hay problemas de hardware o de conectividad. Además, la escalabilidad está limitada: el crecimiento de usuarios o datos fuerza a “vitaminar” un solo servidor en lugar de distribuir la carga de forma más robusta.

Por otro lado, la información está fragmentada entre la base de datos del ERP y los archivos almacenados en Google Drive. Al no haber comunicación automática entre ambos, se generan silos de datos que dificultan tener una visión única y confiable del negocio. Esto aumenta el riesgo de duplicidades e inconsistencias, porque los usuarios pueden exportar información del ERP, trabajarla en Drive y terminar usando versiones distintas de la misma información para reportes y toma de decisiones.

Finalmente, la ausencia de integración provoca procesos manuales intensivos: descargar, subir, copiar y pegar datos entre sistemas. Estos flujos manuales son lentos, propensos a error y poco escalables conforme crece el volumen de operaciones. Sumado a la probable falta de mecanismos formales de alta disponibilidad, copias de seguridad centralizadas y control unificado de permisos, la infraestructura actual presenta debilidades importantes tanto en continuidad de negocio como en seguridad y gobernanza de la información.

## 📈 Mapa de Infraestructura
> (Inserte aquí una imagen o enlace al modelo-final.drawio / .asta / PDF)


## 🔍 Investigación complementaria
### Tema investigado:
Buenas prácticas de arquitectura de infraestructura (cloud, on-premise, híbrida).

### Resumen:
Las mejores prácticas en arquitectura de infraestructura cloud, on-premise e híbrida se centran en principios probados que priorizan la escalabilidad, resiliencia y eficiencia operativa. Tras evaluar fuentes académicas como frameworks de AWS y NIST, así como estudios sobre patrones cloud-native, se identifican enfoques clave adaptables a entornos laborales.

#### Cloud
En arquitecturas cloud puras, como las basadas en AWS Well-Architected Framework, se enfatiza el escalado automático horizontal mediante microservicios y contenedores para manejar cargas variables sin sobreprovisionamiento, reduciendo costos hasta en un 38% según análisis empíricos. La tolerancia a fallos se logra con redundancia multi-zona y failover automatizado, asegurando disponibilidad del 99.99%, mientras que la optimización de costos integra monitoreo continuo y serverless para pagar solo por uso real.

#### On-Premise
Para infraestructuras on-premise, las prácticas destacan el control total con hardware dedicado y virtualización para workloads estables, incorporando aceleradores como GPUs para tareas intensivas y automatización en parches para minimizar downtime manual en un 71%. Se prioriza la seguridad con encriptación local y monitoreo dedicado, aunque limitada en elasticidad comparada con cloud, enfocándose en eficiencia energética y cumplimiento normativo sin dependencias externas.

#### Híbrida
Las arquitecturas híbridas combinan lo mejor de ambos mundos: on-premise para datos sensibles y workloads predecibles, con cloud para picos de demanda vía bursting, optimizando costos y resiliencia mediante conectividad segura como VPNs y zero-trust. Incluyen distribución dinámica de cargas, monitoreo unificado y gobernanza para mitigar complejidad operativa, logrando flexibilidad con reducciones de costos del 38-52% en estudios.

#### Conclusiones
De estas prácticas se aprende que la resiliencia (redundancia, failover) y escalabilidad (microservicios, auto-scaling) son universales, pero híbridas ofrecen mayor adaptabilidad para empresas en transición, implementando marcos como Well-Architected para revisiones regulares que mejoran eficiencia en 56-71%. En el área laboral, prioriza evaluaciones iniciales de workloads, adopta IaC para automatización y monitoreo FinOps para costos, comenzando con pilots híbridos para minimizar riesgos y escalar basado en métricas reales.


## 📚 Referencias
- [1] Panchalingala, Ajay Kumar. AWS Cloud Architecture: A Comprehensive Analysis of Best Practices and Design Principles. 2025. https://eajournals.org/ejcsit/wp-content/uploads/sites/21/2025/06/AWS-Cloud-Architecture.pdf.
- [2] Gundla, Naresh Kumar. Building Castles in the Cloud: Architecting Resilient and Scalable Infrastructure. 2024. https://arxiv.org/pdf/2410.21740.pdf.
- [3] Fuente oficial AWS: https://aws.amazon.com/architecture/well-architected/.

---

_Este documento hace parte de la entrega del taller X del curso AREM (Arquitectura Empresarial) - Universidad de La Sabana._