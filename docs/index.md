# RESUMEN

La distribución de espacio de los recursos de numeración sigue un esquema jerárquico. Para el área de Latinoamérica y el Caribe el espacio de direcciones IP es distribuido por IANA a LACNIC para ser a su vez distribuidos y asignados a Registros Nacionales de Internet (NIR), Proveedores de Servicios de Internet (ISP) y usuarios finales. Asimismo la administración de los Números de Sistemas Autónomos y el espacio de resolución inversa conforman una parte crítica para la eficiente operación de Internet a nivel global.

En este documento describimos las políticas y procedimientos asociados con la distribución, asignación y administración del espacio de direcciones IPv4, IPv6, ASN y la delegación del espacio de resolución inversa asignados a Latinoamérica y el Caribe.

Estas políticas deberán ser seguidas por los NIRs, ISPs y los usuarios finales.

# 1. DEFINICIONES 

Los siguientes términos y sus definiciones son de gran importancia para la comprensión de los objetivos, contextos y políticas descritas en este documento. La distribución de espacio de los recursos de numeración sigue un esquema jerárquico. La responsabilidad de la administración del espacio de direcciones de IP está distribuida globalmente de acuerdo con la estructura jerárquica que se muestra debajo 

## 1.1. IANA (Internet Assigned Number Authority) 

IANA es responsable de distribuir parte del espacio global de las direcciones IP y los números de sistemas autónomos a Registros Regionales de acuerdo a necesidades establecidas. 

## 1.2. Registro de Internet (IR) 

Un Registro de Internet (IR) es una organización responsable de la distribución de espacios de direcciones IP a sus miembros o clientes y del registro de esa distribución. Los IRs están clasificados de acuerdo a su función principal y alcance territorial dentro de la estructura jerárquica delineada en la figura de arriba. 

## 1.3. Registro de Internet Regional (RIR) 

Los Registros de Internet Regionales (RIRs) son establecidos y autorizados por las comunidades regionales respectivas, y reconocidos por el IANA para servir y representar grandes regiones geográficas. El rol principal de los RIRs es administrar y distribuir los recursos de Internet dentro de las respectivas regiones. 

## 1.4. Registro de Internet Nacional (NIR) 

Un Registro de Internet Nacional (NIR) distribuye, principalmente, los recursos de Internet a sus miembros o constituyentes, los cuales generalmente son LIRs. 

## 1.5. Registro de Internet Local (LIR) 

Registro de Internet Local (LIR) es un IR que a su vez asigna recursos de Internet a usuarios de los servicios de red que éste provee. Los LIRs son generalmente ISPs, cuyos clientes son principalmente usuarios finales y posiblemente otros ISPs. 

## 1.6. Proveedor de Servicios de Internet (ISP) 

Un Proveedor de Servicios de Internet asigna principalmente espacio de direcciones IP a los usuarios finales de los servicios de red que éste provee. Sus clientes pueden ser otros ISPs. Los ISPs no tienen restricciones geográficas como lo tienen los NIRs. 

## 1.7. Sitio Final o Usuario Final (EU) 

Un end site es definido como un usuario final (suscriptor) que tiene una relación de negocios o legal (misma o entidades asociadas) con un proveedor de servicios Internet que involucra:

- al proveedor de servicios asignando un espacio de direcciones al usuario final 
- al proveedor de servicios otorgando un servicio de tránsito para el usuario final hacia otros sitios.
- al proveedor de servicios transportando el tráfico del usuario final 
- al proveedor de servicios anunciando un prefijo de ruta agregado que contiene el rango asignado por LACNIC al usuario final 

## 1.8. Distribuir

Distribuir significa delegar el espacio de direcciones a los IRs con el propósito de que ellos realicen la subsiguiente distribución. 

## 1.9. Asignar 

Asignar significa delegar espacio de direcciones a un usuario final, para su uso exclusivamente dentro de la infraestructura que opera, a , así como para fines de interconexión. 

La asignación de espacio de direcciones es sólo para el uso por el receptor original de dicha asignación, así como para dispositivos de terceros, siempre y cuando estén operando dentro de dicha infraestructura. 

No está permitida, por tanto, la subasignación a terceros, fuera de dicha infraestructura (por ejemplo, el uso de asignaciones de usuario final para clientes de un ISP o similares), ni proporcionar direccionamiento a terceros en data-centers (y similares). 

## 1.10. El sistema de registro de Internet

El sistema de registro de Internet ha sido establecido con la finalidad de hacer cumplir los objetivos de exclusividad, conservación, ruteabilidad e información. Este sistema consiste de Registros de Internet (IR) organizados jerárquicamente. Los recursos numéricos de Internet (direcciones, ASNs, otros) son típicamente asignados a los usuarios finales por los ISPs o los NIRs.

Por otra parte, estos recursos son previamente distribuidos a los NIRs e ISPs por parte de los Registros Regionales de Internet. 

Bajo este sistema los usuarios finales son aquellas organizaciones que operan redes en donde se utilizan los recursos. Los NIRs al igual que LACNIC mantienen recursos para ser asignados a usuarios finales o distribuidos a Proveedores de Servicios de Internet. Los recursos asignados son utilizados para la operación de redes, mientras que los recursos distribuidos se mantienen en los Registros de Internet para futuras asignaciones a sus usuarios finales. 

Se recuerda que los recursos distribuidos o asignados por LACNIC o los NIRs, lo son a título exclusivo para el uso por parte del receptor de los mismos, o con la autorización de éste, por parte de terceros, siempre y cuando lo permitan las políticas vigentes. Se recomienda que dichas autorizaciones puedan ser verificadas por medio de RPKI. 

## 1.11. Ruteabilidad no garantizada 

Ni LACNIC, ni los NIR garantizan la ruteabilidad de las direcciones distribuidas o asignadas. 

Los receptores de recursos son responsables de negociar dicha ruteabilidad con sus proveedores de conectividad. LACNIC proveerá en los casos en los que sea necesario, la orientación correspondiente. 

Sin embargo, los recursos distribuidos o asignados deben ser anunciados en un plazo máximo de 90 días, salvo en aquellos casos en que se justifique la necesidad de no hacerlo. 

Los RIRs deben aplicar procedimientos operativos que reduzcan la posibilidad de fragmentación del espacio de direcciones, para minimizar riesgos de pérdida de ruteabilidad. 

## 1.12. Multiproveedor 

Un sitio es multiproveedor si recibe conectividad de tiempo completo de más de un proveedor de servicios de Internet y tiene uno o más prefijos de ruteo anunciados por al menos dos de sus proveedores de conectividad. Se entiende como proveedores independientes a el hecho de que uno no utilice al otro para alcanzar Internet. 

## 1.13. ROAs RPKI con ASN 0 

LACNIC creará autorizaciones de origen (ROAs) específicas en la infraestructura de RPKI con AS 0 en el campo Origin ASN y la lista de recursos numéricos de Internet no distribuidos o no asignados exclusivamente bajo la administración de LACNIC en la lista de prefijos de tales ROAs. 

El número de los ROA antes mencionados y cualquier otro parámetro técnico quedará a discreción de LACNIC. 

Solo LACNIC tendría la autoridad para crear ROAs RPKI para los recursos numéricos de Internet aún no distribuidos ni asignados o bien para los recursos recuperados o devueltos, de los cuales LACNIC es el custodio legítimo. 

Una vez que un recurso numérico de Internet se distribuya o asigne, LACNIC invalidará los ROAs que contengan dicho recurso y emitirá otros nuevos donde el recurso no aparezca, según sea necesario. 

## 1.14. Principios para una buena administración/custodia 

El principio fundamental es la distribución de recursos de numeración de Internet únicos de acuerdo con las necesidades técnicas y operativas de las redes que hacen o harán uso de dichos recursos de numeración. Permitiendo el crecimiento y la sostenibilidad de Internet. 

Los recursos de numeración de Internet bajo la custodia de LACNIC se deben distribuir a organizaciones legalmente establecidas en su región de servicio y para atender mayoritariamente* redes y servicios que operan en dicha región. Se permite que clientes externos se conecten directamente a una infraestructura principal ubicada dentro de la región. 

Se entiende mayoritariamente como más del 50%. 

Los servicios de anycast con utilización de recursos fuera de la región son aceptables siempre que sean prestados por una organización legalmente establecida en la región de servicio y que al menos una copia del servicio se mantenga en infraestructura local. 
Al obtener cualquier tipo de recursos de LACNIC o el NIR correspondiente, en caso de tener recursos legados, estos dejan de ser considerados legados. 

### 1.14.1. Distribución racional 

Los recursos de numeración de Internet se deben distribuir garantizando su unicidad y teniendo en cuenta las necesidades técnicas operativas de las redes e infraestructuras que harán uso de los mismos.

Se deben tener en cuenta ciertas consideraciones en cuanto a las posibles limitaciones de los espacios disponibles para cada recurso de numeración en el momento de la distribución. 

### 1.14.2. Registro público de datos 

Proveer un registro público de datos relacionados con los recursos de numeración de Internet es un requisito fundamental del sistema de distribución de recursos de numeración de Internet.

Con el objeto fundamental de garantizar la unicidad y proveer información sobre el uso y datos de contacto en caso de problemas operativos o de seguridad. También para estudios sobre utilización de estos recursos. 

### 1.14.3. Distribución jerárquica 

La distribución de recursos de numeración de Internet en forma jerárquica contribuye a la escalabilidad del sistema de enrutamiento de las direcciones de Internet, permitiendo que las direcciones sean agrupadas y anunciadas de la manera más resumida posible. 

Los objetivos arriba mencionados pueden, en algunos casos, estar en conflicto entre sí o con los intereses particulares de las organizaciones solicitantes. En estos casos es necesario analizar cuidadosamente cada situación particular de manera de poder alcanzar un compromiso adecuado entre las diferentes partes involucradas en el conflicto. 

## 1.15. Solicitud de recursos 

Las solicitudes de recursos a LACNIC o los NIRs correspondientes, se realizarán con los sistemas en vigor. 

Cualquier solicitud que sea considerada incompleta, será regresada al solicitante con las debidas indicaciones, para poder ser completada.

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

3. DISTRIBUCIÓN DE NÚMEROS DE SISTEMA AUTÓNOMO (ASN) 

Un Sistema Autónomo (AS) es un grupo de redes de direcciones IP que son gestionadas por uno o más operadores de red que poseen una clara y única política de ruteo. Cada Sistema Autónomo tiene un número asociado el cual es usado como un identificador para el Sistema Autónomo en el intercambio de información del ruteo externo. Los protocolos de ruteo externos tales como BGP son usados para intercambiar información de ruteo entre Sistemas Autónomos. 

La expresión Sistema Autónomo es con frecuencia interpretada incorrectamente como apenas una forma conveniente de agrupar redes que están bajo de una misma gestión. Sin embargo, en el caso en que hay más de una política de ruteo en el grupo, más de un AS es necesario. Por otro lado, si el grupo de redes posee la misma política que los otros grupos, estos quedan dentro del mismo AS independientemente de la estructura de la gestión. De esta manera, por definición, todas las redes que componen un AS comparten la misma política de ruteo. 

Con el objetivo de disminuir la complejidad de las tablas rutas globales, un nuevo Número de Sistema Autónomo (ASN), debe ser asignado solamente en el caso en que una nueva política de ruteo es necesaria. 

