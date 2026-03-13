# 🗒️ Registro de Trabajo en Clase - Taller X

## 📆 Fecha de la sesión
_Indique la fecha de la clase en que se trabajó este taller._

## 👥 Integrantes presentes
- Carlos David Bello Ortiz
- Jonatan David Vergara Suarez
- Jhojan camilo Jiménez Amaya

## 🧠 Actividades realizadas en clase

Se discutio primero que partes de la infraestructura, tendrian sentido que correspondan a encontrarse On-premise y cuales serian las que estarian en la nube,
primero se definio que el Api Gateway se encontraria en la nube ya que seria el modo en que los servicios en la nube podrian ser accedidos, igualmente se definio
que los servicios usado para el rastreo de los envios, el servicio de envios y notificaciones de estado de paquete, estarian en la nube usando EC2 el cual es
tipo IaaS y lambda el cual es PaaS/Serverless, luego usaria la seria de servicios, de CloudTrail,CloudWatch, SNS y SQS para el monitoreo y las alartas y en la nube
se usaria una base de datos Aurora por su escalabilidad, luego se usaria AWS Direct Connect, para que se pueda comunicar y conectar la infraestructora On-premise
con la infraestructura en Cloud, On-premise, empezaria con el firewall, el cual luego esta conectado con el VPN y desde aqui pasaria, al router, al switch para 
conectarse ahi a los servidores ( por ahora uno de cada uno ) de procesamiento de rutas y el servidor de procesamiento de paquetes los cuales tendrian un base de 
datos local que cuente con Redis para usar el cache para permitir una mayor velocidad del servicio, inicialmente se habria considerado un Load Balancer pero era 
redundante debido a que solo habia dos servidores con funciones diferentes.

## 🧩 Boceto inicial del modelo



## Analisis de la Infraestructura
Primeramente, se identifica la falta de redundancia en los servidores On-premise, por lo que uno de ellos fallando podria llevar a la perdida de servicio hasta
que se logre solucionar el problema o reemplazar. por lo que una solución seria contar con varios servidores de cada tipo y hacer uso de un balanceador de carga
para cada servidor permitiendo asegurar la disponibilidad , AWS Direct connect como unica conexion puede resultar peligroso si llega a perderse la conexión por lo 
que un AWS Site-to-Site VPN como respaldo ayudaria a continuar las operaciones en caso de fallo en la conexión, luego se evidencia la falta de monitoreo On-premise
por lo cual haria falta el uso de agentes locales para realizar el monitoreo

---

_Este documento resume el trabajo colaborativo realizado durante la sesión del taller X en el curso AREM - Universidad de La Sabana._na.
