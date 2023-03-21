1.La organización planea migrar su aplicación de supervisión de transacciones financieras a Google Cloud. Los auditores necesitan ver los datos y ejecutar los informes en BigQuery, pero no se les permite realizar transacciones en la aplicación. Usted lidera la migración y busca la solución más sencilla que requiera el menor tiempo posible de mantenimiento. ¿Qué debería hacer?

    R: Crear un grupo de auditores y asignarles roles/bigquery.dataViewer

Feedback: 

    La respuesta A no es correcta porque Google recomienda asignar roles de IAM a grupos, no a usuarios individuales. Los grupos son más fáciles de administrar que los usuarios individuales y proporcionan visibilidad de alto nivel de los roles y permisos.
    La respuesta B no es correcta porque usa un rol básico para otorgar a los auditores acceso de lectura a todos los recursos del proyecto.
    La respuesta C es correcta porque usa un rol predefinido para otorgar acceso de lectura a BigQuery al grupo de auditores. Si cambian las responsabilidades del trabajo, se pueden agregar auditores al grupo o borrarlos.
    La respuesta D no es correcta porque se puede lograr el objetivo mediante un rol predefinido, que requiere menos mantenimiento.

2.Usted administra el primer proyecto de Google Cloud de su empresa. En el proyecto, que incluye información sensible, participarán líderes de proyecto, desarrolladores y verificadores internos. Debe asegurarse de que solo los miembros específicos del equipo de desarrollo tengan acceso a la información sensible. Desea asignar los roles de Identity and Access Management (IAM) adecuados que también requieran el menor tiempo posible de mantenimiento. ¿Qué debería hacer?

    R: Crear grupos. Asignar un rol predefinido de IAM a cada grupo según sea necesario, incluidos aquellos que deberían tener acceso a datos sensibles. Asignar usuarios a los grupos

Feedback: 

    La respuesta A no es correcta por dos motivos: se recomienda usar grupos y no asignar roles a cada usuario. Además, los roles básicos no tienen el nivel de detalle suficiente para justificar el acceso a datos sensibles.
    La respuesta B no es correcta porque los roles básicos no tienen el nivel de detalle suficiente para justificar el acceso a datos sensibles.
    La respuesta C no es correcta porque crear y mantener roles personalizados requerirá más mantenimiento que usar roles predefinidos.
    La respuesta D es correcta porque los roles predefinidos tienen el nivel de detalle suficiente para establecer los permisos de los roles específicos que requieren acceso a datos sensibles. Esta solución también usa grupos, que es lo que se recomienda para administrar permisos de roles individuales.

3.Es responsable de supervisar todos los cambios en las instancias de Cloud Storage y Firestore. Para cada cambio, debe invocar una acción que verificará el cumplimiento del cambio casi en tiempo real. Desea lograrlo con una configuración mínima. ¿Qué debería hacer?

    R: B. Usar los eventos de Cloud Function y llamar a la secuencia de comandos de seguridad de los activadores de Cloud Function

Feedback: 

    La respuesta A no es correcta porque configurar activadores en cada base de datos individual requiere configuración adicional.
    La respuesta B es correcta porque proporciona una respuesta rápida y requiere una configuración mínima.
    La respuesta C no es correcta porque requiere programación personalizada.
    La respuesta D no es correcta porque requiere una cantidad importante de programación personalizada.

4.Su aplicación necesita procesar una importante tasa de transacciones. La tasa de transacciones supera las capacidades de procesamiento de una única máquina virtual (VM). Desea expandir las transacciones en varios servidores en tiempo real y de la forma más rentable. ¿Qué debería hacer?

    R: C. Enviar las transacciones a Pub/Sub. Procesarlas en las VMs en un grupo de instancias administrado

