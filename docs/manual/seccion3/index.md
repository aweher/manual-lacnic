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