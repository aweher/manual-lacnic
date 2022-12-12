# 2. DIRECCIONES IPv4 

## 2.1. ALCANCE 

Este capítulo describe el sistema de administración de recursos de Internet en el área de Latinoamérica y el Caribe. Particularmente describe las reglas y guías que gobiernan la distribución de los bloques de direcciones IPv4 asignados a Latinoamérica y el Caribe. En el caso de direcciones IP las reglas establecidas en este capítulo están relacionadas para todos los bloques de direcciones IPv4 distribuidas o asignadas vía LACNIC y las anteriores distribuidas y asignadas por ARIN. 
Este capítulo no describe espacio de direcciones de Internet privadas y espacios de direcciones multicast. 

Este capítulo tampoco describe la administración del espacio del direccionamiento IPv6 el cual es tratado en el capítulo de "Políticas para la distribución y asignación de direcciones IPv6". Se hace aquí una distinción entre distribución y asignación de direcciones IP. Las direcciones son distribuidas a los NIRs e ISPs para que a su vez sean asignadas a sus usuarios finales. 

## 2.2. ESPACIO DE DIRECCIONES IPv4 Y EL SISTEMA DE REGISTRO DE INTERNET 

### 2.2.1. Tipo de direcciones IPv4 

Para propósitos de este capítulo las direcciones IPv4 son números binarios de 32 bits que son usados como direcciones en los protocolos IPv4, el cual es utilizado en Internet. Existen tres tipos de direcciones IPv4. 

#### 2.2.1.1. Direcciones IPv4 públicas 

Las direcciones IPv4 públicas constituyen el espacio de direcciones de Internet. Estas son distribuidas para ser globalmente únicas de acuerdo a los objetivos que se describirán más adelante en este documento. El principal propósito de este espacio de direcciones es permitir la comunicación usando IPv4 sobre Internet. Un propósito secundario es permitir la comunicación entre redes privadas interconectadas. 

##### 2.2.1.2. Direcciones IPv4 privadas 

Algunos rangos de direcciones IPv4 han sido reservados para la operación de redes privadas. Cualquier organización puede usar estas direcciones IPv4 en sus redes privadas sin la necesidad de solicitarlo a algún Registro de Internet. La principal condición establecida para el uso de direcciones IPv4 privadas es que los dispositivos que usen estas direcciones IPv4 no necesiten ser alcanzados desde Internet. Para una descripción más detallada acerca del espacio de direcciones IPv4 privadas, por favor consulte el RFC 1918. 

##### 2.2.1.3. Direcciones IPv4 especiales y reservadas 

Estas son rangos de direcciones IPv4 reservadas para aplicaciones como el multicasting, estas direcciones IPv4 están descritas en el RFC 1112 y para propósitos de este capítulo están más allá del contexto del mismo. 

## 2.3. POLÍTICAS PARA LA DISTRIBUCIÓN Y ASIGNACIÓN DE DIRECCIONES IPv4 

### 2.3.1. Introducción 

En este capítulo se describirá cómo un Registro de Internet (Para futuras referencias este concepto comprende a Proveedores de Servicios de Internet y Registros Nacionales de Internet) puede obtener una distribución de direcciones IPv4 y cómo ese espacio distribuido deberá ser administrado. 

Los espacios de direcciones IPv4 son distribuidos a los Registros de Internet (IRs) usando un modelo de lento inicio. Las distribuciones están basadas en una necesidad justificada, no solamente sobre las bases de predicción de clientes. Debido a que el número de direcciones IPv4 es limitado, muchos factores deben considerarse en la delegación de espacios de direcciones IPv4. La idea es distribuir el espacio de direcciones IPv4 a los Registros de Internet en la misma relación en que estos asignarán las direcciones IPv4 a sus usuarios. 

El tamaño de una distribución a un IR en particular está basado en la tasa en la cual ha asignado anteriormente espacios de direcciones IPv4 a sus clientes. El objetivo es evitar la existencia de grandes bloques que no sean asignados a los usuarios finales. Debido a restricciones de tipo técnico y la posibilidad de sobrecarga en las tablas de rutas, deberán ser implementadas ciertas políticas para asegurar el cumplimiento de los objetivos de conservación y ruteabilidad. En este capítulo se habla de tamaños de prefijos y tamaños de bloques. La notación estándar implica que cuando se hable de prefijos mayores, se hace referencia a bloques de menor tamaño. Por ejemplo, cuando se menciona que cierta política se aplica a prefijo mayor a un /20, esto significa que se está hablando de un bloque menor de 16 /24. 

### 2.3.2. Aspectos a considerar en la administración de direcciones IPv4 

