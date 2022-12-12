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
