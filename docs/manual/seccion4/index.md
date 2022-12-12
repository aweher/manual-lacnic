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