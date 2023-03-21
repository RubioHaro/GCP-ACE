# Cloud Engineer Preguntas de ejemplo: Google Cloud

Las siguientes preguntas de ejemplo le ayudarán a familiarizarse con el formato de las preguntas del examen y con el contenido que pudiera cubrir el examen.


<style type="text/css">
    ol { list-style-type: upper-alpha; }
</style>

## Preguntas: 

1.La organización planea migrar su aplicación de supervisión de transacciones financieras a Google Cloud. Los auditores necesitan ver los datos y ejecutar los informes en BigQuery, pero no se les permite realizar transacciones en la aplicación. Usted lidera la migración y busca la solución más sencilla que requiera el menor tiempo posible de mantenimiento. ¿Qué debería hacer?


<ol type="a">
  <li>
    Asignar roles/bigquery.dataViewer a los auditores individuales
  </li>
  <li>
    Crear un grupo de auditores y asignarles roles/visualizador
  </li>
  <li>
    Crear un grupo de auditores y asignarles roles/bigquery.dataViewer
  </li> 
  <li>
    Asignar un rol personalizado a cada auditor que permita acceso de solo lectura a BigQuery
  </li> 
</ol>

2.Usted administra el primer proyecto de Google Cloud de su empresa. En el proyecto, que incluye información sensible, participarán líderes de proyecto, desarrolladores y verificadores internos. Debe asegurarse de que solo los miembros específicos del equipo de desarrollo tengan acceso a la información sensible. Desea asignar los roles de Identity and Access Management (IAM) adecuados que también requieran el menor tiempo posible de mantenimiento. ¿Qué debería hacer?

<ol type="a">
  <li>
  Asignar un rol básico a cada usuario
  </li>
  <li>
  Crear grupos. Asignar un rol básico a cada grupo y, luego, asignar usuarios a los grupos
  </li>
  <li>
  Crear grupos. Asignar un rol personalizado a cada grupo, incluidos aquellos que deberían tener acceso a datos sensibles. Asignar usuarios a los grupos
  </li> 
  <li>
  Crear grupos. Asignar un rol predefinido de IAM a cada grupo según sea necesario, incluidos aquellos que deberían tener acceso a datos sensibles. Asignar usuarios a los grupos
  </li> 
</ol>

3.Es responsable de supervisar todos los cambios en las instancias de Cloud Storage y Firestore. Para cada cambio, debe invocar una acción que verificará el cumplimiento del cambio casi en tiempo real. Desea lograrlo con una configuración mínima. ¿Qué debería hacer?

<ol type="a">
  <li>
  Usar el mecanismo del activador en cada almacén de datos para invocar la secuencia de comandos de seguridads
  </li>
  <li>
  Usar los eventos de Cloud Function y llamar a la secuencia de comandos de seguridad de los activadores de Cloud Function

  </li>
  <li>
  Usar una secuencia de comandos de Python para obtener registros de los almacenes de datos, analizarlos y, luego, invocar la secuencia de comandos de seguridad

  </li> 
  <li>
  Redireccionar las consultas de cambio de datos a una aplicación de App Engine y llamar a la secuencia de comandos de seguridad desde la aplicación
  </li> 
</ol>

4.Su aplicación necesita procesar una importante tasa de transacciones. La tasa de transacciones supera las capacidades de procesamiento de una única máquina virtual (VM). Desea expandir las transacciones en varios servidores en tiempo real y de la forma más rentable. ¿Qué debería hacer?

<ol type="a">
  <li>
 Enviar las transacciones a BigQuery. En las VMs, sondear en busca de transacciones que no tienen la clave “procesada” y marcarlas como “procesadas” cuando termine

  </li>
  <li>
  Configurar Cloud SQL con una memoria caché para obtener velocidad. En sus múltiples servidores, sondear en busca de transacciones que no tengan la clave “procesada” y marcarlas como “procesadas” cuando termine

  </li>
  <li>
  Enviar las transacciones a Pub/Sub. Procesarlas en las VMs en un grupo de instancias administrado
  </li> 
  <li>

  Registrar las transacciones en Cloud Bigtable y sondear en busca de transacciones nuevas desde las VMs

  </li> 
</ol>

5.Su equipo necesita conectar de forma directa los recursos locales a varias máquinas virtuales dentro de una nube privada virtual (VPC). Desea otorgarle a su equipo acceso rápido y seguro a las VMs con mantenimiento y costo mínimos. ¿Qué debería hacer?

<ol type="a">
  <li>
  Configurar Cloud Interconnect
  </li>
  <li>
  Usar Cloud VPN para crear un puente entre la VPC y su red
  </li>
  <li>
  Asignar una dirección IP pública y una contraseña segura a cada VM
  </li> 
  <li>
  Iniciar una VM de Compute Engine, instalar un router de software y crear un túnel directo a cada VM
  </li> 