La presente sección describe un conjunto de aspectos sobre los cuales se debe basar la relación tanto entre los Registros de Internet y sus clientes, como entre los Registros de Internet y LACNIC. 

#### 2.3.2.1. Las direcciones IPv4 son delegadas 

LACNIC distribuirá recursos de Internet en un esquema de delegación. Este esquema de distribución de los recursos tendrá una validez de un año. Es posible la renovación de esta distribución y estará sujeta a las condiciones establecidas en el momento de la renovación. 

#### 2.3.2.2. Política de lento inicio 

Los bloques de direcciones IPv4 son distribuidos a los IRs usando un procedimiento llamado de lento inicio. Los Proveedores de Servicios de Internet que soliciten bloques de direcciones IPv4 portables (independientes del proveedor) por primera vez recibirán una cantidad mínima basándose en sus requerimientos inmediatos, a excepción de lo establecido en el punto 2.3.3.3. ("Distribuciones directas a proveedores de servicio internet"). 

A partir de esta distribución inicial los bloques distribuidos pueden ser incrementados basándose en la verificación de la utilización de los bloques en uso de acuerdo a la información provista a LACNIC. De esta manera LACNIC será responsable de determinar las distribuciones iniciales y subsecuentes. Las distribuciones de direcciones IPv4 iniciales deberán permitir a los IRs operar al menos por doce meses sin requerir nuevas ampliaciones. 

Las distribuciones iniciales no estarán basadas sobre ninguna restricción de ruteo ni actuales ni futuras, sino sobre necesidades reales y comprobables de uso de direcciones IPv4. 

Asimismo, el número de direcciones IPv4 proyectado por el solicitante es útil para la planeación de los requerimientos futuros del mismo. 

#### 2.3.2.3. Bloques distribuidos 

Para asegurar la eficiente implementación y uso de esquemas sin clases (CIDR), LACNIC distribuirá bloques de direcciones IPv4 en base a los límites soportados por este esquema. Para ayudar en el eficiente despliegue de CIDR, los Proveedores de Servicios de Internet (ISPs) y Usuarios Finales son alentados a solicitar espacio de direcciones IP inicialmente a sus proveedores inmediatos (upstream providers). El proveedor inmediato deberá mantener el control de los bloques asignados al término del contrato con sus clientes. 

#### 2.3.2.4. Evitar la fragmentación de bloques 

Las direcciones IP bajo el esquema CIDR son distribuidas a los IRs en bloques. Se recomienda que la publicación de estos bloques en las tablas de ruteo permanezca intacta. Más específicamente, los ISPs deberán tratar las asignaciones de direcciones IP a sus clientes como préstamos por la duración de la conectividad. En la terminación del contrato de conectividad de Internet, por ejemplo, si un cliente se cambia a otro ISP, el cliente tendrá que regresar las direcciones IPv4 que se encuentren actualmente en uso y renumerarlas con las nuevas direcciones IPv4 del nuevo proveedor. Nuevos pedidos de direcciones IP estarán condicionados a la finalización de esta tarea. El IR deberá ofrecer suficiente tiempo para que el proceso de renumeración finalice antes de que estas direcciones IP sean utilizadas de nuevo por otro cliente. 

#### 2.3.2.5. Documentación 

Los Registros de Internet deberán utilizar de manera eficiente el conjunto de direcciones IPv4 que les haya sido distribuido. Para este fin, los IRs deben documentar la justificación de cada asignación de direcciones IPv4. Ante requerimiento de LACNIC, esta información deberá ser proporcionada por el IR correspondiente. LACNIC no hará distribuciones complementarias a los Registros de Internet que no tengan correctamente documentado el uso de los bloques que ya se le hayan sido distribuidos previamente. Las distribuciones actuales podrán también ser revisadas en estos casos. 

La documentación a solicitar puede incluir: 

- Planes de Ingeniería. 
- Plan de subdivisión de redes (subnetting) y agregaciones. 
- Descripción de la topología de la red. 
- Descripción de planes de ruteo de la red. 
- Comprobantes de inversiones (equipamientos). 
- Otros documentos relevantes. 

#### 2.3.2.6. Uso del esquema sin clases (CIDR) 

Debido a los requerimientos de incrementar la eficiencia en la utilización de los espacios de direcciones IPv4, todas las distribuciones y o asignaciones son hechas con la suposición de que las organizaciones hacen uso de máscaras de subred de longitud variable (VLSM) y esquema sin clases (CIDR) dentro de sus redes. 
El uso de esquemas de clases es generalmente inaceptable debido a la limitada disponibilidad de espacio libre para direcciones IPv4. 

#### 2.3.2.7. Direccionamiento estático 

