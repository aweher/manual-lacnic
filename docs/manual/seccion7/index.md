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