Feedback: 

    La respuesta A no es correcta porque su latencia es significativamente más alta que la respuesta en tiempo real requerida.
    La respuesta B no es correcta porque no proporcionará el rendimiento deseado.
    La respuesta C es correcta porque Pub/Sub es una solución escalable que puede distribuir una gran cantidad de tareas entre varios servidores de forma eficaz y a bajo costo.
    La respuesta D no es correcta porque, aunque es rápido, generará un gasto adicional para almacenar los datos.

5.Su equipo necesita conectar de forma directa los recursos locales a varias máquinas virtuales dentro de una nube privada virtual (VPC). Desea otorgarle a su equipo acceso rápido y seguro a las VMs con mantenimiento y costo mínimos. ¿Qué debería hacer?

    R: B. Usar Cloud VPN para crear una conexión VPN entre la VPC y su red.

Feedback: 

    La respuesta A no es correcta porque es mucho más costosa que otras soluciones existentes.
    La respuesta B es correcta porque concuerda con las prácticas recomendadas de Google.
    La respuesta C no es correcta porque requerirá un gran esfuerzo de mantenimiento.
    La respuesta D no es correcta porque configurar conexiones para cada VM individual requiere mucho mantenimiento.

6.Usted implementará Cloud Storage en su organización. Debe cumplir las reglamentaciones de la organización. Entre las reglamentaciones, se incluye lo siguiente: 1) Archivar los datos de más de un año de antigüedad 2) Borrar los datos de más de 5 años de antigüedad 3) Usar Standard Storage para todos los demás datos Desea implementar estos lineamientos automáticamente y de la forma más sencilla disponible. ¿Qué debería hacer?

    R: A. Configurar políticas de administración del ciclo de vida de los objetos

Feedback: 

    La respuesta A es correcta porque el ciclo de vida de los objetos le permite automatizar la implementación de la política de datos de su organización.
    La respuesta B no es correcta porque no es necesario copiar un objeto a otro bucket para cambiar la clase de almacenamiento del objeto.
    La respuesta C no es correcta porque requiere programación personalizada.
    La respuesta D no es correcta porque migrar un objeto al bucket DELETED no lo borra en realidad.

7.Creará una aplicación de Cloud IoT que requiere almacenamiento de datos de hasta 10 petabytes (PB). La aplicación debe admitir lectura y escritura de alta velocidad para pequeños fragmentos de datos, pero su esquema de datos es sencillo. Desea usar la solución más económica para el almacenamiento de datos. ¿Qué debería hacer?

    R: C. Almacenar los datos en Cloud Bigtable e implementar la lógica empresarial en el lenguaje de programación de su preferencia

Feedback: 

    La respuesta A no es correcta porque Cloud Spanner no sería la solución más económica.
    La respuesta B no es correcta porque Cloud Storage orientado a BLOB no es una opción adecuada para la lectura y escritura de fragmentos de datos pequeños.
    La respuesta C es correcta porque Bigtable proporciona lecturas y escrituras de alta velocidad, admite un esquema sencillo y es rentable.
    La respuesta D no es correcta porque BigQuery no proporciona las lecturas y escrituras de alta velocidad que requiere el IoT.

8.Ha creado una implementación de Kubernetes en Google Kubernetes Engine (GKE) que tiene un servicio de backend. También tiene Pods que ejecutan el servicio de frontend. Debe asegurarse de que no haya interrupciones en las comunicaciones entre los Pods de su servicio de frontend y backend si se migran o reinician. ¿Qué debería hacer?

    R: A. Crear un servicio que agrupe sus Pods en el servicio de backend y, luego, indicarles a los Pods de frontend que se comuniquen a través de ese servicio

Feedback: 

    
    La respuesta A es correcta porque el servicio de Kubernetes tiene la finalidad de proporcionar un destino que se pueda usar cuando los Pods se migren o se reinicien.
    La respuesta B no es correcta porque la creación del servicio crea una entrada de DNS.
    La respuesta C no es correcta porque las direcciones IP internas estáticas no cambian automáticamente cuando se reinician los Pods.
    La respuesta D no es correcta porque las direcciones IP externas estáticas no cambian automáticamente cuando se reinician los Pods, y toman el tráfico fuera de las redes de Google.