Debido a restricciones en la disponibilidad de direcciones IPv4, el uso de asignación de direcciones IPv4 de forma estática (ejemplo, una dirección por cliente) para usuarios dial−up no será respaldado de ninguna manera por LACNIC. Se entiende que el uso del direccionamiento estático puede facilitar algunos aspectos administrativos. Sin embargo, la actual tasa de consumo de las direcciones IPv4, no permiten justificar la asignación de direcciones estáticas por razones administrativas. Por esta razón, se espera que las organizaciones que están considerando el uso de asignación de direcciones IPv4 en forma estática, investiguen e implementen tecnologías de asignación dinámica. 

#### 2.3.2.8. Webhosting 

Con el desarrollo del protocolo HTTP 1.1 se ha eliminado la necesidad de la reserva de una dirección IP para cada dominio web en casos de múltiples websites en el mismo servidor. LACNIC promueve el desarrollo del alojamiento de páginas web basados en el uso del nombre en contraste al basado en direcciones IPv4. 

Por lo tanto, este último caso no será aceptado como justificación de uso de direcciones IPv4. LACNIC considerará las excepciones en que las aplicaciones necesiten el uso de webhosting basado en direcciones IPv4 lo que deberá ser debidamente descrito y justificado. 

#### 2.3.2.9.

Este punto ha sido intencionalmente dejado en blanco 

#### 2.3.2.10.

Este punto ha sido intencionalmente dejado en blanco 

#### 2.3.2.11.

Este punto ha sido intencionalmente dejado en blanco 

#### 2.3.2.12. Supervisión de asignaciones 

##### 2.3.2.12.1. Ventana de asignación 

Los ISPs podrán hacer asignaciones a sus clientes, de bloques menores de 16 /24 es decir prefijos mayores a /20, siguiendo la política definida por LACNIC en el presente documento. En algunos casos, la asignación deberá ser consultada con LACNIC o con el NIR correspondiente a los efectos de asegurar la optimización del uso del espacio de direcciones IP y la correcta aplicación de las políticas de LACNIC. 

LACNIC define como ventana de asignación, las asignaciones de bloques mayores o iguales a 2 /24 o sea prefijos menores o iguales a /23. Estas asignaciones deberán ser consultadas con LACNIC o con el NIR correspondiente. La comunicación entre los ISPs y LACNIC o el NIR correspondiente, deberá incluir la misma información y justificaciones establecidas para los usuarios finales, contenida en este documento. 

##### 2.3.2.12.2. Distribuciones a los NIRs 

Los NIRs quedarán exceptuados del cumplimiento del punto 3.2.12.1. En su lugar estarán sujetos a esquemas de auditorías más estrictos de acuerdo a lo estipulado en los contratos entre LACNIC y los NIRs. 

Estas auditorías serán hechas al menos una vez al año y con periodicidad mayor en caso de que sea necesario. 

#### 2.3.2.13. Registro de asignaciones 

Todas las asignaciones de bloques IPv4 de prefijos /29 o menores (bloques mayores) realizadas por ISPs a los clientes conectados a su red y los usuarios de los servicios prestados deben registrarse en la base de datos WHOIS de LACNIC en un plazo máximo de 7 días a partir de la asignación. 

La información disponible en la base de datos WHOIS también será utilizada por LACNIC cuando analice las solicitudes de bloques IPv4 adicionales realizadas por el ISP. 

El Registro de asignaciones también es necesario por los siguientes motivos: 

- Para asegurarse que el IR finalizó o está finalizando la distribución de espacio de direcciones de modo que se justifique la distribución de un nuevo espacio adicional. 
- Para proporcionar información a la comunidad Internet sobre cuál organización está usando el espacio de direcciones IPv4 incluyendo a la persona de contacto en caso de problemas de tipo operativo, de seguridad, etc. 
- Para el estudio de distribuciones de direcciones IPv4 en la región. 
- Para facilitar la geolocalización de las subasignaciones realizadas por los miembros en nuestra región. 

##### 2.3.2.13.1. Información necesaria 

Las asignaciones registradas en la base de datos WHOIS de LACNIC deben incluir la siguiente información sobre quien recibe la asignación: nombre de la organización, dirección postal, contactos administrativos, técnicos y de abuso con números de teléfono e correos electrónicos actualizados. 

###### 2.3.2.13.1.1 Clientes residenciales 

Los ISPs que ofrezcan servicios a clientes residenciales pueden registrar en la base de datos WHOIS de LACNIC bloques de direcciones en uso por los equipos o áreas de atención al cliente, por servicio. 

La información que se registre debe indicar el área de servicio, dirección postal principal del ISP, contactos administrativos, técnicos y de abuso del ISP con números de teléfono y correos electrónicos actualizados. 