Compartir un mismo ASN entre un grupo de redes que no están bajo de la misma gestión va a requerir una coordinación adicional entre los administradores de las redes y en algunos casos, va a requerir algún nivel de rediseño de la red. Sin embargo, esta es probablemente la única forma de implementar una política de ruteo deseada. 

LACNIC distribuirá Números de Sistema Autónomo a las organizaciones que cumplan con los siguientes requisitos:

1. La organización debe tener necesidad de interconexión con otros sistemas autónomos al momento de la solicitud, o tener programada la necesidad de interconexión en menos de 6 meses a partir del momento de la solicitud, luego de cumplido este plazo LACNIC podrá revocar el ASN asignado en caso el recurso no haya sido utilizado. 
2. Detallar la política de ruteo de la organización solicitante, indicando los ASN con los que se interconectarán y las direcciones IP que serán anunciadas a través del ASN solicitado.

Es obligación de la organización que reciba un Número de Sistema Autónomo de LACNIC, el mantener las informaciones de dirección postal y puntos de contactos actualizados. 

En el sistema WHOIS de LACNIC es posible representar hasta 3 puntos de contacto distintos que son: 
owner−c, que representa el contacto administrativo de la organización a la que el ASN fue asignado; 
routing−c, contacto que puede registrar, a través del sistema de administración de IP y ASN, las políticas de enrutamiento adoptadas por ese Sistema Autónomo; 
abuse−c, contacto de seguridad (Abuse Contact). 

## 3.1.Terminología 

Los números de sistemas autónomos de 16 bits fueron definidos en la RFC 1930 y se utilizará para su identificación números enteros del 0 al 65535. Igualmente, los números de sistemas autónomos de 32 bits fueron definidos por la RFC 4893 y se utilizarán para su identificación números enteros del 0 al 4294967295. Utilizando en ambos casos la representación textual del valor decimal “asplain” definida en el RFC 5396. 

Consecuentemente, se tomará la siguiente terminología para ASNs de 16 y 32 bits: 

- "Números de AS sólo de 16 bits" se refiere a Números de AS en el rango de 0 – 65535 
- "Números de AS sólo de 32 bits" se refiere a Números de AS en el rango de – 65536 - 4294967295 
- "Números de AS de 32 bits" se refiere a Números de AS en el rango de 0 – 4294967295

## 3.2. Etapas de distribución de AS 

Existirán tres etapas para la distribución de ASNs por parte de LACNIC: 

1. El 1º de enero de 2007 el registro procesará las solicitudes que específicamente solicitan Números de AS sólo de 32 bits y distribuirá dichos Números de AS según lo pedido por el solicitante. En ausencia de solicitudes específicas para obtener un Número de AS sólo de 32 bits, el registro distribuirá un Número de AS sólo de 16 bits. 

2. El 1º de enero de 2009 el registro procesará las solicitudes que específicamente solicitan Números de AS sólo de 16 bits y distribuirá dichos Números de AS según lo pedido por el solicitante. En ausencia de solicitudes específicas para obtener un Número de AS sólo de 16 bits, el registro distribuirá un Número de AS sólo de 32 bits. 

3. A partir del 1o de enero de 2010 LACNIC distribuirá Nú́meros de AS solo de 32 bits por omisión. Se asignarán Números de AS solo de 16 bits, siempre que haya disponibilidad, en respuesta a solicitudes que explícitamente, así lo pidan y justifiquen debidamente las razones técnicas por las cuales un Número de AS solo de 32 bits no es adecuado para sus necesidades.

## 3.3. Fusiones, adquisiciones, reorganizaciones o reubicaciones

Se recuerda que las políticas de LACNIC no reconocen la venta o transferencia no autorizada de los recursos asignados o distribuidos y considerará tales transferencias inválidas. 

Sin embargo, LACNIC procesará y registrará la transferencia de recursos ASN como resultado de fusiones, adquisiciones, reorganizaciones o reubicaciones, ya sean parciales o completas, tanto si se trata de recursos de ISPs o usuarios finales. 

Para tramitar dicho cambio y proceder al registro, se deberá proporcionar documentación legal que lo respalde a criterio de LACNIC, por ejemplo: 

- Una copia del documento legal que respalda las transferencias de activos.
- Un inventario detallado de todos los activos utilizados por el solicitante con el cual mantendrá en uso el espacio el recurso.
- Una lista de los clientes de la parte solicitante que usa los recursos.

Se deberá justificar también que sigue manteniéndose la necesidad del conjunto de los recursos, obligándose si fuera el caso, al retorno de los excedentes de los mismos o alternativamente a su transferencia a terceras partes, atendiendo a lo que corresponda según las políticas vigentes (3.). En el caso de un retorno, LACNIC determinará las condiciones y plazo.

## 3.4. Inclusión del ASN originador en el WHOIS cuando estuviera disponible 

LACNIC deberá incluir en la información del WHOIS el ASN originador de los prefijos consultados, siempre que esta información estuviera disponible.

El ASN originador del bloque en custodia podrá ser tomado del repositorio de RPKI, tomando como valor el ASN de origen del ROA.

En las situaciones en las que la información de ASN originador de un bloque no estuviera especificada, la respuesta del WHOIS deberá indicar ese hecho.

# 4. POLÍTICAS PARA LA DISTRIBUCIÓN Y ASIGNACIÓN DE DIRECCIONES IPv6 

## 4.1. Alcance 

Este capítulo describe políticas para la distribución y asignación del espacio globalmente único de direcciones IPv6.

[RFC2373, RFC2373bis] designan 2000::/3 a ser el espacio global de direcciones unicast que IANA puede distribuir a los RIRs. Este capítulo trata las distribuciones iniciales y subsiguientes del espacio de direcciones unicast 2000::/3, para los cuales los RIRs formulan políticas de distribución y asignación. Dado que los usuarios finales generalmente recibirán asignaciones de /48 [RFC 6177], el énfasis particular de este documento es sobre recomendaciones a los LIR/ISPs para las asignaciones a sus usuarios y clientes conectados" 

## 4.2. Definiciones 

Los siguientes términos son específicos de las políticas de distribución de IPv6. 

### 4.2.1. Utilización 

A diferencia de IPv4, IPv6 es generalmente asignado a usuarios finales en cantidades fijas. La utilización real de direcciones dentro de cada asignación será bastante baja comparada con las asignaciones de IPv4. En IPv6, la "utilización" es medida en términos de prefijos asignados a usuarios finales, y no al tamaño de los mismos, ni al número de direcciones realmente utilizadas dentro de dichos prefijos, y así deberá entenderse a lo largo de este documento. 

### 4.2.2. HD Ratio 

El HD Ratio es un modo de medir la eficiencia de asignación de direcciones [RFC 3194]. Es una adaptación del HD Ratio, originalmente definido en [RFC 1715], y es expresado de la siguiente manera: 

```txt
      Log (número de objetos asignados) 
HD = ------------------------------------------- 
      Log (número máximo de objetos asignables) 
```

donde, en el caso de este documento, los objetos son direcciones IPv6 de usuarios (/48s) asignadas desde un prefijo IPv6 de un tamaño dado (ver Apéndice 2).

## 4.3.Principios de la política IPv6

Para cumplir con los objetivos descritos en la sección anterior, las políticas en este capítulo discuten y siguen los principios básicos descritos debajo. 

### 4.3.1. Espacio de direcciones no debe ser considerado propietario

Es contrario a los objetivos de este documento y no se encuentra entre los intereses de la comunidad de Internet en su conjunto que los espacios de direcciones sean considerados propietarios. 

Las políticas en este capítulo se basan en el entendimiento de que el espacio globalmente único de direcciones unicast de IPv6 es licenciado para su uso en lugar de adueñado. Específicamente, las direcciones IP serán distribuidas y asignadas en base a una licencia, con licencias sujetas a renovación periódica. La otorgación de una licencia está sujeta a condiciones específicas a aplicarse al comienzo como así también en cada renovación de la misma. 

Los RIRs generalmente renovarán las licencias automáticamente, siempre que las organizaciones solicitantes hagan un esfuerzo de buena fe para cumplir con el criterio bajo el cual calificaron o fueron otorgadas una distribución o asignación. Sin embargo, en aquellos casos en que una organización no está utilizando el espacio de direcciones como se espera, o está mostrando mala fe en regirse por las obligaciones asociadas, los RIRs se reservan el derecho de no renovar la licencia. 

Notar que cuando una licencia es renovada, la nueva licencia será evaluada y controlada bajo las políticas de direcciones de IPv6 aplicables en el lugar y momento de la renovación, las cuales podrían diferir de las políticas bajo las cuales fue originalmente distribuida o cedidas.

### 4.3.2. Distribución Mínima 

Los RIRs aplicarán un tamaño mínimo para distribuciones de IPv6 para facilitar el filtro basado en el prefijo. 

El tamaño mínimo de distribución para un espacio de direcciones IPv6 es /32. 

### 4.3.3. Consideraciones de la infraestructura de IPv4 

Cuando un proveedor de servicios de IPv4 pide espacio IPv6 para una transición final de servicios existentes a IPv6, el número de clientes actuales de IPv4 podría ser usado para justificar un pedido más grande del que estaría justificado si el mismo estuviera basado solamente en la infraestructura IPv6.

## 4.4. Políticas para distribución y asignación 

### 4.4.1. Distribución inicial 

#### 4.4.1.1. Distribuciones de direcciones IPv6 a LIR o ISP con distribuciones IPv4 previas realizadas por LACNIC. 

LACNIC distribuirá́ bloques de direcciones IPv6 a un LIR o ISP que cuente con distribuciones de direcciones IPv4 previamente realizadas por LACNIC. En caso de anunciar la asignación en el sistema de rutas inter-dominio de Internet, la organización receptora deberá́ anunciar el bloque asignado con la mínima desagregación que le sea posible a quien está publicando los bloques IP. 

LACNIC realizará una distribución de un /32 al recibir una solicitud de direccionamiento IPv6 por parte de un LIR o ISP con distribuciones previas de IPv4. En caso de requerir una distribución inicial más grande que un /32, el LIR o ISP deberá presentar la documentación requerida según el punto 4.4.1.3. 

#### 4.4.1.2. Distribuciones de direcciones IPv6 a LIR o ISP sin distribuciones IPv4 previas realizadas por LACNIC. 

Para calificar para la distribución inicial de un espacio de direcciones IPv6, una organización debe: 

- Ser un LIR o ISP. 
- Documentar un plan detallado sobre los servicios y la conectividad en IPv6 a ofrecer a otras organizaciones (clientes) o a sus propios/relacionados(as) departamentos/ entidades/sitios, a los cuales asignará /48s. 
- Anunciar en el sistema de rutas inter-dominio de Internet el bloque asignado, con la mínima desagregación que le sea posible a quien está publicando los bloques IP, en un plazo no mayor a 12 meses. 
- Ofrecer servicios en IPv6 a clientes o entidades propias/relacionadas (incluyendo departamentos y/o sitios) localizados físicamente en la región de LACNIC en un plazo no mayor a 24 meses.

#### 4.4.1.3. Tamaño de distribución inicial 

Las organizaciones podrían calificar para una distribución inicial mayor a /32 entregando documentación que justifique el pedido. 