9.Usted es el responsable del servicio de administración de usuarios de su empresa global. El servicio agregará, actualizará, borrará y enumerará direcciones. Un microservicio de contenedor de Docker implementa cada una de estas operaciones. La carga de procesamiento puede variar de baja a muy alta. Desea implementar el servicio en Google Cloud para permitir la escalabilidad y una administración mínima. ¿Qué debería hacer?

    R: A. Implementar sus contenedores de Docker en Cloud Run

Feedback: 

    La respuesta A es correcta porque Cloud Run es un servicio administrado que requiere una administración mínima.
    La respuesta B no es correcta porque los grupos de instancias administrados carecen de capacidades administrativas para exponer sus servicios.
    La respuesta C no es correcta porque, aunque GKE proporciona escalabilidad, requiere la administración continua del clúster.
    La respuesta D no es correcta porque requiere esfuerzos para volver a implementar los cuatro microservicios en un contenedor de Docker. También perderá la arquitectura de microservicio.

10.Proporciona un servicio que necesita abrir a toda su red de socios.  Tiene un servidor y una dirección IP en la que se encuentra la aplicación. Desea no tener que cambiar la dirección IP en el servidor DNS si su servidor falla o se reemplaza. También desea evitar el tiempo de inactividad y entregar una solución de costo y configuración mínimos. ¿Qué debería hacer?

    R: C. Reservar una dirección IP externa estática y asignarla mediante Cloud DNS

Feedback: 

    La respuesta A no es correcta porque actualizar los registros DNS podría tardar hasta 24 horas y ocasionaría tiempo de inactividad.
    La respuesta B no es correcta porque las IP internas no se pueden enrutar ni se pueden ver en Internet.
    La respuesta C es correcta porque las IP externas se pueden enrutar y se las puede publicitar y ver en Internet. Además, es la solución más rentable.
    La respuesta D no es correcta porque, si bien es posible, proporcionar su propia dirección IP no es tan rentable como Google Cloud DNS.

11.Su equipo creará los entornos de desarrollo, prueba y producción de su implementación de proyecto en Google Cloud. Debe implementar y administrar estos entornos de forma eficiente y asegurarse de que sean coherentes. Quiere seguir las recomendaciones de Google. ¿Qué debería hacer?

    R: D. Usar Cloud Foundation Toolkit a fin de crear una plantilla de implementación que sea útil para todos los entornos e implementar con Terraform

Feedback: 

    La respuesta A no es correcta porque crear una secuencia de comandos de gcloud personalizada que cumpla con las prácticas recomendadas de Google Cloud requiere importantes esfuerzos de desarrollo y mantenimiento.
    La respuesta B no es correcta porque parametrizar las diferencias de los entornos demanda mucho tiempo y es propensa a errores.
    La respuesta C no es correcta porque es propensa a errores y, además, involucra un trabajo de conciliación importante.
    La respuesta D es correcta porque Cloud Foundation Toolkit (CFT) proporciona plantillas listas para usar que reflejan las prácticas recomendadas de Google Cloud y se pueden usar a fin de automatizar la creación de los entornos.

12.Recibió un mensaje de error cuando intentó iniciar una VM nueva: “Ha agotado el rango de IP en su subred”. Desea resolver el error con el mínimo esfuerzo.  ¿Qué debería hacer?

    R: B. Expandir el rango de CIDR en su subred y reiniciar la VM que emitió el error

Feedback: 

    La respuesta A no es correcta porque no necesita una subred nueva. Una vez que expanda el rango de CIDR, la VM inicial funcionará si vuelve a realizar la implementación.
    La respuesta B es correcta porque, una vez que expanda el rango de CIDR, podrá volver a implementarla y funcionará.
    La respuesta C no es correcta porque migrar sus VMs a otra subred implica un esfuerzo adicional innecesario que demanda tiempo.
    La respuesta D no es correcta porque, una vez que el rango de CIDR se agota, volver a implementar la VM con errores no solucionará el problema.