Las asignaciones deben realizarse por bloques de direcciones que totalizan la cantidad de clientes atendidos en el área o por equipo. 

###### 2.3.2.13.1.2 Privacidad de Clientes residenciales 

Los clientes residenciales que reciban asignación de bloques IPv4 de prefijo /29 o menores (bloques mayores) no están obligados a tener sus datos registrados en la base de datos WHOIS de LACNIC. 

El ISP cuyo cliente residencial reciba asignación IPv4 de prefijo /29 o menor (bloque mayor) puede optar por registrar la asignación en la base de datos WHOIS de LACNIC colocando sus propios datos o código que le sirva de referencia interna. Los datos de contactos administrativos, técnicos y de abuso deben ser los del ISP. 

##### 2.3.2.13.2 Geolocalización 

Además de la información disponible en WHOIS, se publicar en un archivo las asignaciones hechas por LACNIC y las subasignaciones realizadas por sus miembros junto con la información del país en que se encuentra asignado el prefijo. El archivo podrá ser descargado por la comunidad de forma libre. Este archivo podrá ser empleado entre otras cosas para geolocalizar una IP. 

El formato y lugar de la publicación será definido por el staff de LACNIC.

#### 2.3.2.14. Seguridad y Confidencialidad 

LACNIC mantendrá sistemas y prácticas que cuiden y protejan la confidencialidad de toda información que a LACNIC le sea entregada en el envío de documentación para la justificación de la distribución o asignación de direcciones IPv4. 

#### 2.3.2.15. Igualdad en el procesamiento de solicitudes 

LACNIC tomará todas las solicitudes en el orden estricto en el cual estas sean recibidas, sin importar factores geográficos, demográficos, idiomáticos, etc. LACNIC bajo ninguna circunstancia dará trato especial o hará excepciones al estándar establecido para el procesamiento de solicitudes. Para esto contará con un sistema de numeración de solicitudes que le permita una buena administración de las mismas. 

#### 2.3.2.16. Microasignaciones 

LACNIC hará microasignaciones de prefijo mayor al estándar (bloque menor) en casos especiales que se enumeran en el punto 2.3.3 "Políticas para la distribución de espacio inicial de direcciones IPv4". 

#### 2.3.2.17. Fusiones, adquisiciones, reorganizaciones o reubicaciones 

Se recuerda que las políticas de LACNIC no reconocen la venta o transferencia no autorizada de los recursos asignados o distribuidos y considerará tales transferencias inválidas, con excepción de las transferencias que se sujeten a la sección 2.3.2.18. Sin embargo, LACNIC procesará y registrará la transferencia de recursos IPv4 como resultado de fusiones, adquisiciones, reorganizaciones o reubicaciones, ya sean parciales o completas, tanto si se trata de recursos de ISPs o usuarios finales. Para tramitar dicho cambio y proceder al registro, se deberá proporcionar documentación legal que lo respalde a criterio de LACNIC, por ejemplo: 

- Una copia del documento legal que respalda las transferencias de activos. 
- Un inventario detallado de todos los activos utilizados por el solicitante con el cual mantendrá en uso el espacio el recurso. 
- Una lista de los clientes de la parte solicitante que usa los recursos. 

Se deberá justificar también que sigue manteniéndose la necesidad del conjunto de los recursos, obligándose si fuera el caso, al retorno de los excedentes de los mismos o alternativamente a su transferencia a terceras partes, atendiendo a lo que corresponda según las políticas vigentes (2.3.3. y 2.3.4.). En el caso de un retorno, LACNIC determinará las condiciones y plazo.

#### 2.3.2.18. Transferencias de direcciones IPv4 

Se permitirán transferencias de direcciones IPv4 entre LIRs y/o usuarios finales, en adelante entidades, bajo las condiciones establecidas en la presente sección. Esta política aplica tanto a los casos en que alguna de las entidades involucradas sea de otra región (transferencias inter-RIR), como para transferencias dentro de la región LACNIC (transferencias intra-RIR). 

!##### 2.3.2.18.1. El tamaño mínimo de bloque que se permite transferir es un /24.

!##### 2.3.2.18.2. Para que una entidad dentro de LACNIC, pueda ser el destinatario de una transferencia, debe pasar primero por el proceso de justificación de recursos IPv4 ante LACNIC. Es decir, la entidad debe justificar ante LACNIC la distribución/asignación inicial/ adicional, según sea el caso, de acuerdo a las políticas vigentes. Si el destinatario es una entidad de otra región, estará sujeta a los criterios, verificaciones y requisitos del RIR correspondiente. 