</ol>

6.Usted implementará Cloud Storage en su organización. Debe cumplir las reglamentaciones de la organización. Entre las reglamentaciones, se incluye lo siguiente: 1) Archivar los datos de más de un año de antigüedad 2) Borrar los datos de más de 5 años de antigüedad 3) Usar Standard Storage para todos los demás datos Desea implementar estos lineamientos automáticamente y de la forma más sencilla disponible. ¿Qué debería hacer?

<ol type="a">
  <li>
  Configurar políticas de administración del ciclo de vida de los objetos
  </li>
  <li>
  Ejecutar una secuencia de comandos a diario. Copiar los datos que tengan más de un año de antigüedad a un bucket de archivo y borrar los datos de más de cinco años de antigüedad  
</li>
  <li>
  Ejecutar una secuencia de comandos a diario. Establecer la clase de almacenamiento en ARCHIVE para los datos que tengan más de un año de antigüedad y borrar los datos de cinco años de antigüedad  
</li> 
  <li>
  Configurar una clase de almacenamiento predeterminada para tres buckets con los nombres: STANDARD, ARCHIVE, DELETED. Usar una secuencia de comandos para migrar los datos al bucket adecuado cuando su condición coincida con los lineamientos de su empresa
  </li> 
</ol>

7.Creará una aplicación de Cloud IoT que requiere almacenamiento de datos de hasta 10 petabytes (PB). La aplicación debe admitir lectura y escritura de alta velocidad para pequeños fragmentos de datos, pero su esquema de datos es sencillo. Desea usar la solución más económica para el almacenamiento de datos. ¿Qué debería hacer?

<ol type="a">
  <li>
  Almacenar los datos en Cloud Spanner, y agregar una caché en memoria para obtener velocidad

  </li>
  <li>
  Almacenar los datos en Cloud Storage y distribuirlos a través de Cloud CDN para obtener velocidad

</li>
  <li>
  Almacenar los datos en Cloud Bigtable e implementar la lógica empresarial en el lenguaje de programación de su preferencia

</li> 
  <li>
  Usar BigQuery e implementar la lógica empresarial en SQL
  </li> 
</ol>

8.Ha creado una implementación de Kubernetes en Google Kubernetes Engine (GKE) que tiene un servicio de backend. También tiene Pods que ejecutan el servicio de frontend. Debe asegurarse de que no haya interrupciones en las comunicaciones entre los Pods de su servicio de frontend y backend si se migran o reinician. ¿Qué debería hacer?

Extra: A Pod (as in a pod of whales or pea pod) is a group of one or more containers, with shared storage and network resources, and a specification for how to run the containers. A Pod's contents are always co-located and co-scheduled, and run in a shared context. A Pod models an application-specific "logical host": it contains one or more application containers which are relatively tightly coupled. In non-cloud contexts, applications executed on the same physical or virtual machine are analogous to cloud applications executed on the same logical host.

source: https://kubernetes.io/docs/concepts/workloads/pods
<ol type="a">
  <li>
  Crear un servicio que agrupe sus Pods en el servicio de backend y, luego, indicarles a los Pods de frontend que se comuniquen a través de ese servicio

  </li>
  <li>
  Crear una entrada de DNS con una dirección IP fija que el servicio de frontend pueda usar para llegar al servicio de backend

</li>
  <li>
  Asignar direcciones IP internas estáticas que el servicio de frontend pueda usar para llegar a los Pods de backend

</li> 
  <li>
  Asignar direcciones IP externas estáticas que el servicio de frontend pueda usar para llegar a los Pods de backend
  </li> 
</ol>

9.Usted es el responsable del servicio de administración de usuarios de su empresa global. El servicio agregará, actualizará, borrará y enumerará direcciones. Un microservicio de contenedor de Docker implementa cada una de estas operaciones. La carga de procesamiento puede variar de baja a muy alta. Desea implementar el servicio en Google Cloud para permitir la escalabilidad y una administración mínima. ¿Qué debería hacer?


<ol type="a">
  <li>
  Implementar sus contenedores de Docker en Cloud Run
  </li>
  <li>
Iniciar cada contenedor de Docker como un grupo de instancias administrado
</li>
  <li>
Implementar sus contenedores de Docker en Google Kubernetes Engine
</li> 
  <li>
Combinar los cuatro microservicios en una imagen de Docker y, luego, implementarla en la instancia de App Engine  </li> 
</ol>

10.Proporciona un servicio que necesita abrir a toda su red de socios.  Tiene un servidor y una dirección IP en la que se encuentra la aplicación. Desea no tener que cambiar la dirección IP en el servidor DNS si su servidor falla o se reemplaza. También desea evitar el tiempo de inactividad y entregar una solución de costo y configuración mínimos. ¿Qué debería hacer?