13.Ejecuta varias aplicaciones relacionadas en instancias de máquina virtual (VM) de Compute Engine. Desea seguir las prácticas recomendadas de Google y exponer cada aplicación a través de un nombre de DNS. ¿Qué debería hacer?

    R: D. Usar Cloud DNS para traducir sus nombres de dominio en las direcciones IP

Feedback: 

    La respuesta A no es correcta porque el correo electrónico no es la forma de enviar solicitudes de publicación de DNS.
    La respuesta B no es correcta porque no puede hacer público el nombre de DNS interno.
    La respuesta C no es correcta porque no puede hacer públicos los nombres de DNS.
    La respuesta D es correcta porque Cloud DNS es la herramienta adecuada para traducir los nombres de dominio en direcciones IP.

14.Usted está a cargo de la optimización del consumo de recursos de Google Cloud. En particular, debe investigar los cargos del consumo de recursos y presentar un resumen con los resultados. Desea hacerlo de la forma más eficaz posible. ¿Qué debería hacer?

    R: B. Adjuntar etiquetas de recursos para reflejar el propietario y el propósito de los recursos. Exportar datos de Facturación de Cloud a BigQuery y analizarlos con Data Studio

Feedback: 

    La respuesta A no es correcta porque necesita programación personalizada, no sigue las prácticas recomendadas de Google y no es la solución más eficaz.
    La respuesta B es correcta porque describe las prácticas recomendadas de Google: las etiquetas de recursos se adjuntan a los recursos y se propagan en los elementos de facturación.
    La respuesta C no es correcta porque ya no se crean etiquetas de políticas cuando se crea una etiqueta de recurso para un recurso, y no se pueden usar a fin de realizar un seguimiento de los recursos.
    La respuesta D no es correcta porque necesita programación personalizada.

15.Creará un entorno para que los investigadores ejecuten consultas en SQL ad hoc. Los investigadores trabajan con grandes cantidades de datos.  A pesar de que usarán el entorno durante una hora al día en promedio, los investigadores necesitan acceso al entorno funcional en cualquier momento del día. Necesita entregar una solución rentable. ¿Qué debería hacer?

    R: B. Almacenar los datos en BigQuery y ejecutar consultas en SQL en BigQuery

Feedback: 

    La respuesta A no es correcta porque HBase no permite consultas ad hoc.
    La respuesta B es correcta porque BigQuery permite consultas ad hoc y es rentable.
    La respuesta C no es correcta porque HDFS no es el sistema de almacenamiento recomendado para usar con Dataproc en Google Cloud.
    La respuesta D no es correcta porque no es la solución más rentable, ya que el clúster se encuentra en ejecución en todo momento.

16.Migrará su carga de trabajo de la implementación local a Google Kubernetes Engine (GKE). Desea minimizar los costos y mantenerse dentro del presupuesto. ¿Qué debería hacer?

    R: A. Configurar Autopilot en GKE para supervisar la utilización de nodos y eliminar nodos inactivos

Feedback: 

    La respuesta A es correcta porque Autopilot está diseñado con el fin de reducir el costo operativo de la administración de clústeres y optimizar sus clústeres para la producción.
    La respuesta B no es correcta porque viola el principio de aprovisionamiento según demanda en lugar del aprovisionamiento excesivo. A pesar de que el descuento por uso continuo reduce el presupuesto, no usar recursos innecesarios reducirá aún más los costos.
    La respuesta C no es correcta porque Horizontal Pod Autoscaler se usa a fin de ajustar los parámetros de Kubernetes para el rendimiento, no para quitar recursos innecesarios.
    La respuesta D no es correcta porque, a pesar de que Google Kubernetes Engine usa Compute Engine de forma interna, los grupos de instancias administrados carecen de capacidades de Autopilot para el escalamiento de Kubernetes.

