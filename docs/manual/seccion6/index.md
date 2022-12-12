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