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