!##### 2.3.2.18.3. LACNIC o el RIR correspondiente (en función de la dirección de la transferencia), verificará la titularidad del recurso a transferir y que esté libre de disputas. En los casos de transferencias intra-RIR, ambas entidades deberán presentar a LACNIC una copia firmada del documento legal que respalde la transferencia. En los casos de transferencias inter-RIR, la documentación que respalda la operación será la acordada entre ambos RIR. 

!##### 2.3.2.18.4. LACNIC mantendrá una bitácora de transferencias, accesible públicamente, de todas las transferencias de bloques IPv4 que se registren ante él. En dicha bitácora se registrará la fecha de la operación, la entidad fuente de la transferencia, la entidad destino, las direcciones transferidas y, si fuera una transferencia inter-RIR, los RIRs fuente y destino. 

!##### 2.3.2.18.5. La entidad fuente de la transferencia quedará automáticamente inelegible para recibir distribuciones y/o asignaciones de recursos IPv4 por parte de LACNIC durante un año, a partir de la fecha de operación registrada en la bitácora de transferencias. 

!##### 2.3.2.18.6. Las direcciones previamente transferidas no podrán ser subsecuentemente transferidas (ni total, ni parcialmente) durante un periodo de un año, a partir de la fecha de operación registrada en la bitácora de transferencias.

!##### 2.3.2.18.7. Una vez concluida la transferencia, LACNIC modificará la información del recurso transferido para reflejar el cambio de titular. 

!##### 2.3.2.18.8. Cada entidad, tanto la que transfiere como la que recibe, quedará sujeta a las políticas y condiciones de membresía del RIR correspondiente. 

!##### 2.3.2.18.9. Las direcciones provenientes de distribuciones o asignaciones de LACNIC, ya sean iniciales o adicionales, no podrán ser sujetos a transferencias (ni totales ni parciales) durante un periodo de tres años a partir de su fecha de distribución o asignación. 

!##### 2.3.2.18.10. Los recursos legados transferidos entrantes, dejarán de ser considerados legados.

### 2.3.3. Distribución y asignación inicial de direcciones IPv4 

LACNIC distribuirá direcciones IPv4 a organizaciones que entren en los siguientes casos: 

- Distribuciones a Proveedores de Servicios de Internet 
- Micro asignaciones a Infraestructura Crítica 
- Distribuciones Directas a Proveedores de Servicios de Internet. 
- Asignaciones a Usuarios Finales. 

Esta sección describe en detalle las políticas a aplicar por LACNIC para la distribución inicial de direcciones IPv4 portables (independiente del proveedor) en cada uno de estos casos. Debido a que el número de direcciones IPv4 disponibles en Internet es limitado, muchos factores deben ser considerados en la determinación de la distribución del espacio de direcciones IPv4. Por consiguiente, el espacio de direcciones IPv4 es distribuido a los ISPs siguiendo un modelo de lento inicio. Las distribuciones están basadas en una necesidad justificada actual y no en base a predicciones de número de clientes, estudios de mercado, etc. 

#### 2.3.3.1. Distribución inicial a ISPs

El tamaño mínimo de distribución inicial aplicado a Proveedores de Servicios de Internet establecido en la región LACNIC es de un /24. 

2.3.3.1.1. Requisitos para un prefijo /24 a un /22 

Para calificar para la distribución de un prefijo /24 a un /22 el ISP solicitante deberá cumplir los siguientes requisitos 

1. Demostrar el uso o la necesidad inmediata de al menos el 25% del prefijo solicitado. 
2. Entregar un plan detallado de uso de 50% de uso del prefijo solicitado para un año. 
3. Si previamente había un bloque asignado por un proveedor, y se desea mantener el mismo para evitar la renumeración, y hay acuerdo entre ambas partes, se podrá ceder dicho bloque (con el cambio de titularidad en el whois, a través de LACNIC).

Si se ha justificado espacio adicional y es posible su distribución, el receptor podrá decidir si la cesión le es conveniente y recibe un bloque por el espacio adicional o prefiere un único bloque por el total y, por lo tanto, renumera. En caso de renumeración, el bloque previamente asignado deberá ser retornado en un plazo máximo de 12 meses. Excepcionalmente, este plazo podrá ser extendido en 6 meses adicionales si se justifica que no ha habido tiempo para la consecución de los recursos que precisa y la renumeración correspondiente. 

4. En caso de que el solicitante aun no cuente con un bloque IPv6 asignado por LACNIC, solicitar al mismo tiempo un bloque IPv6 cumpliendo con la política aplicable.

##### 2.3.3.1.2. Requisitos para un prefijo /21 o menor (bloque de 8 /24 o más)

En caso de que el ISP solicitante requiera una distribución inicial de direcciones IPv4 a partir de un prefijo /21 deberá cumplir los siguientes requerimientos 