<ol type="a">
  <li>
  Crear una secuencia de comandos que actualice la dirección IP del dominio cuando el servidor falle o se reemplace

  </li>
  <li>
  Reservar una dirección IP interna estática y asignarla mediante Cloud DNS

</li>
  <li>
  Reservar una dirección IP externa estática y asignarla mediante Cloud DNS

</li> 
  <li>
  Emplear el método Use su propia IP (BYOIP) para usar su propia dirección IP
  </li> 
</ol>

11.Su equipo creará los entornos de desarrollo, prueba y producción de su implementación de proyecto en Google Cloud. Debe implementar y administrar estos entornos de forma eficiente y asegurarse de que sean coherentes. Quiere seguir las recomendaciones de Google. ¿Qué debería hacer?

<ol type="a">
  <li>
  Crear una secuencia de comandos de Cloud Shell que use comandos de gcloud para implementar los entornos
  </li>
  <li>
  Crear una configuración de Terraform para todos los entornos. Parametrizar las diferencias entre los entornos

</li>
  <li>
  Crear una configuración de Terraform para cada entorno. Usarlas para realizar implementaciones repetidas. Conciliar las plantillas de forma periódica

</li> 
  <li>
  Usar Cloud Foundation Toolkit a fin de crear una plantilla de implementación que sea útil para todos los entornos e implementar con Terraform 
  </li> 
</ol>

12.Recibió un mensaje de error cuando intentó iniciar una VM nueva: “Ha agotado el rango de IP en su subred”. Desea resolver el error con el mínimo esfuerzo.  ¿Qué debería hacer?

<ol type="a">
  <li>
  Crear una subred nueva y, luego, iniciar su VM en ella
  </li>
  <li>
  Expandir el rango de CIDR en su subred y reiniciar la VM que emitió el error

</li>
  <li>
  Crear otra subred y migrar varias VMs existentes a la subred nueva

</li> 
  <li>
  Reiniciar la VM mediante la retirada exponencial hasta que se inicie de forma correcta
  </li> 
</ol>

13.Ejecuta varias aplicaciones relacionadas en instancias de máquina virtual (VM) de Compute Engine. Desea seguir las prácticas recomendadas de Google y exponer cada aplicación a través de un nombre de DNS. ¿Qué debería hacer?

<ol type="a">
  <li>
  Usar el servicio de DNS interno de Compute Engine para asignar nombres de DNS a sus instancias de VM y dar a conocer los nombres a sus usuarios

  </li>
  <li>
  Asignar a cada instancia de VM un rango de alias de direcciones IP y, a continuación, hacer públicos los nombres de DNS internos

</li>
  <li>
  Asignar rutas de Google Cloud a sus instancias de VM, asignar nombres de DNS a las rutas y hacer públicos los nombres de DNS

</li> 
  <li>
  Usar Cloud DNS para traducir sus nombres de dominio en las direcciones IP
  </li> 
</ol>

14.Usted está a cargo de la optimización del consumo de recursos de Google Cloud. En particular, debe investigar los cargos del consumo de recursos y presentar un resumen con los resultados. Desea hacerlo de la forma más eficaz posible. ¿Qué debería hacer?

<ol type="a">
  <li>
  Cambiar el nombre de los recursos para reflejar el propietario y el propósito. Escribir una secuencia de comandos de Python para analizar el consumo de recursos

  </li>
  <li>
  Adjuntar etiquetas de recursos para reflejar el propietario y el propósito de los recursos. Exportar datos de Facturación de Cloud a BigQuery y analizarlos con Data Studio

</li>
  <li>
  Asignar etiquetas de políticas a los recursos para reflejar el propietario y el propósito. Exportar datos de Facturación de Cloud a BigQuery y analizarlos con Data Studio

</li> 
  <li>
  Crear una secuencia de comandos para analizar el uso de los recursos en función del proyecto al que pertenecen los recursos. En esa secuencia de comandos, usar las cuentas de servicio y las cuentas de IAM que controlan dichos recursos
  </li> 
</ol>


15.Creará un entorno para que los investigadores ejecuten consultas en SQL ad hoc. Los investigadores trabajan con grandes cantidades de datos.  A pesar de que usarán el entorno durante una hora al día en promedio, los investigadores necesitan acceso al entorno funcional en cualquier momento del día. Necesita entregar una solución rentable. ¿Qué debería hacer?

<ol type="a">
  <li>
  Almacenar los datos en Cloud Bigtable y ejecutar consultas en SQL que proporciona el esquema de Bigtable

  </li>
  <li>
  Almacenar los datos en BigQuery y ejecutar consultas en SQL en BigQuery