En este caso, la distribución inicial, estará basada en el espacio necesario para atender a los clientes, número de usuarios, extensión de la infraestructura de la organización, estructura jerárquica y/o geográfica de la organización, segmentación de la infraestructura por razones de seguridad y la longevidad prevista para dicha distribución inicial. 

El prefijo asignado al ISP debe estar dentro de las "fronteras" binarias de la dirección IPv6 para poder cumplir con las consideraciones mencionadas anteriormente.

#### 4.4.1.4. Rectificación del tamaño de distribución inicial 

Si una organización, durante el despliegue de IPv6, aprecia que hay discrepancias en la actualidad respecto de cuando realizó la petición de distribución inicial, referidas a las necesidades del tamaño de la misma, podrá justificar un nuevo plan de direccionamiento a LACNIC, sin necesidad de esperar a cumplir los requisitos de la asignación subsiguiente, y por tanto no tendrá que demostrar umbrales de utilización, sino el deseo de aplicar un plan de direccionamiento diferente y más apropiado para la realidad del despliegue a realizar. 

El nuevo tamaño se ajustará al nuevo plan de direccionamiento según lo indicado en el punto 4.4.1.3., y por tanto calificará para la ampliación del prefijo actual en el número de bits que sea preciso. 

Si no fuera posible entregar esa longitud de prefijo, porque los adyacentes ya están siendo utilizados por otras organizaciones, o bien al hacer esa distribución no quedara espacio suficiente para sucesivas distribuciones, LACNIC deberá informar al solicitante y esté podrá optar por:

a) Recibir un nuevo prefijo con el nuevo tamaño solicitado y en un plazo de 6 meses renumerar su red y devolver a LACNIC la distribución inicial "original". o 

b) Recibir un prefijo complementario para completar dicho plan de direccionamiento, y por tanto anunciar ambos, el prefijo inicial "original" y el nuevo prefijo resultante de la nueva distribución. A todos los efectos, para subsiguientes distribuciones, se considerará el conjunto de ambas distribuciones, como si fuera una sola distribución. 

Este procedimiento sólo podrá ser utilizado una única vez por cada organización, así que es preciso, que, en ésta “segunda oportunidad”, se estudie con mucho detenimiento el plan de direccionamiento definitivo para la red a medio/largo plazo.


### 4.4.2. Distribución subsiguiente 

Las organizaciones que ya tengan una distribución IPv6 pueden recibir distribuciones subsiguientes de acuerdo a las siguientes políticas. 

#### 4.4.2.1. Criterio de distribución subsiguiente 

La distribución subsiguiente será provista cuando una organización (ISP/LIR) satisfaga el umbral de evaluación de utilización histórica de direcciones en términos del número de usuarios en unidades de asignaciones de /48. El HD Ratio [RFC 3194] es usado para determinar los umbrales de utilización que justifican la distribución de direcciones adicionales como se describe debajo. 

#### 4.4.2.2. HD Ratio aplicado 

El valor HD Ratio de 0.94 es adoptado como una aceptable utilización de direcciones para justificar la distribución de espacio de dirección adicional. En el Apéndice 2 se provee una tabla que muestra el número de asignaciones que son necesarias para lograr un valor aceptable de utilización dado el tamaño del bloque de direcciones. 

#### 4.4.2.3. Tamaño de la distribución subsiguiente 

Cuando una organización ha logrado una aceptable utilización de su espacio de direcciones distribuido, está inmediatamente calificada para obtener una distribución adicional que resulte en una duplicación de su espacio de direcciones distribuido. Cuando sea posible, la distribución será realizada de bloques de direcciones adyacentes, es decir que su distribución existente es extendida un bit hacia la izquierda. 

Si una organización necesita más espacio de direcciones, debe proveer documentación justificando sus nuevos requerimientos para atender a los clientes, número de usuarios, extensión de la infraestructura de la organización, estructura jerárquica y/o geográfica de la organización, segmentación de la infraestructura por razones de seguridad y la longevidad prevista para dicha distribución subsiguiente.

#### 4.4.2.4. Distribución de LIR a ISP 

No hay una política específica para la distribución de espacio de direcciones de una organización (LIR) a los ISPs subordinados. Cada LIR podría desarrollar su propia política para ISPs subordinados para alentar una utilización óptima del bloque de direcciones total distribuido al LIR. Sin embargo, todas las asignaciones de /48 a organizaciones Usuarios Finales deben ser registradas por el LIR o por sus ISPs subordinados de modo que el RIR/NIR pueda evaluar apropiadamente el HD Ratio cuando sea necesaria una distribución subsiguiente.

### 4.4.3. Asignaciones por parte de los ISPs 

Los LIRs deben realizar asignaciones IPv6 de acuerdo con las siguientes provisiones. 


#### 4.4.3.1. Asignación del espacio de direcciones 