1. Proveer información de las asignaciones realizadas por prefijos de longitudes /29 o menores (más de 8 direcciones IPv4) en el WHOIS de LACNIC 

2. Proveer documentación justificando la distribución de espacio de direcciones inicial. (Llenado de la plantilla de solicitud de direcciones IPv4 para ISP). Se deberá incluir información detallada mostrando cómo será utilizado ese recurso dentro de los periodos de tres, seis y doce meses 

3. Si previamente había un bloque asignado por un proveedor, y se desea mantener el mismo para evitar la renumeración, y hay acuerdo entre ambas partes, se podrá ceder dicho bloque (con el cambio de titularidad en el whois, a través de LACNIC).

Si se ha justificado espacio adicional y es posible su distribución, el receptor podrá decidir si la cesión le es conveniente y recibe un bloque por el espacio adicional o prefiere un único bloque por el total y, por lo tanto, renumera. En caso de renumeración, el bloque previamente asignado deberá ser retornado en un plazo máximo de 12 meses. Excepcionalmente, este plazo podrá ser extendido en 6 meses adicionales si se justifica que no ha habido tiempo para la consecución de los recursos que precisa y la renumeración correspondiente. 

4. En caso de que el solicitante aun no cuente con un bloque IPv6 asignado por LACNIC, solicitar al mismo tiempo un bloque IPv6 cumpliendo con la política aplicable.

Adicionalmente se deberán considerar los siguientes requerimientos dependiendo del status multiproveedor o no multiproveedor del ISP solicitante:

Si el solicitante es un ISP multiproveedor, pronto a serlo o tiene necesidades de interconexión:

Estar utilizando eficientemente un equivalente al 25% del espacio solicitado como mínimo (contiguo o no).

En caso de ser multiproveedor indicar nombre y número de sistema autónomo de sus proveedores.

En caso de estar pronto a ser multiproveedor o tener necesidades de interconexión con otros sistemas autónomos describir detalladamente el plan y los plazos (es recomendable presentar contratos o cartas de intención firmadas).

Si el solicitante es un ISP no multiproveedor: 

Estar utilizado eficientemente un 50% del espacio solicitado como mínimo (contiguo o no).

#### 2.3.3.2. Microasignaciones a infraestructura crítica 

Se llaman microasignaciones a aquellas que signifiquen prefijos mayores o iguales a un / 22 pero siempre menores o iguales a un /24. LACNIC podrá realizar este tipo de asignación en casos de proyectos e infraestructuras de redes claves o críticas para la región como son IXP (Internet Exchange Point), NAP (Network Access Point), RIR, ccTLD entre otros. 

En el caso de los IXP o NAP para poder solicitar este tipo de asignación las organizaciones deberán cumplir los siguientes requisitos: 

1. Documentar adecuadamente los siguientes aspectos: 
1.1. Demostrar a través de sus estatutos su calidad de IXP o NAP. Deberá poseer al menos tres miembros y una política abierta para la asociación de nuevos miembros. 
1.2. Enviar un diagrama de la estructura de red de la organización. 
1.3. Documentar el plan de numeración a instrumentar. 

2. Proveer un plan de utilización para los próximos tres y seis meses. En el resto de las solicitudes se estudiarán basados en el análisis de documentación que justifique los aspectos críticos y/o claves del proyecto. 

3. En caso de que el solicitante aun no cuente con un bloque IPv6 asignado por LACNIC, solicitar al mismo tiempo un bloque IPv6 cumpliendo con la política aplicable. 

La organización que reciba una micro asignación no podrá realizar asignaciones con estas direcciones IPv4.

#### 2.3.3.3. Distribuciones directas a proveedores de servicio de internet 

LACNIC reconoce que pueden existir circunstancias donde existan necesidades justificadas de realizar una distribución inicial de un /20 o un prefijo menor. 

LACNIC podrá realizar este tipo de distribución a aquellas organizaciones que cumplan con los siguientes requisitos: 

1. Ser organización multiproveedor, o ser proveedor de servicios de Internet y demostrar la posibilidad de Interconexión con otros proveedores o puntos de intercambio de tráfico (NAP/IXP). 

2. Enviar una descripción detallada de la topología de red. 

3. Enviar un portafolio con descripción detallada de los servicios a ofrecer. 

4. Enviar un plan detallado del despliegue del uso del direccionamiento a tres, seis y doce meses. 

5. En caso de que el solicitante aun no cuente con un bloque IPv6 asignado por LACNIC, solicitar al mismo tiempo un bloque IPv6 cumpliendo con la política aplicable. 

LACNIC puede en cualquier momento solicitar para este tipo de distribuciones información adicional que ayude a la justificación de un mínimo de distribución.