</li>
  <li>
  Crear un clúster de Dataproc, almacenar los datos en un sistema de almacenamiento HDFS y ejecutar las consultas en SQL en Spark

</li> 
  <li>
  Crear un clúster de Dataproc, almacenar los datos en Cloud Storage y ejecutar consultas en SQL en Spark
  </li> 
</ol>

16.Migrará su carga de trabajo de la implementación local a Google Kubernetes Engine (GKE). Desea minimizar los costos y mantenerse dentro del presupuesto. ¿Qué debería hacer?

<ol type="a">
  <li>
  Configurar Autopilot en GKE para supervisar la utilización de nodos y eliminar nodos inactivos

  </li>
  <li>
  Configurar la capacidad necesaria; el descuento por uso continuo lo mantendrá dentro del presupuesto

</li>
  <li>
  Aumentar y reducir la escala vertical de los nodos individuales con Horizontal Pod Autoscaler

</li> 
  <li>
  Crear varios nodos mediante Compute Engine, agregarlos a un grupo de instancias administrado y configurar el grupo para aumentar y reducir la escala vertical según la carga
  </li> 
</ol>

17.Su aplicación permite que los usuarios suban fotos. Debe convertir cada foto en su formato binario interno optimizado y almacenarlas. Desea usar la solución más eficaz y rentable. ¿Qué debería hacer?

<ol type="a">
  <li>
  Almacenar los archivos cargados en Cloud Bigtable, supervisar las entradas de Bigtable y, luego, ejecutar una Cloud Function para convertir los archivos y almacenarlos en Bigtable


  </li>
  <li>
  Almacenar los archivos cargados en Firestore, supervisar las entradas de Firestore y, a continuación, ejecutar una Cloud Function para convertir los archivos y almacenarlos en Firestore


</li>
  <li>
  Almacenar los archivos cargados en Filestore, supervisar las entradas de Filestore y, a continuación, ejecutar una Cloud Function para convertir los archivos y almacenarlos en Filestore


</li> 
  <li>
  Guardar los archivos cargados en un bucket de Cloud Storage y supervisar el bucket para las cargas. Ejecutar una Cloud Function para convertir los archivos y almacenarlos en un bucket de Cloud Storage
  </li> 
</ol>

18.Migrará su solución local a Google Cloud. Como primer paso, la nueva solución en la nube necesitará transferir 100 TB de datos. Sus cargas diarias estarán dentro de su límite de ancho de banda actual de 100 Mbps. Desea seguir las prácticas recomendadas de Google para usar la forma más rentable de implementar la migración. ¿Qué debería hacer?


<ol type="a">
  <li>
  Configurar la interconexión de socio para la duración de la primera carga
  </li>
  <li>
  Obtener un dispositivo de Transfer Appliance, copiar los datos en él y enviarlo a Google
</li>
  <li>
  Configurar la interconexión dedicada para la duración de la primera carga y, luego, volver al ancho de banda normal
</li> 
  <li>
  Dividir los datos entre 100 computadoras y subir cada porción de datos a un bucket. A continuación, ejecutar una secuencia de comandos para combinar las cargas
  </li> 
</ol>

19.Debe configurar la facturación de un proyecto. Desea evitar el consumo excesivo de recursos debido a un error o un ataque malicioso y evitar sorpresas o aumentos repentinos en la facturación. ¿Qué debería hacer?

<ol type="a">
  <li>
  Configurar presupuestos y alertas en su proyecto

  </li>
  <li>
  Configurar cuotas para los recursos que se usarán en el proyecto

</li>
  <li>
  Configurar un límite de gasto en la tarjeta de crédito que se usa en la cuenta de facturación

</li> 
  <li>
  Etiquetar todos los recursos de acuerdo con las prácticas recomendadas, exportar de forma periódica los informes de facturación y analizarlos con BigQuery
  </li> 
</ol>

20.Su equipo de proyecto debe estimar los gastos del proyecto de Google Cloud para el próximo trimestre. Usted conoce los requisitos del proyecto. Desea generar la estimación lo antes posible. ¿Qué debería hacer?

<ol type="a">
  <li>
    Crear un modelo de aprendizaje automático sencillo que prediga sus gastos del próximo mes

  </li>
  <li>
    Estimar la cantidad necesaria de horas de tiempo de procesamiento y, luego, multiplicarla por el precio por hora de la VM

</li>
  <li>
    Usar la calculadora de precios de Google Cloud para ingresar el consumo previsto de todos los grupos de recursos

</li> 
  <li>
    Usar la calculadora de precios de Google Cloud para ingresar el consumo de todos los grupos de recursos y, luego, ajustar a fin de obtener descuentos por volumen
  </li> 
</ol>