Las asignaciones deben ser realizadas de acuerdo con la necesidad presentada por el usuario del ISP y de acuerdo a las recomendaciones existentes [RIPE-690, https:// www.ripe.net/publications/docs/ripe-690], de las cuales destacan las siguientes: 

- Se debe asignar, al usuario o sitio final, un prefijo que sea múltiplo de "n" x /64, suficiente para atender su necesidad actual y planeada, y teniendo en cuenta protocolos existentes y posibilidades de futuro, evitando así procesos de renumeración. 
- La selección exacta del tamaño del prefijo a asignar es una decisión operacional del LIR/ISP, aunque se recomienda una infraestructura más simple y funcional con /48 para todos los extremos de la red. 
- Se recomienda el uso de prefijos persistentes para evitar efectos indeseados. 
- Se recomienda el uso de /64 para los punto-a-punto, con direccionamiento GUA. 

A los RIRs/NIRs no les concierne el tamaño de direcciones que los LIRs/ISPs realmente asignan. Por lo tanto, los RIRs/NIRs no pedirán información detallada sobre redes de usuarios IPv6 como lo hicieron en IPv4, excepto para los casos que se describen en la Sección 4.4.2 y para los propósitos de medir la utilización como se define en este capítulo. 

#### 4.4.3.2. Asignación a la infraestructura del operador 

Una organización (ISP/LIR) puede asignar un /48 por PoP como un servicio de infraestructura de un operador de servicio IPv6. Cada asignación a un PoP es considerada como una asignación sin tener en cuenta el número de usuarios que usen el PoP. Puede obtenerse una asignación separada para operaciones propias del operador. 

### 4.4.4. Asignaciones directas a Usuarios Finales 

LACNIC realizará asignaciones de direcciones IPv6 portables (independientes del proveedor) directas a usuarios finales según las dos políticas detalladas en 4.4.4.1 y 4.4.4.2, dependiendo si la organización cuenta o no con asignaciones de direcciones IPv4 portables previamente realizadas por LACNIC

#### 4.4.4.1. Asignaciones directas de direcciones IPv6 portables a Usuarios Finales con asignaciones IPv4 portables previas realizadas por LACNIC.

LACNIC asignará bloques de direcciones IPv6 portables directamente a Usuarios Finales si cuentan con asignaciones de direcciones IPv4 portables previamente realizadas por LACNIC. 

En caso de anunciar el bloque designado en el sistema de rutas inter-dominio de Internet, la organización receptora deberá anunciar el bloque designado con la mínima desagregación posible para quien esté publicando los bloques IP. 
Las asignaciones se realizarán en bloques siempre mayores o iguales a un /48. Sucesivas asignaciones tendrán que ser documentadas y justificadas. Además, siempre que sea posible, se realizarán de un bloque de direcciones adyacente (es decir, extendiendo la asignación existente "n" bits a la izquierda).

#### 4.4.4.2. Asignaciones directas de direcciones IPv6 portables a Usuarios Finales sin asignaciones IPv4 portables previas realizadas por LACNIC. 

LACNIC asignará bloques de direcciones IPv6 portables directamente a Usuarios Finales, los cuales deberán cumplir con los siguientes requisitos: 

a. No ser un LIR o ISP. 
b. En caso de anunciar el bloque designado en el sistema de rutas inter-dominio de Internet, la organización receptora deberá anunciar el bloque designado con la mínima desagregación posible para quien esté publicando los bloques IP. 
c. Proveer información detallada mostrando como el bloque solicitado será utilizado dentro de tres, seis y doce meses. 
d. Entregar planes de direccionamiento por al menos un año. 

Las asignaciones se realizarán en bloques siempre mayores o iguales a un /48. 

Sucesivas asignaciones tendrán que ser documentadas y justificadas. Además, siempre que sea posible, se realizarán de un bloque de direcciones adyacente (es decir, extendiendo la asignación existente "n" bits a la izquierda).

#### 4.4.4.3. Rectificación del tamaño de la asignación inicial 

Una organización que sea Usuario Final podrá justificar un nuevo plan de direccionamiento ante LACNIC una única vez en caso de que el plan presentado inicialmente y que justificó la primera asignación no pueda atender sus necesidades actuales. 

El nuevo prefijo se ajustará al nuevo plan y deberá cumplir con las secciones 4.4.4.1 o 4.4.4.2. 

En caso de que no fuera posible entregar ese tamaño de prefijo, ya sea porque los adyacentes ya están siendo utilizados por otras organizaciones o porque al hacer esa asignación no queda espacio suficiente para otras asignaciones sucesivas, LACNIC deberá informar al solicitante, quien deberá optar por: 
- recibir un nuevo bloque con el prefijo solicitado y justificado y que contemple la totalidad de la necesidad presentada, con el compromiso de renumerar su red y devolver a LACNIC el bloque original en un plazo de 6 meses; 
- recibir un nuevo bloque que, sumado al bloque ya asignado, contemple la necesidad presentada y justificada en el nuevo plan y mantener los dos bloques. 

Cada organización podrá utilizar este procedimiento una única vez.

### 4.4.5. Microasignación en IPv6 

LACNIC podrá realizar microasignaciones en casos de proyectos e infraestructuras de redes claves o críticas para el funcionamiento, y desarrollo de IPv6 en la región como son IXP (Internet Exchange Point), NAP (Network Access Point), RIR, proveedores de DNS ccTLD, entre otros. Dichas asignaciones se realizarán en prefijos mayores o igual a un /32 pero siempre menores o iguales a un /48. 

En el caso de los IXP o NAP para poder solicitar este tipo de asignaciones las organizaciones deberán cumplir los siguientes requisitos: 1. Documentar adecuadamente los siguientes aspectos: 

1.1. Demostrar a través de sus estatutos su calidad de IXP o NAP. Deberá poseer al menos tres miembros y una política abierta para la asociación de nuevos miembros. 
1.2. Enviar un diagrama de la estructura de red de la organización. 
1.3. Documentar el plan de numeración a instrumentar. 

2. Proveer un plan de utilización para los próximos tres y seis meses. 

En el resto de las solicitudes se estudiarán basados en el análisis de documentación que justifique los aspectos críticos y/o claves del proyecto. 

Todas las microasignaciones se asignarán de bloques de direcciones específicamente reservados para este tipo de asignaciones. LACNIC hará pública la lista de dichos bloques y las microasignaciones realizadas. 

### 4.4.6. Registro de asignaciones 

Todas las asignaciones de bloques IPv6 de prefijos /48 o menores (bloques mayores) realizadas por los ISPs a los clientes conectados a su red y los usuarios de los servicios prestados deben registrarse en la base de datos WHOIS de LACNIC en un plazo mínimo de 7 días a partir de la asignación. 

La información disponible en la base de datos WHOIS también será usada por LACNIC cuando analice las solicitudes de bloques IPv4 adicionales realizadas por el ISP. 

La información disponible en la base de datos WHOIS será utilizada por LACNIC para calcular el HD Ratio cuando analice las solicitudes de bloques IPv6 adicionales realizadas por el ISP. 

El Registro de asignaciones también es necesario por los siguientes motivos: 

- Para asegurarse que el IR finalizó o está finalizando la distribución de espacio de direcciones de modo que se justifique la distribución de un nuevo espacio adicional. 
- Para proporcionar información a la comunidad Internet sobre cuál organización está usando el espacio de direcciones IPv6 incluyendo a la persona de contacto en caso de problemas de tipo operativo, de seguridad, etc. Para el estudio de distribuciones de direcciones IPv6 en la región.

#### 4.4.6.1. Información Necesaria 

Las asignaciones registradas en la base de datos WHOIS de LACNIC deben incluir el nombre de la organización, dirección postal, contactos administrativos, técnicos y de abuso con números de teléfono e correos electrónicos actualizados.

##### 4.4.6.1.1. Clientes residenciales 

Los ISPs que ofrezcan servicios a clientes residenciales pueden registrar en la base de datos WHOIS de LACNIC bloques de direcciones en uso por los equipos o áreas de atención al cliente, por servicio. 

La información que se registre debe indicar el área de servicio, dirección postal principal del ISP, contactos administrativos, técnicos y de abuso del ISP con números de teléfono y correos electrónicos actualizados. 

Las asignaciones deben realizarse por bloques de direcciones que totalizan la cantidad de clientes atendidos en el área o por equipo.

##### 4.4.6.1.2. Privacidad de Clientes residenciales 

Los clientes residenciales que reciban asignación de bloques IPv6 de prefijo /48 o menores (bloques mayores) no están obligados a tener sus datos registrados en la base de datos WHOIS de LACNIC. 

El ISP cuyo cliente residencial reciba asignación IPv6 de prefijo /48 o menor (bloque mayor) puede optar por registrar la asignación en la base de datos WHOIS de LACNIC colocando sus propios datos o código que le sirva de referencia interna. Los datos de contactos administrativos, técnicos y de abuso deben ser los del ISP.

### 4.4.7. Resolución inversa 

Cuando un RIR/NIR asigna espacio de direcciones IPv6 a una organización, también está delegando la responsabilidad de manejar la zona de consulta reversa que corresponde al espacio de direcciones IPv6 asignado. Cada organización debe manejar debidamente su zona de consulta reversa. Cuando una organización hace una asignación de direcciones, debe delegar a la organización asignada, bajo pedido, la responsabilidad de manejar la zona de consulta reversa que corresponde a las direcciones asignadas.

### 4.4.8. Poseedores de IPv6 ya existentes 

Las organizaciones que hayan recibido distribuciones de IPv6 /35 bajo la política previa de IPv6 [RIRv6 Policies] están inmediatamente autorizadas a expandir su distribución a un prefijo de direcciones /32 sin necesidad de justificación, siempre y cuando satisfagan los criterios de la Sección 4.4.1.1. El prefijo de direcciones /32 contendrá el prefijo mayor ya distribuido (uno o múltiples prefijos /35 en muchos casos) que ya ha sido reservado por el RIR para una subsecuente distribución a la organización. Las solicitudes de espacio adicional más allá del mínimo tamaño /32 serán evaluadas como se discutió en otra parte del documento. 

## 4.5. IPv6 Fusiones, adquisiciones, reorganizaciones y reubicaciones

Se recuerda que las políticas de LACNIC no reconocen la venta o transferencia no autorizada de los recursos asignados o distribuidos y considerará tales transferencias inválidas. 

Sin embargo, LACNIC procesará y registrará la transferencia de recursos IPv6 como resultado de fusiones, adquisiciones, reorganizaciones o reubicaciones, ya sean parciales o completas, tanto tanto si se trata de recursos de ISPs o usuarios finales. 

Para tramitar dicho cambio y proceder al registro, se deberá proporcionar documentación legal que lo respalde a criterio de LACNIC, por ejemplo: 

- Una copia del documento legal que respalda las transferencias de activos. 
- Un inventario detallado de todos los activos utilizados por el solicitante con el cual mantendrá en uso el espacio el recurso. 
- Una lista de los clientes de la parte solicitante que usa los recursos.

Se deberá justificar también que sigue manteniéndose la necesidad del conjunto de los recursos, obligándose si fuera el caso, al retorno de los excedentes de los mismos o alternativamente a su transferencia a terceras partes, atendiendo a lo que corresponda según las políticas vigentes (4.4.1., 4.4.2., 4.4.3. y 4.4.4.). En el caso de un retorno, LACNIC determinará las condiciones y plazo.

# 5. DELEGACIÓN DE RESOLUCIÓN INVERSA

## 5.1. Introducción. 

En la mayor parte de las conexiones hechas a través de Internet se utiliza el nombre de las máquinas en vez de sus direcciones IP. Por motivos obvios los nombres son más fáciles de memorizar que los números. Sin embargo, las conexiones vía Internet entre las computadoras conectadas a esta red serán realizadas utilizando las direcciones IP. Por lo tanto, antes de iniciarse la conexión, se hace una traducción del nombre de la máquina a su dirección IP. Este proceso se llama Resolución DNS directa, o sea, conversión del nombre en dirección IP. 

Muchas veces es necesario también hacer la operación inversa, de donde surge el nombre de Resolución Inversa. En esta conversión, a partir de la dirección IP de un dispositivo, se intenta llegar al nombre asociado a éste. 

Para que el proceso de resolución inversa sea posible es necesario que se utilice un dominio ficticio "in-addr.arpa", una abreviación para “Address and Routing Parameter Area”. 

La delegación DNS de este seudo−dominio es responsabilidad de los Registros de Internet, ya que son ellos los responsables por las distribuciones de direcciones IP. 

## 5.2. Registro de servidores DNS 

Todo el espacio de direcciones IP distribuido debe tener un servidor DNS asociado que será responsable por la resolución inversa. En el caso de la región de cobertura de LACNIC [anexo 1], esos servidores deben ser registrados en LACNIC, quien a su vez es el responsable de la resolución inversa de los bloques administrados por esta organización. 

LACNIC podrá utilizar información producto de la resolución inversa como indicador de la utilización del bloque de direcciones IP distribuido. 

El registro de los servidores DNS del espacio de direcciones IP administrado por LACNIC, será hecho de forma diferente dependiendo del tamaño del espacio distribuido. Los prefijos menores o iguales a /16 distribuidos por LACNIC, deberán tener registrados en LACNIC los servidores DNS responsables para la resolución inversa. La información ingresada será relacionada a prefijos /16. Las distribuciones subsiguientes de segmentos de prefijos mayores hechas dentro de estos bloques, deberán tener los servidores DNS registrados en las organizaciones que recibieron los prefijo menores o iguales a /16 directamente desde LACNIC. 

Los prefijos mayores que /16, distribuidos por LACNIC, deberán tener registrados en LACNIC los servidores DNS responsables para la resolución inversa para todos los prefijos /24 que componen el espacio total de direcciones IP distribuido por LACNIC. De esta forma, las distribuciones subsiguientes de prefijos hasta /24 hechas dentro de ese bloque deberán tener los servidores DNS registrados en LACNIC. 

Por ejemplo: 

1. El ISP−A recibe de LACNIC un prefijo /15 (200.0.0.0/15). Él deberá informar a LACNIC cuáles serán los servidores DNS responsables para la resolución inversa de cada uno de los prefijos /16 que componen el bloque recibido, o sea, los bloques 200.0.0.0/16 y 200.1.0.0/16. Los servidores DNS de distribuciones subsiguientes de prefijos mayores hechas dentro de este bloque, deberán ser registrados en los servidores DNS del ISP−A que a su vez están registrados en los servidores DNS de LACNIC como los responsables para la resolución inversa de los bloques 200.0.0.0/16 y 200.1.0.0/16. 

2. El ISP−B recibe de LACNIC un prefijo /20 (200.2.0.0/20). Él deberá informar a LACNIC cuáles serán los servidores DNS responsables para la resolución inversa de los bloques del 200.2.0.0 hasta el 200.2.15.0. Cuando el ISP−B haga una subdistribución de un bloque con prefijo mayor que /21 y menor o igual a /24, deberá registrar en los servidores de LACNIC cuáles son los nuevos servidores de DNS responsables para la resolución inversa de ese bloque distribuido. De esta forma, en el sistema de administración de direcciones IP de LACNIC no será posible registrar servidores DNS para distribuciones subsiguientes hechas en bloques con prefijo menor o igual a /16 que hayan sido distribuidos directamente por LACNIC. Corresponderá a la organización que recibió la distribución hacer el registro de los servidores DNS responsables para la resolución inversa de esas distribuciones hechas dentro de ese bloque. 

Esto será también reflejado en la base de datos del servidor WHOIS. Es decir, para distribuciones subsiguientes dentro de los bloques de prefijo menor o igual a /16 distribuidos directamente por LACNIC, no será visible vía WHOIS cuales son los servidores DNS responsables para la resolución inversa de esas distribuciones. Esto ocurre porque el registro de estos servidores no es hecho en LACNIC. Se recomienda que en caso en que sea necesario identificar los servidores DNS de distribuciones subsiguientes hechas en estos bloques se utilicen herramientas de consulta DNS. 

Esta condición no existe para distribuciones de prefijos mayores que /16 hechas por LACNIC. En este caso las distribuciones subsiguientes de prefijos hasta /24 hechas dentro de los bloques distribuidos por LACNIC y que tengan prefijos mayores que /16 podrán tener un servidor DNS delegado vía el sistema de administración de direcciones IP de LACNIC. 

El sistema de administración de direcciones IP de LACNIC no acepta la delegación de servidores DNS para bloques con prefijo mayores que /24. Para estos casos se recomienda la adopción de BCP 20. 

Resumiendo: 

Prefijo del bloque distribuido por LACNIC Servidor DNS para distribuciones subsiguientes hechas por LACNIC debe registrarse en: 

- /16 o menor: ISP que recibió el bloque. 
- /17 o mayor: LACNIC 

# 6. POLÍTICA DE LAME DELEGATION 

Se considera que existe un problema de Lame Delegation en un servidor DNS, cuando este servidor aparece registrado en las zonas para la resolución inversa de los bloques de direcciones IP y al momento de solicitar alguna resolución este no responde autoritativamente. 

La respuesta no autoritativa de un servidor DNS se interpreta como un error en la configuración del servidor y dentro de los estándares de LACNIC se considerará a este servidor DNS con problemas de Lame Delegation. 

El proceso de corrección de las delegaciones lame dentro del espacio de direcciones IP administradas por LACNIC seguirá las siguientes fases: 

1. Detección de delegaciones lame. 
2. Monitoreo de los servidores de DNS con problemas de delegaciones lame 3-Notificación a los responsables. 
4. Desactivación de servidores DNS. 
5. Activación de nuevos servidores de DNS

## 6.1.Detección de delegaciones lame 

LACNIC realizará periódicamente revisiones a las zonas in-addr.arpa e ip6.arpa donde existan servidores DNS delegados para la resolución inversa en la región de cobertura LACNIC. Sólo segmentos delegados directamente por LACNIC serán consideradas en los procesos de monitoreo y desactivación de servidores DNS. 

Se considerará que un servidor DNS registrado en el sistema de LACNIC cuenta con problemas de delegación lame si a una consulta del registro SOA del servidor DNS no se obtiene una respuesta autoritativa de este registro.

La verificación será realizada por cada zona in-addr.arpa e ip6.arpa delegada a cada servidor DNS. 

De no tener una respuesta autoritativa el servidor DNS será catalogado con problemas de delegación lame para la zona in-addr.arpa e ip6.arpa que se verificó, por lo que entrará en un proceso de monitoreo.

## 6.2. Monitoreo de los servidores de DNS con problemas de delegación lame 

Antes de establecer que un servidor DNS tiene problemas de delegación lame permanente para una zona in-addr.arpa o ip6.arpa, LACNIC verificará por un periodo de 7 días el servidor DNS. Si el problema persiste después de este periodo LACNIC hará los esfuerzos para notificar a los contactos responsables del bloque de direcciones IP. 

Si un servidor DNS que fue detectado originalmente con problemas de delegación lame responde correctamente para la zona in-addr.arpa o ip6.arpa antes de la fase de desactivación de servidores DNS, saldrá de la lista de monitoreo, correspondiente a estas zonas.

## 6.3. Notificación a los Responsables 

En primera instancia se notificará al contacto administrativo del bloque en cuestión, junto con el contacto técnico si es que cuenta con esta información. Las notificaciones serán quincenales por un periodo de 60 días. LACNIC se reservará el derecho de investigar otro tipo de contactos pasado los primeros 30 días sin respuesta de los contactos administrativos y/o técnico.

## 6.4. Desactivación de Servidores DNS 

Una vez pasado el periodo de notificación definido se procederá a la eliminación de estos servidores DNS dentro de las zonas de LACNIC. 

Sólo en las zonas in-addr.arpa o ip6.arpa donde el servidor DNS presentó problemas de delegación lame será dado de baja el servidor. Si existiera otro servidor DNS que dé servicio a estas zonas no será afectado. 

Se agregará un comentario al registro del bloque en la BD WHOIS que se especifique que el servidor DNS registrado para la resolución inversa de las zonas in-addr.arpa o ip6.arpa correspondiente al segmento fue desactivado por problemas de delegación lame. 

Sólo segmentos delegados directamente por LACNIC serán consideradas en los procesos de monitoreo y desactivación de servidores DNS.

## 6.5. Activación de nuevos servidores de DNS 

La activación de nuevos servidores de DNS seguirá los procedimientos habituales actuales ya incluidos en la política de LACNIC. Sólo el contacto administrativo o técnico del bloque podrá dar de alta nuevos servidores DNS a través del sistema de registro de LACNIC. Todo nuevo servidor DNS que se registre en LACNIC deberá responder autoritativamente al bloque al momento de su alta de otra manera se rechazará el registro del servidor.

# 7. REVOCACIÓN Y DEVOLUCIÓN DE RECURSOS 

Las distribuciones y asignaciones de recursos son válidas mientras los objetivos de exclusividad, conservación, ruteabilidad, información y en general, el resto de las políticas, continúen cumpliéndose. 

LACNIC podrá, por lo tanto, invalidar cualquier distribución o asignación si se determina que los requerimientos ya no existen o se dejan de cumplir los criterios del manual de políticas. 

Podrá ser considerado como causa para la revocación de recursos: 

- Recursos no utilizados o anunciados (cuando sea obligatorio). 
- No mantener el registro de la resolución inversa de las direcciones. 
- No mantener actualizada la información de las distribuciones y asignaciones en la base de datos Whois de LACNIC o NIRs, según corresponda. o Transferencias no autorizadas. 
- De forma genérica, incumplimientos continuados y/o reiterados de políticas. 
- No cumplir con las obligaciones contractuales con LACNIC o sus NIRs, incluyendo impagos o fraude documental. 
- Organizaciones que desaparecieron, o no responden. 

Cuando el incumplimiento ha sido causado por un tercero, sin conocimiento de la organización que recibe los recursos, y sea evidente que no hay connivencia ni negligencia por parte de dicha organización, no se iniciará el proceso de revocación.

## 7.1. Proceso de Revocación de recursos 

Para la eficiente utilización de los recursos de la región, LACNIC verificará con las organizaciones que reciben recursos, el correcto uso de los mismos, de forma automatizada periódicamente cuando sea posible y más exhaustivamente siempre que se cuente con evidencias que permitan inferir que no están siendo correctamente utilizados. 

Una vez se detectan evidencias y son confirmadas, el proceso de recuperación de recursos tiene los siguientes pasos: 

a) LACNIC tratará de contactar a la organización y regularizar la situación. 
b) En caso de que la situación no pueda ser regularizada, LACNIC listará públicamente durante un período máximo de tres meses los recursos a recuperar. 