17.Su aplicación permite que los usuarios suban fotos. Debe convertir cada foto en su formato binario interno optimizado y almacenarlas. Desea usar la solución más eficaz y rentable. ¿Qué debería hacer?

    R: D. Guardar los archivos cargados en un bucket de Cloud Storage y supervisar el bucket para las cargas. Ejecutar una Cloud Function para convertir los archivos y almacenarlos en un bucket de Cloud Storage

Feedback: 

    La respuesta A no es correcta porque Bigtable tiene limitaciones en el almacenamiento de archivos binarios.
    La respuesta B no es correcta porque Firestore no es eficaz para archivos binarios grandes.
    La respuesta C no es correcta porque no es la solución más rentable.
    La respuesta D es correcta porque sigue las prácticas recomendadas de Google y es la solución más eficaz y rentable.

18.Migrará su solución local a Google Cloud. Como primer paso, la nueva solución en la nube necesitará transferir 100 TB de datos. Sus cargas diarias estarán dentro de su límite de ancho de banda actual de 100 Mbps. Desea seguir las prácticas recomendadas de Google para usar la forma más rentable de implementar la migración. ¿Qué debería hacer?
    
    R: B. Obtener un dispositivo de Transfer Appliance, copiar los datos en él y enviarlo a Google

Feedback: 

    La respuesta A no es correcta porque la interconexión de socio, a pesar de ser menos costosa que la interconexión dedicada, no es la solución más rentable para esta migración.
    La respuesta B es correcta porque sigue las prácticas recomendadas de Google para los datos de estos tamaños y es la solución más rentable si desea implementar la migración.
    La respuesta C no es correcta porque la interconexión dedicada no es la más rentable para este caso de uso.
    La respuesta D no es correcta porque no es la solución más rentable.

19.Debe configurar la facturación de un proyecto. Desea evitar el consumo excesivo de recursos debido a un error o un ataque malicioso y evitar sorpresas o aumentos repentinos en la facturación. ¿Qué debería hacer?

    R: La respuesta B es correcta porque la configuración de cuotas evitará que el consumo de recursos supere los límites especificados.

Feedback: 

    La respuesta A no es correcta porque los presupuestos y las alertas generarán notificaciones, pero no evitarán el consumo excesivo de recursos.
    La respuesta B es correcta porque la configuración de cuotas evitará que el consumo de recursos supere los límites especificados.
    La respuesta C no es correcta porque no evitará el consumo excesivo de recursos. En su lugar, su tarjeta de crédito generará un saldo pendiente de pago. Recibirá un correo electrónico de Google al respecto y será responsable de pagar.
    La respuesta D no es correcta porque analizar la causa raíz de superar el presupuesto no evitará el exceso de gastos.

20.Su equipo de proyecto debe estimar los gastos del proyecto de Google Cloud para el próximo trimestre. Usted conoce los requisitos del proyecto. Desea generar la estimación lo antes posible. ¿Qué debería hacer?

    R: C. Usar la calculadora de precios de Google Cloud para ingresar el consumo previsto de todos los grupos de recursos

Feedback:

    La respuesta A no es correcta porque, a pesar de que el AA produce excelentes resultados en muchas áreas, hay enfoques más sencillos que requieren menos tiempo para producir una estimación.
    La respuesta B no es correcta porque necesita agregar otros cargos, como cargos de almacenamiento y de salida de datos.
    La respuesta C es correcta porque la calculadora de precios de Google Cloud proporciona los resultados con rapidez y usted conoce los recursos que se requieren para el proyecto.
    La respuesta D no es correcta porque los descuentos por volumen, también llamados descuentos por uso continuo, se aplican automáticamente y se incluyen en la estimación de la calculadora.