#### 2.3.3.4. Asignaciones a Usuarios Finales 

LACNIC asignará bloques de direcciones IPv4 a usuarios finales que requieren espacio de direcciones IPv4 para su uso interno, para el funcionamiento de sus redes. 

Generalmente los usuarios finales reciben espacio de direcciones IPv4 de sus proveedores inmediatos, no directamente de LACNIC. Las direcciones IPv4 portables (independientes del proveedor) obtenidas directamente de LACNIC u otros Registros Regionales no están garantizadas a ser globalmente ruteables. 

Por esta razón, los usuarios finales deberían contactar a sus Proveedores de Servicios de Internet para asegurar su conectividad dentro de la red. 

Los usuarios finales que no están conectados a un ISP y/o planean no estar conectados a Internet se les recomienda usar direcciones IPv4 privadas. Pueden consultar la descripción de tales direcciones IP en el RFC 1918.

##### 2.3.3.4.1. Información requerida 

LACNIC solicitará la siguiente información a todos los usuarios finales que solicitan bloques de direcciones IPv4. 

1. Proveer información detallada mostrando como el bloque solicitado será utilizado dentro de tres, seis y doce meses 
2. Entregar planes de subneteo por al menos un año, incluyendo máscaras de subred y números de hosts sobre cada subred. El uso de VLSM es requerido. 
3. Entregar una descripción detallada de la topología de la red. 
4. Realizar una descripción detallada de los planes de ruteo de la red, incluyendo los protocolos de ruteo a ser usado también como cualquier limitación existente. 
5. En caso de que el solicitante aun no cuente con un bloque IPv6 asignado por LACNIC, solicitar al mismo tiempo un bloque IPv6 cumpliendo con la política aplicable.

##### 2.3.3.4.2. Tasa de utilización 

La tasa de utilización es un factor clave a justificar para dimensionar el tamaño de la asignación. La tasa de utilización es el porcentaje de direcciones IPv4 que la organización utilizará en un espacio de tiempo determinado. El adoptado por LACNIC es: 

25% de utilización inmediata del bloque solicitado. 
50% de utilización a un año del bloque solicitado. 

Una tasa de utilización más grande puede ser requerida basada en requerimientos individuales. Si la organización solicitante no cumple con esos parámetros se le podrán retirar las direcciones negociando un tiempo razonable para su renumeración. 

##### 2.3.3.4.3.Tamaño de la asignación y procedimiento 

El solicitante debe justificar que anunciará el espacio asignado, con su propio sistema autónomo, al menos a otro sistema autónomo. El tamaño de asignación mínima de direcciones IPv4 para un usuario final es de un bloque con prefijo /24 y el tamaño máximo será un /20, el cual deberá ser justificado, de acuerdo con la tasa de utilización (sección 2.3.3.4.2). 

Si previamente había un bloque asignado por un proveedor, y se desea mantener el mismo para evitar la renumeración, y hay acuerdo entre ambas partes, se podrá ceder dicho bloque (con los cambios correspondientes en el whois). Si se ha justificado espacio adicional y es posible su asignación, el receptor podrá decidir si la cesión le es conveniente y recibe un bloque por el espacio adicional o prefiere un único bloque por el total y, por lo tanto, renumera. En caso de renumeración, el bloque previamente asignado deberá ser retornado en un plazo máximo de 6 meses. Excepcionalmente, este plazo podrá ser extendido en 6 meses adicionales si se justifica que no ha habido tiempo para la consecución de los recursos que precisa y la renumeración correspondiente. 

Para asignaciones adicionales se seguirán las políticas incluidas en la sección 2.3.4 aplicables a los usuarios finales. 

### 2.3.4. Políticas para la distribución de espacio adicional de direcciones IPv4 

Esta política es presentada con el propósito de asistir a los Registros de Internet en el proceso de solicitud de espacio adicional de direcciones IPv4. El factor más importante en la evaluación de las solicitudes de espacio adicional de direcciones IPv4 es la revisión del espacio actual de direcciones lPv4 de las entidades solicitantes. 

La entidad solicitante debe haber utilizado al menos el 80% de su espacio de direcciones IPv4 de las distribuciones realizadas anteriormente por el RIR o NIR correspondiente con el fin de recibir un espacio adicional. Esto incluye el espacio asignados a sus clientes. Por consiguiente, es importante que los IRs requieran a sus clientes seguir las prácticas de eficiente utilización descritas en estas políticas. 

Para la distribución de nuevos bloques de direcciones IPv4 los siguientes son los aspectos a cumplir:

1. El primer paso en el proceso es verificar la utilización de al menos el 80% de las distribuciones anteriores. Este porcentaje de utilización será basado solamente en aquellas redes anunciadas con direcciones IPv4 conectadas a Internet. El método disponible para mostrar esta utilización para aquellos IRs que han asignados direcciones IPv4 a sus clientes, es a través de los registros en la base de datos WHOIS de LACNIC. Hasta que se verifique el uso de por lo menos el 80% de su bloque previamente distribuido se podrá seguir considerando su solicitud. El uso del 80% de las direcciones IP distribuidas previamente cubre también aquellas direcciones utilizadas para uso interno y clientes dial−up de la compañía. Para este último caso pueden justificar su utilización a través del reporte del apéndice 3 [Reporte adicional para la distribución de espacio de direcciones IPv4]. Organizaciones que realicen asignaciones estáticas, podrán justificar la utilización a través del reporte del apéndice 4 [Reporte de distribución de recursos IPv4]. Una vez que se haya verificado al menos el 80% de utilización del espacio previamente distribuido, se continuará el proceso de solicitud de espacio adicional. 

2. Las organizaciones deberán demostrar el uso de las políticas de LACNIC en la asignación de espacio a sus clientes, en especial en lo referido a:

- La emisión de prefijos de longitudes más grandes que /24, donde esto sea posible. 
- Verificar que las asignaciones de bloques dentro de la ventana de asignación fueron enviados para la previa autorización de LACNIC. 

3. Las organizaciones deberán exigir que sus clientes se adhieran a los siguientes criterios: 

- La información de las asignaciones menores a un /29 debe de estar disponible vía WHOIS y deben cumplir con el 80% de su espacio utilizado antes de emitirles a sus clientes el espacio adicional. 
- Las políticas de LACNIC para la comunidad en Internet en general son comunicadas y seguidas por sus clientes. 

4. En la revisión de solicitudes para direcciones IPv4 adicionales, LACNIC también revisará si el espacio designado para devolución fue realmente devuelto en los tiempos descritos en este documento. 

5. Estar al día en el registro de la resolución inversa del espacio de direcciones IPv4 administrado. El registro de la resolución inversa también debe coincidir con el 80% de utilización. 

6. Para la distribución de bloques adicionales, LACNIC verificará que la organización solicitante este al día en sus obligaciones contractuales. 

7. El solicitante debe tener al menos un bloque IPv6 asignado por LACNIC o en caso contrario debe solicitar simultáneamente un bloque inicial IPv6 cumpliendo con la política aplicable vigente para tal fin. En caso de que el solicitante ya cuente con un bloque IPv6 previamente asignado remitirá a LACNIC un documento breve que describa sus avances en la integración del protocolo IPv6. 

8. El paso final es determinar la distribución apropiada a ser emitida. Para poder determinar el tamaño de la distribución a realizar se deberá proveer información detallada mostrando como será utilizado el espacio de direcciones IPv4 dentro de los periodos de tres, seis y doce meses. La política del tamaño de la distribución adicional está basada en la eficiente utilización de espacio dentro de un marco de tiempo de 12 meses.

### 2.3.5. Reserva especial de direcciones IPv4 para infraestructura crítica para la operación de Internet en la región. 

1. Esta reserva entrará en funcionamiento una vez que haya terminado el espacio de direcciones considerado para la Fase 3 de Agotamiento de IPv4 en la región. 

2. LACNIC creará una reserva equivalente a un /15 de direcciones IPv4 para facilitar el despliegue de infraestructura considerara crítica o esencial para la operación de Internet en la región, entendiéndose por infraestructura crítica la definición mostrada en el punto 2.3.3.2 del Manual de Políticas. 

3. La solicitud de direccionamiento para infraestructura crítica puede realizarse en cualquier momento. 

4. La asignación de direcciones de esta reserva estará acotada a los siguientes tamaños: asignación mínima: /24 asignación máxima: /22 

5. El tamaño de la asignación estará sujeto a la comprobación de uso y el análisis por LACNIC o el NIR correspondiente. 
6. Las direcciones asignadas bajo este punto deberán ser devueltas a LACNIC o al NIR correspondiente una vez que la necesidad original de la solicitud haya terminado. 

7. Las direcciones asignadas a partir de esta reserva no podrán ser utilizadas para un propósito distinto del que haya generado la solicitud. La ocurrencia de este evento ocasionará la revocación de la asignación y la subsecuente devolución de las direcciones a LACNIC o al NIR correspondiente.

### 2.3.6. Permiso de transferencia y no-devolución de recursos 

Aunque inicialmente las políticas de distribución y asignación de direcciones están basadas en justificación de necesidad, la implantación de las transferencias deshabilita el mantenimiento de dicha justificación y, por lo tanto, no será obligatorio devolver recursos a LACNIC en caso de transferencias o fusiones y adquisiciones fallidas.