Durante este periodo la organización aún puede regularizar la situación con LACNIC.

c) En el resto de los casos, transcurridos los primeros dos meses desde la publicación de los recursos, LACNIC procederá a eliminar los registros NS que apuntan a los servidores autoritativos de los recursos involucrados. Esta información puede recuperarse una vez que la organización restablece contacto con LACNIC o el NIR correspondiente. 

d) Habiendo transcurrido tres meses de publicación sin que la organización haya regularizado su situación, el recurso será recuperado, por lo que se eliminarán los registros de titularidad sobre estos recursos en la base de datos de LACNIC. 

e) Se aplicarán el resto de estipulaciones indicadas en el Acuerdo de Servicios de Registro y Estatutos.

## 7.2. Excepcionalidad 

Para casos en los que la revocación de recursos involucre infraestructuras esenciales estratégicas para el funcionamiento de Internet en la región, o para situaciones de excepción como desastres naturales o de inestabilidad política, el período de revocación de recursos puede ser extendido por parte del Directorio de LACNIC, previa evaluación del staff a partir de la detección de una situación extraordinaria que así lo requiera.

## 7.3. Devolución de recursos 

Los receptores de recursos pueden devolverlos a LACNIC, siempre que lo deseen, tanto total como parcialmente. 

En el caso de devolución total, aplicará lo indicado en el Acuerdo de Servicios de Registro y Estatutos.

## 7.4. Publicación de los recursos 

LACNIC listará públicamente los recursos que han sido recuperados o devueltos para que se puedan modificar los filtros de ruteo.

## 7.5. Uso de recursos recuperados o devueltos 

Los recursos IPv4, serán incorporados al “final” del pool en vigor en el momento de su recuperación o devolución, para su uso en el orden en que se hayan incorporado al mismo. 

Los recursos IPv6 y ASNs, serán incorporados a sus respectivos pools en vigor, al transcurrir 2 años de su recuperación o devolución. 

Sin embargo, LACNIC podrá utilizar estos recursos de forma diferente, en aplicación de mejores prácticas, para un cumplimiento optimizado de lo indicado en la sección 2 del RFC7020. Por ejemplo, si se recuperan o devuelven ASN de 16 bits.


# 8. SOLICITUD DE BULK WHOIS DEL REGISTRO DE DIRECCIONES DE INTERNET PARA AMERICA LATINA Y CARIBE 

LACNIC proveerá de una copia bulk de la información WHOIS únicamente a aquellas organizaciones que destinen la información a fines de investigación técnicas y/u operacionales de Internet. Su solicitud de la información y la resolución de LACNIC denegando o aprobando la misma podrá ser publicada. 

Para solicitar ésta información Ud. deberá completar el formulario adjuntado a continuación y enviarlo por correo a la siguiente Dirección:

LACNIC Atención: Solicitud de Bulk WHOIS 
Rambla República de México 6125, 
Montevideo Uruguay, CP 11400 

No se aceptaran formularios enviados por fax, ni solicitudes en las que no se proporcione la información que se detalla a continuación: 

Organización solicitante:
Domicilio de la organización:
Persona de contacto: 
  Nombre:
  Teléfono:
  Fax:
  Email:
Razones de la solicitud y destino de la información:

## 8.1. Uso aceptable del Bulk Whois de LACNIC 

El bulk WHOIS de LACNIC se deberá destinar únicamente a fines de investigación técnicas y/u operacionales de Internet, tales como el diseño o elaboración de software de seguridad, proyectos de mejora de rendimientos en Internet y optimización de tráfico en la red. No podrá ser usada con fines de publicidad, mercadeo directo, investigaciones de mercado, y otros propósitos similares. El uso de la información del WHOIS de LACNIC con esos fines se encuentra explícitamente prohibido, y otorgará derecho a suspender al acceso del solicitante a la información e iniciar las acciones legales pertinentes. LACNIC solicita que se le notifique de cualquier actividad o sospecha de uso indebido del WHOIS. 

La redistribución o retransmisión de la información por cualquier medio se encuentra expresamente prohibida. En el caso de que se tenga la intención de publicar todo o parte de la información proporcionada, se deberá requerir la autorización previa y por escrito de LACNIC. 

La presente solicitud se regirá y será interpretada de acuerdo a las leyes de la República Oriental del Uruguay y en caso de producirse diferencias, desavenencias o controversias entre las partes derivadas de este contrato, las mismas procurarán solucionarlas mediante la conciliación del Centro de Conciliación y Arbitraje de la Bolsa de Comercio del Uruguay, realizada de acuerdo con las disposiciones del Reglamento de Conciliación de dicho Centro. En caso de que no sea posible conciliar las mismas, dichas diferencias, desavenencias, o controversias serán resueltas definitivamente mediante arbitraje, observándose para la designación de los árbitros, que serán tres, como para el procedimiento arbitral, las disposiciones contenidas en el Reglamento de Arbitraje del Centro. 

En señal de conformidad con los términos y condiciones de la presente solicitud, firmo la presente en la fecha que se detalla a continuación: 

Organización: 
Firma: 
Aclaración: 
Cargo en la Organización: 
Fecha: ___ | ___ | _____ (dd | mm | aaaa)

# 9. POLÍTICAS GLOBALES 

## 9.1.POLÍTICAS DE DISTRIBUCIÓN DE ESPACIO DE DIRECCIONES IPv4 POR PARTE DE LA IANA A LOS RIRs 

Este capítulo describe las políticas que rigen la distribución de espacio de direcciones IPv4 por parte de la IANA a los Registros Regionales de Internet (RIRs). Este capítulo no estipula requisitos de eficiencia respecto de la provisión de servicios por parte de IANA a un RIR de acuerdo con estas políticas. Estos requisitos deben ser especificados por acuerdos entre los RIRs e ICANN. 

### 9.1.1. Principios de distribución 

- La IANA distribuirá a los RIRs espacio de direcciones IPv4 en bloques con prefijo / 8.
- La IANA distribuirá a los RIRs espacio de direcciones IPv4 suficiente para soportar sus necesidades de registro durante un período de al menos 18 meses.
- La IANA permitirá que los RIRs apliquen sus propias respectivas estrategias de distribución y reserva a fin de asegurar la eficiencia y eficacia de su labor.

### 9.1.2. Distribuciones iniciales 

Todo nuevo RIR, en el momento de su reconocimiento, recibirá un bloque con prefijo /8 distribuido por la IANA. Esta asignación se hará independientemente de las cifras de utilización proyectadas para el nuevo RIR y será independiente del espacio de direcciones IPv4 que los RIRs ya existentes pudieran haber transferido al nuevo RIR como parte del proceso formal de transición.

