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