### 9.1.3. Distribuciones adicionales 

Un RIR califica para recibir de IANA espacio de direcciones IPv4 adicional cuando satisface alguna de las condiciones siguientes: 

- El ESPACIO DISPONIBLE de direcciones IPv4 del RIR es menor que el 50% de un bloque con prefijo /8. 
- El ESPACIO DISPONIBLE de direcciones IPv4 del RIR es menor que el ESPACIO NECESARIO establecido para los 9 meses siguientes. 

En ambos casos la IANA hará una única distribución de un número entero de prefijos /8, suficiente para satisfacer el ESPACIO NECESARIO establecido del RIR durante un período de 18 meses.

# 9.1.3.1. Cálculo del ESPACIO DISPONIBLE 

El ESPACIO DISPONIBLE de direcciones IPv4 de un RIR se calculará de la siguiente manera: 

- ESPACIO DISPONIBLE = DIRECCIONES LIBRES ACTUALES + RESERVAS QUE VENCERÁN EN LOS PRÓXIMOS 3 MESES - ESPACIO FRAGEMENTADO 
- El ESPACIO FRAGMENTADO se calcula como la cantidad total de bloques disponibles menores que el tamaño de la distribución mínima del RIR dentro del actual stock de disponibilidades del RIR.

#### 9.1.3.2. Cálculo del ESPACIO NECESARIO 

Si el Registro Regional de Internet solicitante no establece ninguna situación especial de necesidades para el período en cuestión, el ESPACIO NECESARIO se calculará de la siguiente manera: 

- ESPACIO NECESARIO = PROMEDIO DE DIRECCIONES DISTRIBUIDAS POR MES EN LOS ULTIMOS 6 MESES * DURACIÓN DEL PERÍODO EN MESES 

Si el RIR solicitante prevé que debido a ciertas necesidades especiales el ritmo de distribución en el período en cuestión será diferente al de los pasados 6 meses, el ESPACIO NECESARIO se podrá establecer de la siguiente manera: 

- Calcular el ESPACIO NECESARIO como el total de necesidades para dicho período conforme a su proyección y en base a los hechos especiales que justifican dichas necesidades. 
- Presentar una justificación clara y detallada de la proyección arriba mencionada (punto A). 

Si esta justificación se basa en la tendencia de distribuciones preparada por el Registro Regional de Internet, se deberán adjuntar los datos que expliquen dicha tendencia. 

Si esta justificación se basa en la aplicación de una o más nuevas políticas de distribución del Registro Regional de Internet, se deberá adjuntar el análisis de impacto de la/s nueva/ s política/s. 

Si esta justificación se basa en factores externos tales como nueva infraestructura, nuevos servicios en la región, adelantos tecnológicos o aspectos legales, se deberá adjuntar el análisis correspondiente junto con referencias a fuentes de información que permitan corroborar los datos. 

Si la IANA no tuviera elementos que cuestionen claramente la proyección preparada por el Registro Regional de Internet, la proyección de necesidades especiales para los siguientes 18 meses, indicada en el punto A anterior, se deberá considerar válida.

### 9.1.4. Anuncio de las distribuciones de la IANA 
Cada vez que distribuya espacio de direcciones a un RIR, la IANA enviará un anuncio detallado al RIR que recibe dicha distribución. La IANA también enviará anuncios a todos los demás RIRs, informando sobre la reciente distribución. Los RIRs coordinarán el anuncio a sus respectivas listas de miembros y a cualquier otra lista que estimen necesario. 

La IANA introducirá las modificaciones necesarias en la página "Espacio de Direcciones IPv4" del sitio web de IANA, y puede enviar anuncios a sus propias listas de anuncio. Los anuncios de la IANA se limitarán a informar los rangos de direcciones, el momento en el cual se realizó la distribución, y el Registro al cual han sido distribuidos.

## 9.2. POLÍTICA GLOBAL DE DISTRIBUCIÓN DEL ESPACIO IPV4 REMANENTE 

Esta política describe el proceso para la distribución del espacio IPv4 remanente por parte de IANA a los RIR. Cuando se llegue a un volumen mínimo de espacio disponible, IANA deberá distribuir un /8 a cada RIR, reemplazando la actual política de distribución de espacio IPv4. 

Para satisfacer los requisitos de esta política, en el momento de su adopción IANA reservará un /8 para cada RIR. Las unidades de distribución reservadas dejarán de formar parte del espacio de direcciones disponible en IANA. IANA también deberá reservar un /8 para cualquier nuevo RIR en el momento de su reconocimiento. 

El proceso para la distribución del espacio IPv4 remanente se divide en dos fases consecutivas: 

### 9.2.1. Fase de aplicación de la política existente 

Durante esta fase IANA continuará distribuyendo direcciones IPv4 a los RIR utilizando la política de distribución existente. Esta fase continuará hasta que una solicitud de espacio de direcciones IPv4 presentada a IANA por alguno de los RIR no pueda ser satisfecha con el espacio IPv4 remanente en IANA o bien pueda ser satisfecha pero dejando a IANA sin espacio de direcciones. 

Esta será la última solicitud de espacio de direcciones IPv4 que IANA aceptará de parte de cualquier RIR. En este momento se activará la siguiente fase del proceso. 

### 9.2.2. Fase de agotamiento 

IANA automáticamente distribuirá a cada RIR las unidades de distribución IPv4 reservadas (un /8 a cada uno de ellos) y responderá a la última solicitud con las restantes unidades de distribución disponibles en IANA (M unidades). 

### 9.2.3. Tamaño de las distribuciones IPv4 finales 

Durante esta fase IANA automáticamente distribuirá a cada RIR un /8 del espacio reservado definido en la presente política. IANA también distribuirá M unidades de distribución al RIR que presentó la última solicitud de direcciones IPv4. 

### 9.2.4. Distribución del espacio de direcciones IPv4 remanente 

Una vez completada la evaluación de la última solicitud de direcciones IPv4, IANA DEBERÁ: 

A. Comunicar inmediatamente a la NRO la activación de la segunda fase de la presente política. 
B. Proceder a distribuir M unidades de distribución al RIR que presentó la última solicitud de espacio de direcciones IPv4. 
C. Proceder a distribuir a cada RIR un /8 del espacio reservado. 

##9.3. POLÍTICA DE DISTRIBUCIÓN DE ESPACIO DE DIRECCIONES IPv6 DEL IANA A LOS REGISTROS REGIONALES DE INTERNET (RIRs) 

Este capítulo describe la política que rige las distribuciones de espacio de direcciones IPv6 del IANA a los Registros Regionales de Internet (RIR). Este capítulo no estipula los requerimientos de desempeño en la provisión de servicios del IANA a un RIR de acuerdo con esta política. Tales requerimientos serán especificados por un acuerdo apropiado entre el ICANN y el NRO. 

### 9.3.1. Principios de distribución 

- La unidad de distribución IPv6, (por consiguiente, la distribución mínima de IPv6) del IANA a un RIR es un /12 
- El IANA distribuirá espacio IPv6 suficiente a los RIRs para soportar sus necesidades de registro por al menos un periodo de 18 meses. 
- El IANA permitirá a los RIRs aplicar sus propias estrategias de distribución y reserva con el fin de asegurar la eficiencia y eficacia de sus trabajos

### 9.3.2. Distribuciones Iniciales 

En el inicio de esta política cada RIR existente con menos de un /12 de espacio de direcciones sin distribuir, recibirá una distribución de IPv6 del IANA. 

Cualquier nuevo RIR, al ser reconocido por ICANN, recibirá una distribución IPv6 del IANA. 

### 9.3.3. Distribuciones Adicionales 

Un RIR es elegible a recibir espacio de direcciones IPv6 adicional del IANA cuando unas de las siguientes condiciones se cumplan. 

- El ESPACIO DISPONIBLE de direcciones IPv6 del RIR es menos del 50% de un /12. 
- El ESPACIO DISPONIBLE de direcciones IPv6 es menos que su ESPACIO NECESARIO establecido por los siguientes 9 meses. 

En cada caso el IANA hará una única distribución de IPv6, suficiente para satisfacer el ESPACIO NECESARIO establecido para el RIR para un periodo de 18 meses. 


#### 9.3.3.1. Cálculo de ESPACIO DISPONIBLE 

El ESPACIO DISPONIBLE de direcciones IPv6 de un RIR será determinado como sigue: 

ESPACIO DISPONIBLE = DIRECCIONES LIBRES + RESERVACIONES HA EXPIRAR DURANTE LOS SIGUIENTES 3 MESES – ESPACIO FRAGMENTADO 

El ESPACIO FRAGMENTADO es determinado como la cantidad total de bloques disponibles más pequeños que el tamaño mínimo de distribución del RIR dentro de su espacio disponible total en existencia del RIR.

#### 9.3.3.2. Cálculo del ESPACIO NECESARIO 

Si el RIR solicitante no establece una necesidad especial para el periodo en cuestión, el ESPACIO NECESARIO será determinado como sigue: 

ESPACIO NECESARIO = PROMEDIO DE DIRECCIONES ASIGNADOS MENSUALMENTE DURANTE LOS ULTIMOS 6 MESES * LONGITUD DEL PERIODO EN MESES 

Si el RIR solicitante anticipa que debido a ciertas necesidades especiales la proporción de la distribución para el periodo en cuestión será diferente de los 6 meses anteriores, puede entonces determinar su ESPACIO NECESARIO como sigue: 

Calcular el ESPACIO NECESARIO como sus necesidades totales para ese periodo de acuerdo a su proyección y basado en hechos especiales que justifiquen esas necesidades. 

Entregar una justificación detallada y clara de la proyección mencionado anteriormente. 

Si la justificación es basada en la tendencia de distribuciones preparado por el RIR, debe incluirse los datos que expliquen dicha tendencia. 

Si la justificación es basada en la aplicación de una o más nuevas políticas de distribución del RIR, debe incluirse un análisis de impacto de tales nuevas políticas. 

Si la justificación es basada en factores externos tales como nueva infraestructura, nuevos servicios dentro la región, avances tecnológicos o aspectos legales, debe incluirse el análisis correspondiente junto con referencias a fuentes de información que permitan verificar los datos.

### 9.3.4. Anuncios de las distribuciones del IANA 

El IANA, el NRO, y los RIRs harán anuncios y actualizarán sus respectivos websites en relación a la distribución hecho por el IANA a un RIR. El ICANN y el NRO establecerán procedimientos administrativos para manejar este proceso.

## 9.4. POLÍTICA GLOBAL DE DISTRIBUCIÓN DE ASNS A LOS REGISTROS REGIONALES DE INTERNET 

Este documento describe la política que rige la distribución de Números de Sistema Autónomo (ASNs) por parte de IANA a los Registros Regionales de Internet (RIRs). 

Este documento no estipula requisitos de performance en la provisión de servicios por parte de IANA a un RIR. Tales requisitos deberán ser especificados mediante un acuerdo apropiado entre el ICANN y la NRO (Number Resource Organization). 

### 9.4.1. Principios de las Distribuciones 

IANA distribuye ASNs a los RIRs en bloques de 1024 ASNs. En este documento, el término “bloque de ASNs” se refiere a un conjunto de 1024 ASNs. Hasta el 31 de diciembre de 2009, las distribuciones de bloques de ASNs de sólo 2 bytes y de sólo 4 bytes se harán en forma separada e independiente. Esto significa que, de acuerdo con esta política, hasta el 31 de diciembre de 2009 los RIRs pueden recibir de IANA dos bloques de ASNs diferentes, uno para ASNs de sólo 2 bytes y otro para ASNs de sólo 4 bytes. Después de esta fecha IANA y los RIRs dejarán de diferenciar entre ASNs de sólo 2 bytes y ASNs de sólo 4 bytes, y distribuirán ASNs de un espacio de distribución no diferenciado de 4 bytes 

### 9.4.2. Distribuciones Iniciales 

A cada nuevo RIR se le distribuirá un nuevo bloque de ASNs.

### 9.4.3. Distribuciones Adicionales 

Un RIR podrá recibir de IANA uno o más bloques de ASNs adicionales si se satisface una de las condiciones siguientes: 

- El RIR ha asignado 80% del bloque de ASNs recibido previamente, o. 
- El número de ASNs libres actualmente en poder del RIR es menor que la necesidad proyectada para 2 meses. La proyección se basa en el número promedio de ASNs asignados por el RIR durante los 6 meses precedentes. 

A un RIR se le distribuirán tantos bloques de ASNs como sea necesario para soportar sus necesidades de registración durante los doce meses siguientes, en base a su tasa de asignación promedio durante los seis meses precedentes, a menos que el RIR específicamente solicite una cantidad de bloques menor que aquella para la cual califica.

### 9.4.4. Anuncio de las Distribuciones por parte de IANA 

El IANA, la NRO y los RIRs deberán anunciar y actualizar sus respectivos sitios web / bases de datos cuando la IANA realice una distribución a un RIR. El ICANN y la NRO deberán establecer procedimientos administrativos para manejar este proceso.

## 9.5. POLÍTICA GLOBAL PARA LA DISTRIBUCIÓN DE ESPACIO DE DIRECCIONES IPV4 POR PARTE DE LA IANA POST AGOTAMIENTO 

Tras la adopción de esta política para direcciones IPv4 por parte del Directorio de ICANN, la IANA establecerá un Pool de Direcciones IPv4 Recuperadas para ser utilizado luego del agotamiento del espacio de direcciones IPv4 de los RIR tal como se define en la Sección 1. El Pool de Direcciones IPv4 Recuperadas inicialmente contendrá cualquier fragmento que pudiera haber quedado en el inventario de la IANA. También contendrá cualquier espacio devuelto a la IANA por cualquier otro medio.

### 9.5.1. Pool de Direcciones IPv4 Recuperadas 

El Pool de Direcciones IPv4 Recuperadas será administrado por la IANA. Éste contendrá: 

a. Cualquier fragmento que pudiera haber quedado en el inventario de la IANA después que los últimos /8 del espacio de direcciones IPv4 sea delegado a los RIR 
- El inventario de la IANA excluye las "direcciones IPv4 para usos especiales" según se define en BCP 153 y cualquier dirección distribuida por la IANA para uso experimental. 

b. Cualquier espacio de direcciones IPv4 devuelto a la IANA por cualquier medio. 

El Pool de Direcciones IPv4 Recuperadas permanecerá inactivo hasta que el primer RIR tenga menos de un total de un /9 en su inventario de espacio de direcciones IPv4. 

Cuando uno de los RIR declare tener menos de un total de un /9 en su inventario, el Pool de Direcciones IPv4 Recuperadas será declarado activo y las direcciones de dicho Pool de Direcciones IPv4 Recuperadas será distribuido de acuerdo con lo especificado en la Sección 9.5.2 a continuación.

### 9.5.2. Distribución por parte de la IANA del espacio de direcciones IPv4 devuelto 

a. La IANA podrá comenzar a realizar distribuciones una vez que el pool se declare activo. 
b. En cada "período de distribución de espacio IPv4" cada RIR recibirá de la IANA una única "unidad de distribución IPv4". 
c. Un "período de distribución de espacio IPv4" se define como un período de seis meses que comienza el 1ro de marzo o el 1ro de setiembre de cada año. 
d. La IANA calculará el tamaño de la "unidad de distribución IPv4" en los siguientes momentos: 
- Cuando el Pool de Direcciones IPv4 Recuperadas se active por primera vez 
- Al comenzar cada período de distribución de espacio IPv4 

En estos momentos, para calcular la "unidad de distribución IPv4" la IANA usará la siguiente fórmula: 

Unidad de distribución IPv4 = 1/5 del Pool de Direcciones IPv4 Recuperadas, redondeado hacia abajo al límite CIDR (potencia de 2) siguiente. 

Ningún RIR podrá obtener más que este cálculo usado para determinar la unidad de distribución IPv4, aun cuando puedan justificar su necesidad. 

El tamaño mínimo de la "unidad de distribución IPv4" será un /24. Si el cálculo usado para determinar la unidad de distribución IPv4 da por resultado un bloque menor a un /24, durante dicho período de distribución de espacio IPv4 la IANA no distribuirá ninguna dirección.

### 9.5.3. Informes 

La IANA podrá publicar anuncios de las transacciones de direcciones IPv4 que se produzcan de acuerdo con esta política. La IANA hará las modificaciones necesarias en la página "Espacio de direcciones Protocolo Internet v4" de su sitio web [2] y podrá realizar anuncios a través de sus propias listas de anuncios. Los anuncios de la IANA se limitarán a indicar los rangos de direcciones distribuidos, el momento de la distribución y cuál Registro recibió la distribución.

# 10. POLÍTICA DE DISTRIBUCIÓN DE RECURSOS DE INTERNET CON FINES DE INVESTIGACIÓN Y EXPERIMENTACIÓN 

LACNIC realizará distribuciones experimentales con el objetivo de fomentar la investigación y desarrollo en la región. Estas distribuciones abarcarán todos los recursos que LACNIC posee (direcciones IPv4, IPv6, ASN). 

LACNIC fomentará el uso de recursos privados (cuando sea posible), tanto para direcciones IPv4 (RFC 1918), como para ASN (64512 -65535). 

Para poder recibir una distribución inicial, el experimento deberá cumplir con una de las siguientes condiciones: 

- Estar basado en un RFC de la IETF con categoría experimental. 
- Ser considerado por parte de LACNIC y especialistas externos en el tema como favorable para el desarrollo de la región y la tecnología en general.

Para poder obtener una distribución experimental, el solicitante deberá: 

- Enviar inicialmente toda la información del experimento que LACNIC y los especialistas externos en el tema considere necesaria de forma de evaluar la solicitud. LACNIC publicará la información referente a la solicitud en una página Web pública (a definir por LACNIC) y anunciará la existencia de la solicitud a través de una lista de correo de suscripción abierta (a definir por LACNIC). LACNIC esperará un plazo de 30 días antes de realizar la distribución para recibir comentarios de la comunidad. 
- Utilizar sólo los recursos distribuidos para los fines detallados en la información remitida a LACNIC. 
- No utilizar la distribución con fines comerciales. 
- Los resultados del experimento deben estar en una página Web públicamente accesible (sin controles de acceso). Existirá un enlace desde la página de LACNIC. 
- Presentar un informe anual a LACNIC sobre el avance del experimento. Los informes podrán ser difundidos por LACNIC en sus foros, listas de correos, website y cualquier otra forma de difusión que entienda pertinente, respetando la fuente del mismo. 
- Ingresar la información de redistribución en la base de datos WHOIS de LACNIC. 
- Mantener al día la resolución inversa de los bloques distribuidos. 
- El no cumplimiento de estas condiciones puede acarrear la revocación de la distribución correspondiente. 

Los bloques mínimos de distribución estarán restringidos por las políticas de microasignaciones (tanto para IPv4 como para IPv6). 

Si bien no existe un tamaño máximo de distribución, LACNIC deberá asignar recursos de forma de asegurar su operación normal. 

En el estudio inicial el staff de LACNIC determinará los recursos a asignar. 

La distribución experimental tendrá una duración de un año renovable sucesivamente por igual período, sin un máximo estipulado. Para la renovación se considerará el informe anual presentado. 

En el momento de la renovación será posible solicitar recursos adicionales. La evaluación se realizará considerando el cumplimiento de los puntos detallados anteriormente, junto con la documentación adicional presentada por el solicitante. 

LACNIC publicará la información referente a la solicitud de recursos adicionales en una página Web pública (a definir por LACNIC) y anunciará la existencia de dicha solicitud a través de una lista de correo de suscripción abierta (a definir por LACNIC). LACNIC esperará un plazo de 15 días antes de realizar la distribución de recursos adicionales para recibir comentarios de la comunidad.

# 11. POLÍTICAS SOBRE EL AGOTAMIENTO DEL ESPACIO DE DIRECCIONES IPV4. 

Las siguientes políticas se relacionan al proceso de agotamiento del espacio de direcciones IPv4. 

## 11.1.Reserva especial de distribuciones/asignaciones IPv4 para nuevos miembros. 

1. LACNIC creará una reserva de direccionamiento IPv4 utilizando el espacio distribuido por la IANA a LACNIC post agotamiento, considerando además del espacio recuperado y devuelto mencionado en la sección 7 del manual de políticas. 
2. No se harán distribuciones o asignaciones de recursos IPv4 a organizaciones que ya tengan recursos IPv4 distribuidos o asignados por LACNIC o por las organizaciones que antecedieron a LACNIC en esta reserva en la actual región de servicio de LACNIC. 
3. Solicitudes de recursos IPv4 que según las políticas vigentes de LACNIC sean clasificadas como infraestructura critica podrán recibir direccionamiento bajo las condiciones de esta política aunque ya cuenten con recurso IPv4 asignado por LACNIC. 
4. LACNIC solo podrá realizar distribuciones o asignaciones de recursos IPv4 mayores o iguales a /24 y menores o iguales a /22 de esta reserva. 
5. LACNIC podrá realizar distribuciones o asignaciones de esta reserva a partir de la aprobación de la primera solicitud de recursos IPv4 que no pueda ser satisfecha utilizando la reserva creada en el punto 11.2. 
6. Las solicitudes de recursos IPv4 de prefijos menores a /22 que se encuentren pendientes por aprobación solo podrán recibir un /22 de esta reserva. 
7. Las organizaciones que reciban recursos IPv4 bajo las condiciones establecidas en la siguiente política no podrán recibir recursos IPv4 adicionales por parte de LACNIC provenientes de esta reserva, exceptuando solicitudes para infraestructura crítica 
8. Un bloque recibido bajo esta política no podrá ser transferido siguiendo el punto 2.3.2.18 del manual de políticas durante un periodo de tres años. Lo mismo aplica para sus subbloques, es decir, bloques que agrupen un subconjunto de las direcciones IPv4 que contiene el bloque. 
9. La presente política no substituye el punto 11.2 del Manual de Políticas. La reserva creada bajo el punto 11.2 es independiente a la reserva creada bajo la siguiente política. 
10. En caso de que el solicitante aún no cuente con un bloque IPv6 asignado por LACNIC, también deberá solicitar un bloque IPv6 cumpliendo con la política aplicable. 

## 11.2. Distribuciones/asignaciones para una terminación gradual de recursos IPv4 
1. LACNIC creará una reserva de un /10 de direccionamiento IPv4 con motivo de realizar una terminación gradual de recursos IPv4 en la región LACNIC. 
2. LACNIC solo podrá realizar distribuciones o asignaciones de recursos IPv4 mayores o iguales a /24 y menores o iguales a /22 de esta reserva. 
3. LACNIC podrá realizar distribuciones o asignaciones de esta reserva a partir de la aprobación de la primera solicitud de recursos IPv4 que no pueda ser satisfecha en su totalidad por falta de recursos IPv4 en la región LACNIC. 
4. Las solicitudes de recursos IPv4 menores a /22 que se encuentren pendientes por aprobación solo podrán recibir un /22 una vez que esta política es vigente. 
5. Las organizaciones que reciban recursos IPv4 de LACNIC bajo las condiciones establecidas en la siguiente política podrán recibir recursos IPv4 adicionales por parte de LACNIC seis meses después siempre y cuando generen una nueva solicitud que justifique la necesidad de recursos IPv4 adicionales según las políticas vigentes de distribución o asignación de direccionamiento IPv4. Las organizaciones que soliciten direccionamiento para infraestructura critica, podrán solicitar hasta un /22 en cualquier momento. 
6. Un bloque recibido bajo esta política no podrá ser transferido siguiendo el punto 2.3.2.18 del manual de políticas durante un periodo de tres años. Lo mismo aplica para sus subbloques, es decir, bloques que agrupen un subconjunto de las direcciones IPv4 que contiene el bloque. 
7. La presente propuesta no substituye el punto 11.1 del manual de políticas. La reserva creada bajo el punto 11.1 es independiente a la reserva creada bajo la siguiente propuesta.

 ## 11.3. Distribuciones/asignaciones de espacio IPv4 distribuido por la IANA post agotamiento 

Los recursos IPv4 distribuidos por la IANA a LACNIC una vez que el punto 11.2 del Manual de Políticas sea vigente solamente podrán ser distribuidos/asignados bajo los lineamientos definidos en el punto 11.1 del Manual de Políticas.

# 12. Registro y validación de “abuse-c” y “abuse-mailbox” 

## 12.1. Descripción del “abuse-c” y “abuse-mailbox” 

Todos los recursos que utilicen los sistemas de registro de LACNIC deben incluir obligatoriamente, en las entradas de WHOIS correspondientes, el atributo de contacto abuse-c (contacto de abuso), como mínimo con un email abuse-mailbox válido, monitorizado y adecuadamente atendido, que permita enviar reportes manuales o automáticos de comportamientos abusivos, seguridad, y similares. 

El atributo abuse-mailbox debe estar disponible sin restricciones vía whois, APIs y futuras tecnologías. 

Teniendo en cuenta la naturaleza jerárquica de los objetos, los heredados de aquellos distribuidos directamente por LACNIC (por ejemplo, sub-asignaciones), están cubiertos por los objetos de nivel superior y su propio atributo “abuse-c” es opcional. 

Siguiendo prácticas habituales, otros atributos “email” pueden ser incluidos para otros propósitos. 

## 12.2. Acerca del “abuse-mailbox” 

El “abuse-mailbox” tiene las siguientes características: 

- Requiere intervención por parte del destinatario. 
- No debe exigir el uso de un formulario para reportar un abuso. 
- Debe garantizar que los reportes de abuso, logs, cabeceras, ejemplos, etc., relativos al caso de abuso, sean recibidos. 

## 12.3. Objetivos de la validación del “abuse-c”/“abuse-mailbox” 

El procedimiento, que habrá de ser desarrollado por LACNIC, deberá cumplir con estos objetivos: 

1) Proceso simple que garantice su funcionalidad y el cumplimiento de su propósito. 
2) Confirmar que quien valida: 
- asegura conocer el procedimiento y las políticas de LACNIC 
- monitoriza regularmente el “abuse-mailbox” 
- toma medidas al respecto 
- responde al reporte de abuso.
3) Plazo de validación “inicial” de 15 días. 
4) Si no se valida correctamente, escalado, por cualquier medio posible, con el resto de los contactos disponibles, en un plazo “adicional” de 15 días. 

## 12.4. Validación del "abuse-c"/"abuse-mailbox" 

LACNIC validará el cumplimiento de la política de forma periódica, al menos dos veces al año, y cuando se creen o modifiquen los atributos del “abuse-c”. 

El incumplimiento por parte de cualquier organización se produce si no se ha validado en el plazo “inicial” ni “adicional”. 

## 12.5. Mecanismo de escalado a LACNIC 

Comportamientos fraudulentos (por ejemplo, “abuse-mailbox” que solo responden a emails de LACNIC, a determinado asunto o determinado cuerpo del mensaje), o el incumplimiento del resto de los aspectos de esta política (la incorrecta o no atención de los casos de abuso), podrán ser reportados a LACNIC, para su re-validación según 12.4.

# A. APENDICES 

a. Apéndice 1. Lista de países y territorios de cobertura de LACNIC. 

Lista de países y territorios de cobertura de LACNIC: 

- Argentina 
- Aruba 
- Belice 
- Bolivia 
- Bonaire 
- Brasil 
- Chile 
- Colombia 
- Costa Rica 
- Cuba 
- Curazao 
- Ecuador 
- El Salvador 
- Guatemala 
- Guyana 
- Guyana Francesa 
- Haití 
- Honduras 
- Islas Falkland (Malvinas) 
- México 
- Nicaragua 
- Panamá 
- Paraguay 
- Perú 
- República Dominicana 
- Saba 
- San Eustaquio 
- San Martin 
- South Georgia and The South Sandwich Islands 
- Suriname 
- Trinidad y Tobago 
- Uruguay 
- Venezuela

b. Apéndice 2: HD Ratio 

El HD Ratio no tiene el fin de reemplazar las mediciones tradicionales de uso que los ISPs tienen actualmente con IPv4. De hecho, el HD Ratio aún requiere el conteo de objetos asignados. El principal valor del HD Ratio es su utilidad al determinar los rangos razonables de utilización para un espacio de direcciones de un tamaño dado. Este documento utiliza el HD Ratio para determinar los rangos en los cuales una distribución dada ha alcanzado un nivel aceptable de utilización y se justifica la distribución de espacio adicional. 

El rango de utilización T, expresado como un número individual de prefijos /48 a ser distribuidos desde un prefijo P de IPv6 puede ser calculado como: 

T=2((48-P)*HD)

Por consiguiente, el rango de utilización de una organización que solicita subsecuentes distribuciones de bloques de direcciones IPv6 es especificado en función del tamaño del prefijo y el HD ratio. Esta utilización se refiere a la asignación de /48s a los usuarios finales y no a la utilización de esos /48s dentro de los usuarios finales. Es un HD ratio de la utilización de una distribución de direcciones y no de la utilización de una asignación de direcciones. 

De acuerdo a las recomendaciones de [RFC 3194], este documento adopta un HD Ratio de 0.94 como el rango de utilización para distribuciones de espacio de direcciones IPv6. 

La siguiente tabla ofrece cifras absolutas y porcentajes de utilización de direcciones equivalentes para prefijos IPv6 correspondientes a un HD- Ratio de 0.94 

c. Apéndice 3: Reporte adicional para la distribución de espacio de direcciones IPv4 

d. Apéndice 4: Reporte de distribución de recursos IPv4 

La siguiente planilla, tiene como propósito informar a LACNIC la distribución de bloques IPv4 asignado a su Organización, por favor, complete las columnas con la información solicitada. Tenga en cuenta que solo deberá detallar los bloques asignados directamente por LACNIC o un NIR (México o Brasil) y cuyas subasignaciones sean iguales o menores a /30.

e. Apéndice 5: Requisitos para los candidatos para el ASO AC Proceso de Nominaciones del Address Council 

Cualquier individuo proveniente de la región de LACNIC puede ser nominado en este proceso, con la excepción de los integrantes del staff de cualquier RIR, los integrantes del Directorio de LACNIC y las personas de la misma nacionalidad de alguno de los miembros en ejercicio en el ASO/AC elegidos por la comunidad de LACNIC. Auto nominaciones son permitidas. 

Los candidatos, para ser admitidos, deberán declarar tener conocimiento del proceso de desarrollo de políticas de LACNIC, el rol del ASO AC y las formas de participación de la comunidad en estos procesos. 

Si vencido el plazo para la presentación de candidatos no se hubiera presentado ningún candidato que cumpla con todos los requerimientos, se anunciará un nuevo plazo de 15 días para la presentación de candidatos donde no regirá la restricción relativa al país de procedencia de los candidatos. 

En caso de que un miembro del ASO AC sea elegido para ocupar un cargo en el Directorio de LACNIC, éste deberá renunciar a su cargo en el ASO AC antes de asumir su cargo en el Directorio.

# B. REFERENCIAS 
[RFC 1112] “Host extensions for IP multicasting” S.E. Deering 08/1989 RFC 1112 

[RFC 1466] “Guidelines for Management of IP Address Space” E. Gerich 05/1993 RFC 1466 
[RFC 1518] “An Architecture for IP Address Allocation with CIDR”, Y. Rekhter and T. Li 09/1993 RFC 1518 
[RFC 1519] “Classless Inter−Domain Routing (CIDR): an Address Assignment and Aggregation Strategy”, V. Fuller, T. Li, J. Yu, and K. Varadham, 09/1993 RFC 1519 
[RFC 1715] "The H Ratio for Address Assignment Efficiency", C. Huitema. November 1994, RFC 1715. 
[RFC 1918] “Address Allocation for Private Internets”, Y. Rekhter , D. Karrenberg , R. Moskowitz , G. de Groot , and E. Lear 02/1996 RFC 1918. 
[RFC 1930] “Guidelines for creation, selection and registration de an Autonomous System (AS)”, J. Hawkinson 03/1996 RFC 1930. 
[RFC 2050] “Internet Registry IP Allocation Guidelines”, K. Hubbard, M. Kosters, D. Conrad, D. Karrenberg, J. Postel 11/1996 RFC 2050. 
[RFC 2317] “Classless IN−ADDR.ARPA delegation”, H. Eidnes, G. de Groot, P. Vixie 03/1998 RFC 2317 
[RFC 2373] "IP Version 6 Addressing Architecture", R. Hinden, S. Deering. July 1998, RFC 2373. 
[RFC 2373bis] http://www.ietf.org/internet-drafts/draft-ietf-ipngwg-addr-arch-v3-07.txt 
[RFC 2928] "Initial IPv6 Sub TLA ID Assignments", R. Hinden, S. Deering, R. Fink, T. Hain. September 2000, RFC 2928. 
[RFC 3177] "IAB/IESG Recommendations on IPv6 Address". IAB, IESG. September 2001, RFC 3177. 
[RFC 3194] "The H Density Ratio for Address Assignment Efficiency An Update on the H ratio", A. Durand, C. Huitema. November 2001, RFC 3194. 
[RFC 4893] “BGP Support for Four-octet AS Number Space”, Q. Vohra, E. Chen 05/2007 RFC 4893. 
[IAB Request] "Email from IAB to IANA", http://www.iab.org/iab/DOCUMENTS/ IPv6addressspace.txt 
[RIRs on 48] http://www.arin.net/policy/ipv6reassign.html 
[RIRv6 Policies] http://www.apnic.net/policy/ipv6-address-policy.html https://www.afrinic.net/docs/policies/afpol-v6200407-000.htm http://www.ripe.net/ripe/docs/ripe-466.html https://www.arin.net/policy/nrpm.html
