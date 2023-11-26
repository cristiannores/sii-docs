INSTRUCTIVO TÉCNICO
FACTURA ELECTRÓNICA
Instructivo para la Emisión de Facturas y otros Documentos Tributarios
Electrónicos, en los computadores de los contribuyentes
15/10/2009
Modificaciones sobre versión anterior:
Se agrega ANEXO 5: Compatibilidad y Restricciones de Uso de Opciones Habilitadas en la
WEB.
En Anexos 3 y 4, se destaca la importancia de no hacer envíos de documentos tributarios
electrónicos como un único texto, sin incluir saltos de línea.
Servicio de Impuestos Internos
FACTURA ELECTRÓNICA - INSTRUCTIVO TÉCNICO PARA LA EMISIÓN DE
DOCUMENTOS .......................................................................................................................... 3
Objetivo .................................................................................................................................... 3
1. Actividades Previas a la Emisión de Documentos. .......................................................... 3
1.1 Enrolamiento .................................................................................................................. 3
1.2 Autorización de Firmantes ............................................................................................. 3
1.3 Obtención de rango de folios autorizados y Código de Autorización de Folios. ........... 3
1.4 Verificaciones al “Código de Autorización de Folios”. ................................................. 4
2.- Funciones a Incorporar en el Sistema de Facturación......................................................... 5
2.1.- Alimentar su sistema de facturación con los folios autorizados por el SII. ................. 5
2.2.- Asignar número de folio único a cada documento. ...................................................... 5
2.3.- Calcular el Timbre Electrónico para cada documento. ................................................ 5
2.4.- Generar documento en formato XML exigido por el SII............................................. 5
2.5.- Firmar documento completo. ....................................................................................... 5
2.6.- Adecuar procedimiento de impresión de documentos ................................................ 6
2.7.- Implementar el intercambio de DTEs con otros contribuyentes autorizados ............. 6
DESCRIPCIÓN DE ANEXOS: ............................................................................................... 7
ANEXO 1: Código de Autorización de Folios. ........................................................................ 8
A.1.1. Proceso de Generación De Una Autorización de Folios. ........................................ 8
A.1.2 Estructura de la Autorización .................................................................................... 9
A.1.3 Almacenamiento y Uso del CAF ............................................................................. 15
ANEXO 2: Timbre Electrónico del DTE ............................................................................. 16
A.2.1 Introducción .............................................................................................................. 16
A.2.2 Generación De Un Timbre ....................................................................................... 16
A.2.3 Estructura .................................................................................................................. 16
A.2.4 Consideraciones para la Generación y Firma del Timbre Electrónico. .................... 20
A.2.5 Reglas Para La Generación e Impresión Del Timbre PDF417................................. 22
ANEXO 3: Uso de XML en Envíos de Documentos Tributarios Electrónicos (DTEs). ...... 23
A 3.1. Formato XML y Base64 .......................................................................................... 23
A 3.2. Envío de DTE .......................................................................................................... 24
A.3.3. Carátula de Identificación de un Envío ................................................................... 24
A.3.4. Documento Tributario Electrónico (DTE) .............................................................. 26
A.3.3.1 Firma Digital del DTE ........................................................................................... 27
A.3.3.2 Valores Llave Pública del DTE ............................................................................. 28
A.3.3.3. Documentación Adicional. ................................................................................... 28
A.3.3.4. Tamaño Máximo de Envíos de Información al SII .............................................. 28
ANEXO 4: Intercambio de Información entre Contribuyentes Electrónicos......................... 29
4.1 Respuesta de Recepción de un envío de DTEs ............................................................ 29
4.2 Respuesta de Aprobación/Rechazo Comercial de DTEs ............................................ 29
4.3 Reglas para Intercambio de Información entre Emisores Electrónicos ....................... 29
ANEXO 5: Compatibilidad y Restricciones de Uso de Opciones Habilitadas en la WEB.... 30
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 2 de 30
Servicio de Impuestos Internos
FACTURA ELECTRÓNICA - INSTRUCTIVO TÉCNICO PARA LA EMISIÓN DE
DOCUMENTOS
Objetivo
Entregar los antecedentes técnicos necesarios para que los contribuyentes autorizados por el SII para
emitir documentos tributarios electrónicos puedan generar y enviar documentos válidos, de acuerdo a la
normativa del Servicio.
1. Actividades Previas a la Emisión de Documentos.
Para emitir documentos tributarios electrónicos las empresas previamente deben estar enroladas para
ello por el SII y definir los firmantes autorizados al interior de su empresa. De acuerdo con esto, las
actividades previas a la emisión de documentos son:
1.1 Enrolamiento
El SII registra los siguientes datos de los contribuyentes autorizados: la fecha de autorización, los tipos
de documentos electrónicos autorizados, la identificación del Usuario-Administrador y la dirección de
correo electrónico para intercambio de información con otros contribuyentes autorizados.
1.2 Autorización de Firmantes
La firma digital es una pieza fundamental en el sistema de factura electrónica, ya que permite asegurar
la integridad de los documentos y la autenticidad del emisor de los mismos. Las empresas enroladas al
sistema deberán registrar ante el SII los firmantes autorizados al interior de su empresa para realizar
ciertas acciones que el SII ha definido que deben efectuarse sólo por parte de los firmantes autorizados
de la empresa:
- Definición y actualización de firmantes autorizados ante el SII, lo que deberá ser efectuado por
un “Usuario-Administrador” designado por la empresa a través del representante legal.
- Solicitar números de folios para generar documentos electrónicos tributarios válidos.
- Solicitar la anulación de folios previamente autorizados, lo que también debería ser ejecutado
por el perfil de “Usuario-Administrador”. Esta anulación de folios se puede utilizar sólo cuando
los DTEs generados erróneamente no hayan sido enviados al SII.
- Firmar documentos tributarios electrónicos.
- Enviar documentos emitidos al SII y consultar diagnóstico de validación de documentos en el
sitio del SII.
La empresa deberá adquirir certificados digitales para los firmantes autorizados al interior de la
empresa.
1.3 Obtención de rango de folios autorizados y Código de Autorización de Folios.
La obtención del rango de folios autorizados, sólo la podrán efectuar los firmantes autorizados, quienes,
se deberán autenticar en el sitio del SII, con certificado digital.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 3 de 30
Servicio de Impuestos Internos
En respuesta a las solicitudes de folios válidas, el SII entregará la autorización consistente en el Código
de autorización de folios y en un par de llaves que permiten generar y verificar el timbre electrónico
(Ver ANEXO 1).
1.4 Verificaciones al “Código de Autorización de Folios”.
El contribuyente deberá verificar la validez y autenticidad del Código de Autorización de Folios (CAF)
recibido del SII. Para ello debería:
• Verificar que el CAF esté correctamente firmado por el SII, verificando la firma del SII que
incluye, con la llave pública que el SII publique para esos efectos.
• Verificar que el par de llaves que incluye el CAF funciona correctamente. Para ello debería
generar una firma con la llave privada y verificar la firma con la llave pública.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 4 de 30
Servicio de Impuestos Internos
2.- Funciones a Incorporar en el Sistema de Facturación.
Todo documento electrónico debe estar numerado con un folio único y estar firmado en forma
electrónica en su totalidad, incluyendo el timbre Para ello el contribuyente deberá incorporar a sus
aplicaciones las siguientes funciones:
2.1.- Alimentar su sistema de facturación con los folios autorizados por el SII.
El contribuyente debe ingresar como parámetros a su sistema de facturación el “Código de autorización
de folios” y la llave privada entregada por el SII, que le permite generar el timbre electrónico.
El sistema del contribuyente debe administrar el Código de autorización de folios por tipo de
documento y rango de folios con que esté operando. Tanto el CAF como la llave privada de timbraje
asignada por el SII, deben contar con mecanismos de seguridad que impidan el acceso a dicha
información a personas no autorizadas.
2.2.- Asignar número de folio único a cada documento.
El sistema del contribuyente debe asignar en forma única un número de folio para cada documento,
utilizando para ello el rango del código de autorización de folios con que fue alimentado. Es
obligatorio, como medida de seguridad, que esta asignación de folios sea hecha rigurosamente en forma
unívoca para cada documento.
2.3.- Calcular el Timbre Electrónico para cada documento.
El Timbre Electrónico del DTE consiste en una firma electrónica, sobre los campos que se definen
como representativos del documento e incluyendo el Código de Autorización de Folios proporcionado
por el SII.
La firma que constituye el timbre electrónico debe ser generada con la llave privada entregada por el
SII junto con el rango de folios correspondiente.
Los campos y la estructura del Timbre electrónico del DTE se detallan en ANEXO 2.
2.4.- Generar documento en formato XML exigido por el SII.
El contribuyente debe generar el documento en formato XML de acuerdo al formato definido por el SII.
Ver ANEXO 3. Uso de XML en Envíos de Documentos Tributarios Electrónicos.
2.5.- Firmar documento completo.
El contribuyente debe generar la firma digital sobre el documento completo. Esta firma debe ser
generada con un certificado digital vigente y no revocado al momento de la firma.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 5 de 30
Servicio de Impuestos Internos
2.6.- Adecuar procedimiento de impresión de documentos
El contribuyente debe adecuar sus procedimientos y formularios utilizados para la impresión, con el fin
de generar la representación impresa según la norma del SII, incluyendo el código de barras 2D,
simbología PDF417, que contenga la información del código del timbre electrónico.
La información incluida en la impresión del Timbre Electrónico es:
1. Versión del timbre electrónico
2. Rut del Emisor
3. Tipo de Documento
4. Número de Folio
5. Fecha de emisión
6. Rut del Receptor
7. Razón Social Receptor
8. Monto total
9. Descripción del primer Item del Detalle
10. Fecha y hora de generación del timbre electrónico,
11. Código de Autorización de Folios (proporcionado por el SII)
12. Algoritmo de firma (Hash y encriptación) que se usó en la firma con que
generó el timbre
13. Firma digital sobre los datos anteriores, con la llave privada entregada por
el SII para dicho propósito.
2.7.- Implementar el intercambio de DTEs con otros contribuyentes autorizados
Para el intercambio de información entre contribuyentes autorizados se deberá tener habilitado como
mínimo la posibilidad recibir y enviar información por e-mail con un archivo adjunto que contenga los
documentos, el comprobante de recepción o rechazo, todos ellos en el formato XML establecido por el
SII. (ver ANEXO 3 con esquema de los envíos de DTEs y ANEXO 4 con esquema XML de la
recepción o rechazo)
Cada contribuyente autorizado tendrá registrada en el SII la casilla electrónica a la cual se le debe
enviar la información relacionada con factura electrónica: Envíos de DTEs, Comprobantes de
Recepción y de Rechazo.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 6 de 30
Servicio de Impuestos Internos
DESCRIPCIÓN DE ANEXOS:
ANEXO 1. Código de Autorización de Folios
ANEXO 2. Timbre Electrónico del DTE
ANEXO 3. Uso de XML en Envíos de DTEs
ANEXO 4. Intercambio de información entre contribuyentes
Nota Importante:
Los ejemplos de llaves y firmas (generalmente muy largos) que se incluyen en estos ANEXOS, han
sido acortados (lo que se indica con ...), para facilitar la lectura del documento. En los documentos
tributarios electrónicos válidos que los contribuyentes emitan, llaves y firmas criptográficas se deben
codificar en Base64, estándar para intercambiar datos binarios, según especificación del documento
RFC 2045.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 7 de 30
Servicio de Impuestos Internos
ANEXO 1: Código de Autorización de Folios.
A.1.1. Proceso de Generación De Una Autorización de Folios.
La genera el SII en base a una solicitud vía web de autorización de folios enviada por un contribuyente.
a) El contribuyente, al solicitar la autorización debe autenticarse con certificado digital y señalar
el tipo de DTE y el número de Folios requeridos. El SII determinará si autorizará el rango
solicitado, o una parte de él.
b) El SII genera un par de llaves (pública y privada) asociadas al rango de folios, y genera la
sección Datos con la información del contribuyente, de los números autorizados y la llave
pública, según la estructura definida en A.1.2.
c) El SII firma digitalmente la sección Datos usando un certificado digital de propiedad de SII
construyendo la sección Firma del Código de autorización
d) Se agrega a continuación la llave privada que deberá usar el contribuyente para timbrar
electrónicamente.
e) La autorización estará formada por las secciones CAF (Datos, Firma) y Llaves Privada y
Pública, según el formato XML que se define en A.1.2 .
1. Código de Autorización de Folios, CAF (Datos, Firma) que incluye:
a) Versión del timbre electrónico
b) Rut Empresa
c) Razón Social Empresa
d) Tipo de documento
e) Rango de folios autorizados
f) Fecha de autorización de folios
g) Llave pública generada por el SII, para verificar la validez del timbre
electrónico.
h) Identificador de la llave pública del SII que permite verificar la firma del SII
sobre el CAF.
i) Firma del SII sobre los campos anteriores, con su llave privada. Con la llave
pública del SII el contribuyente puede verificar la firma del SII, para
asegurarse de la integridad y autenticidad de la información recibida.
2. Llave privada generada por el SII, que permite generar el timbre electrónico
3. Llave pública generada por el SII, que permite verificar la validez del timbre
electrónico (es la misma incluida en el CAF (f), pero en un formato distinto).
f) El documento XML resultante de estas operaciones, es enviado al contribuyente.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 8 de 30
Servicio de Impuestos Internos
A.1.2 Estructura de la Autorización
La autorización es un archivo XML que se compone de 3 secciones: el CAF (código de autorización de
folios), la llave privada (RSASK) y la llave pública (RSAPUBK).
El código de autorización de folios a su vez, se compone de dos elementos, datos y firma, según lo
siguiente:
<AUTORIZACION>
<CAF version=”1.0”>
<DA> .
.
.
</DA>
<FRMA>... <FRMA>
</CAF>
<RSASK> ......</RSASK>
<RSAPUBK> .... </RSAPUBK>
</AUTORIZACION>
Sección Datos
La sección Datos (<DA>), contiene los datos relativos al contribuyente, al tipo de DTE que se está
autorizando y al rango de folios que abarca esta autorización. La estructura detallada es la siguiente:
<CAF version=”1.0”>
<DA>
<RE>.... </RE>
<RS>.... </RS>
<TD>...</TD>
<RNG>
<D>... </D>
<H>... </H>
</RNG>
<FA>... </FA>
<RSAPK> ... </RSAPK>
<IDK> ... <IDK>
</DA>
<FRMA>... </FRMA>
</CAF>
Donde los campos que se etiquetan son:
a) Versión: es una cadena de caracteres ASCII indicando la versión del código. Por ejemplo “1.0”.
b) RUT Empresa (<RE>) : es una cadena de caracteres ASCII indicando el RUT del emisor al cual
está autorizando este código en formato XXXXXXXX-X. Por ejemplo “11111111-1”, el cual
equivale al contribuyente con RUT 11.111.111-1
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 9 de 30
Servicio de Impuestos Internos
c) Razon Social de la Empresa: representa el nombre de la empresa asociado al Rut Empresa, con un
máximo de 40 caracteres.
d) Tipo DTE (<TD>): es una cadena de caracteres ASCII que representa el tipo de DTE que se está
autorizando (Facturas, Guías de Despacho, etc.). Este valor está conforme a la definición de tipos
de DTE impuesta por SII, donde, por citar un ejemplo, el tipo de DTE de factura quedará
representado por la cadena de caracteres ASCII “33”.
e) Rango de Folios (<RNG>): es un par de valores indicando el rango de folios autorizados en
estructura “Desde-Hasta”. Por ejemplo, un código autorizando el rango de folios desde el 50 al 110,
contendría los valores desde “50” hasta “110”.
f) Fecha (<FA>) : es una cadena de caracteres ASCII indicando la fecha en que fue autorizado el
rango de folios en formato AAAA-MM-DD, es decir, los primeros 4 caracteres señalando el año,
los dos siguientes señalando el mes y los últimos 2 señalando el día, separados por guiones. Si la
fecha fuese el 29 de Febrero del 2004, el valor quedaría “2004-02-29”.
g) Llave Pública del contribuyente (<RSAPK>) : Como define el modelo de operación de documentos
tributarios electrónicos, cada vez que el contribuyente solicita nuevos folios, el SII le proporciona
además el par de llaves (pública y privada) que le permiten generar y verificar el timbre electrónico
de los DTEs asociados. Este valor, es una cadena de caracteres ASCII con el valor de la llave
pública, generada por el SII. Inicialmente el SII entregará sólo llaves correspondientes al algoritmo
criptográfico de llave pública RSA.
Una llave pública RSA tiene dos valores numéricos que la definen, un módulo y un exponente. El
valor de “Llave Pública del contribuyente” queda definido por estos 2 valores, como se muestra a
continuación:
<RSAPK>
<M>... </M>
<E>... </E>
</RSAPK>
Módulo <M> : Indica el valor del módulo de la llave. Este valor es la codificación en Base64
del arreglo de bytes en orden Big-Endian (el byte más significativo es el
elemento 0 del arreglo) que contiene el valor entero sin signo (unsigned
integer) del módulo.
Exponente <E> : Indica el valor del exponente de la llave. Este valor es la codificación en
Base64 del arreglo de bytes en orden Big-Endian (el byte más significativo
es el elemento 0 del arreglo) que contiene el valor entero sin signo (unsigned
integer) del exponente.
<RSAPK>
<M>AMPa7mxz8ysTRazehr5/Oiau98/ ... lku7y2twwndI/142ds54aWjqd </M>
<E>A2.../B</E>
</RSAPK>
Figura A.1: Ejemplo de “Llave Pública del contribuyente” para una llave RSA
h) Identificación llave pública del SII (<IDK>): Identificación de la llave pública del SII que permite
verificar la firma del SII sobre el CAF (<FRMA>). Se trata de un identificador de la llave y no de la
llave.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 10 de 30
Servicio de Impuestos Internos
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 11 de 30
Servicio de Impuestos Internos
Ejemplo:
Si se estuviese
• Autorizando al contribuyente RUT 11.111.111-1, con razón social “Ejemplo S.A.”
• el rango de folios desde el 50 al 101
• para el tipo de DTE factura (definida como “33” por SII)
• con fecha 10 de Junio del 2002
• donde al firmante autorizado que solicitó los folios se le generó una llave pública RSA en la
solicitud de autorización y
• la llave pública del SII que verifica su firma sobre el CAF tiene la identificación 1
La sección Datos quedaría compuesta por la cadena de caracteres mostrada en Figura A.2
<DA>
<RE>11111111-1</RE>
<RS>Ejemplo S.A.</RS>
<TD>33</TD>
<RNG>
<D>50</D>
<H>101</H>
</RNG>
<FA>2002-06-10</FA>
<RSAPK>
<M>AMPa7mxz8ysTRazehr5/Oiau98/ ... lku7y2twwndI/142ds54aWjqd </M>
<E>A2.../B</E>
</RSAPK>
<IDK> 1 </IDK>
</DA>
Figura A.2: Ejemplo de Datos
Sección Firma
La sección Firma (<FRMA>) corresponde a la firma digital del SII sobre Datos (<DA>) es decir
Firma = FirmaSII(Datos).
Se entiende por firma digital a la aplicación de un algoritmo criptográfico de firma sobre el extracto
(digest) calculado a partir de Datos. A la fecha de este documento, el modelo de operación de DTEs
soporta dos algoritmos de firmas digitales SHA1+RSA y SHA1+DSA. Dependiendo del algoritmo, el
valor de este campo es como sigue a continuación:
a) Algoritmos SHA1 y RSA: firma digital generada con el algoritmo de digest SHA1 y el algoritmo
criptográfico de firma RSA según lo definido por OSI Interoperability Workshop. El valor de
“Firma” queda definido en este caso de la siguiente forma:
<FRMA algoritmo=”SHA1withRSA”>
</FRMA>
Donde:
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 12 de 30
Servicio de Impuestos Internos
- SHA1withRSA: Indica que la firma fue generada usando el algoritmo de digest SHA1 y el
algoritmo criptográfico de firma RSA. El valor es la cadena de caracteres ASCII
“SHA1withRSA”.
- Valor Firma (<FRMA>) : Contiene el valor de la firma. Este valor es la codificación en Base64
del valor de la firma usando el formato DER encoded PKCS#1.
<FRMA algoritmo=”SHA1withRSA”>
F2/hdgF42d4eAw ... iU7=6faRDs6k=
</FRMA>
Figura A.3: Ejemplo de Firma SHA1+RSA
b) Algoritmos SHA1 y DSA: firma digital generada con el algoritmo de digest SHA1 y el algoritmo
criptográfico de firma DSA según lo definido por FIPS PUB 186. El valor de “Firma” queda
definido en este caso como se muestra en A.6.
<FRMA algoritmo=”SHA1withDSA”>
</FRMA>
Donde:
- SHA1withDSA: Indica que la firma fue generada usando el algoritmo de digest SHA1 y el
algoritmo criptográfico de firma DSA. El valor es la cadena de caracteres ASCII
“SHA1withDSA”.
- Valor Firma (<FRMA>): Contiene el valor de la firma. Una firma utilizando DSA esta
compuesta por dos valores r y s. Este valor es la codificación en Base64 del valor de la firma
representado por la secuencia ASN.1 de dos valores INTEGER de r y s en ese orden
(SEQUENCE ::= r INTEGER, s INTEGER ).
<FRMA algoritmo=”SHA1withDSA”>
MCw7yGfcx451 ... aKhy72bvDw==
</FRMA>
Figura A.4: Ejemplo de Firma SHA1+DSA
Sección Llave Privada
La sección Llave Privada (<RSASK>) corresponde a llave privada asignada por el SII al contribuyente
para generar el timbre electrónicos de los DTEs del rango de folios respectivo. La firma generada con la
llave privada puede ser validada con la llave pública asociada (<RSAPK>)
La llave privada RSA generada por el SII, se entrega en formato estándar PEM (Privacy Enhanced
Mail).
Sección Llave Pública
La sección Llave Pública (<RSAPUBK>) corresponde a la llave pública asignada por el SII al
contribuyente, para verificar el timbre electrónico de los DTEs. esta llave también se incluye dentro del
CAF y se entrega además en formato estándar PEM (Privacy Enhanced Mail), para facilitar al
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 13 de 30
Servicio de Impuestos Internos
contribuyente la verificación del par de llaves proporcionadas por el SII, antes de comenzar a
utilizarlas.
En el ejemplo de Figura A.2,
Si se estuviese:
• Autorizando al contribuyente con RUT 11.111.111-1, con Razon Social “Ejemplo S.A:”
• el rango de folios desde el 50 al 101
• para el tipo de DTE factura (definida como “33” por SII)
• con fecha 10 de Junio del 2002
• donde al solicitante se le asignó una llave pública RSA
• el identificador de la llave pública del SII que verifica la firma es 3
• el SII firmó la sección datos usando SHA1+RSA y asignó la llave privada RSA respectiva
El código de Autorización de folios quedaría compuesto por la cadena de caracteres mostrada
<AUTORIZACION>
<CAF version=”1.0”>
<DA>
<RE>11111111-1</RE>
<RS>Ejemplo S.A.</RS>
<TD>33</TD>
<RNG>
<D>50</D>
<H>101</H>
</RNG>
<FA>2002-06-10</FA>
<RSAPK>
<M>AMPa7mxz8ysTRazehr5/Oiau98/ ... lku7y2twwndI/142ds54aWjqd </M>
<E>A2.../B</E>
</RSAPK>
<IDK> 3 </IDK>
</DA>
<FRMA algoritmo=”SHA1withRSA”>
F2/hdgF42d4eAw ... iU7=6faRDs6k=
</FRMA>
</CAF>
<RSASK>:----- BEGIN RSA PRIVATE KEY-----
nShd63c ...
-----END RSA PRIVATE KEY-----
</RSASK>
<RSAPUBK>:----- BEGIN PUBLIC KEY-----
fs3D21axS ...
-----END PUBLIC KEY-----
</RSAPUBK>
</AUTORIZACION>
Figura A.5: Ejemplo de Autorización de Folios
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 14 de 30
Servicio de Impuestos Internos
A.1.3 Almacenamiento y Uso del CAF
El archivo XML con la información de folios autorizados por el SII debe ser almacenado y resguardado
adecuadamente por los contribuyentes autorizados ya que contiene la información que permite asignar
folios y generar el timbre electrónico de los documentos. tributarios electrónicos que emita.
El CAF debe incluirse en el timbre electrónico de cada documento tributario para permitir que el SII
verifique que el número de folio fue efectivamente autorizado por el Servicio. Esta verificación del SII
arrojará un resultado negativo si el CAF incluido en el timbre electrónico presenta alguna diferencia
con el entregado por el SII, por lo que resulta de vital importancia almacenar y conservar el CAF
tal como fue entregado por el Servicio.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 15 de 30
Servicio de Impuestos Internos
ANEXO 2: Timbre Electrónico del DTE
A.2.1 Introducción
Cada documento emitido debe ir timbrado electrónicamente, incluyendo la información representativa
del DTE y el código de autorización de folios asociado.
A.2.2 Generación De Un Timbre
a) El contribuyente debe identificar cuál es el código de autorización de folios correspondiente al
folio del DTE que va a emitir. Este CAF debe ser incorporado a la sección Datos del timbre, sin
modificación alguna respecto al entregado por el SII.
b) Debe armar la sección Datos del timbre electrónico del DTE con los datos del DTE según la
estructura definida en A.2.2 Estructura.
c) Posteriormente, el contribuyente debe firmar digitalmente la sección Datos usando la llave
privada entregada por el SII al autorizar los folios y construye la sección Firma.
d) El timbre estará formado por las secciones Datos y Firma según el formato que se definió en
la sección anterior A.2.2 Estructura.
Este timbre, se debe incluir en el DTE resultante y en su versión impresa. En el caso de la versión
impresa del DTE, el timbre se imprime en un código de barras bidimensional, simbología PDF417.
A.2.3 Estructura
El Timbre es una cadena de caracteres ASCII que se compone de dos secciones, datos y firma, como se
detalla a continuación:
<TED version=”1.0”>
<DD> .
.
.
</DD>
<FRMT algoritmo=”SHA1withRSA”>
...
</FRMT>
</TED>
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 16 de 30
Servicio de Impuestos Internos
Sección Datos
La sección Datos (<DD>), contiene los datos representativos del DTE: RUT del emisor, tipo
del DTE, folio del DTE, fecha de emisión, RUT del receptor, Razon Social del Receptor,
Monto Total del DTE, Descripción del primer Item de detalle, el CAF y el TimeStamp (fecha y
hora) de generación del timbre, etiquetados de la siguiente forma:
<TED version=”1.0”>
<DD>
<RE>.... </RE>
<TD>... </TD>
<F>... </F>
<FE>... </FE>
<RR>.... </RR>
<RSR>.... </RSR>
<MNT>... </MNT>
<IT1>.... </IT1>
<CAF>... </CAF>
<TSTED>… </TSTED>
</DD>
Donde las etiquetas representan:
a) Versión: es una cadena de caracteres ASCII indicando la versión del timbre. La versión que
define este documento es la “1.0”.
b) RUT Emisor (<RE>) : es una cadena de caracteres ASCII indicando el RUT del emisor del
DTE en formato XXXXXXXX-X. Por ejemplo “11111111-1”, que equivale al contribuyente
emisor con RUT 11.111.111-1
c) Tipo DTE (<TD>): es una cadena de caracteres ASCII que representa el tipo de DTE que se
está timbrando (Facturas, Guías de Despacho, etc.). Este valor está conforme a la definición de
tipos de DTE impuesta por SII, donde, por citar un ejemplo, el tipo de DTE de factura quedaría
representado por la cadena de caracteres ASCII “33”.
d) Folio DTE (<F>): es una cadena de caracteres indicando el número de folio en notación
decimal entera del DTE que se está timbrando . Por ejemplo, el timbre electrónico del DTE
número de folio 2752, contendría en este valor la cadena ASCII “2752”.
e) Fecha (<FE>): es una cadena de caracteres ASCII indicando la fecha de emisión (generación)
del DTE en formato AAAA-MM-DD, es decir, los primeros 4 caracteres señalando el año, los
dos siguientes señalando el mes y los últimos 2 señalando el día; separados por el carácter “-“
(guión). Si la fecha fuese el 29 de Febrero del 2004, el valor quedaría “2004-02-29”.
f) RUT Receptor (<RR>): es una cadena de caracteres ASCII indicando el RUT del receptor del
DTE en formato XXXXXXXX-X. Por ejemplo “22222222-2”, que equivale al contribuyente
emisor con RUT 22.222.222-2
g) Razón Social del Receptor (<RSR>): representa el nombre de la empresa asociado al Rut
Empresa, con un máximo de 40 caracteres.
h) Monto Total del DTE (<MNT>) : es una cadena de caracteres ASCII que representa el Monto
Total del DTE en pesos chilenos, en notación decimal entera (sin decimales). Por ejemplo, el
valor 13 queda representado por “13” y el valor 9 queda representado por “9”.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 17 de 30
Servicio de Impuestos Internos
i) Item 1(<IT1>): es una cadena de caracteres que contiene la descripción del primer item del
detalle, con un máximo de 40 caracteres.
j) Código de Autorización de Folios (<CAF>): Contiene el código de autorización de
folios, que autoriza el DTE, es decir, que el folio del DTE está dentro del rango del código de
autorización, que el tipo y emisor coinciden en ambos, y que la llave pública del contribuyente
contenida en el código, es la que verifica la sección Firma del timbre electrónico. Para la
especificación del código de autorización vea el ANEXO 1 “Código de Autorización
de Folios”.
k) TimeStamp del Timbre Electrónico (<TSTED>): Contiene la fecha y hora en que se
generó el timbre electrónico en formato AAAA-MM-DDTHH:MI:SS
Si se estuviese generando el timbre electrónico del
• DTE número 67
• tipo de DTE factura electrónica (definida como “33” por SII)
• del contribuyente emisor RUT 11.111.111-1
• para el Receptor RUT 12345678-5, razon social “Comprador S.A.”
• con fecha 11 de Junio del 2002,
• por un total de 24365 y el primer item del detalle es “Caja de Zapatos”
• el timbre se hubiera generado a las 7 horas con 34 minutos y 15 segundo
la sección Datos quedaría compuesta por la cadena de caracteres mostrada en Figura A.6.
<TED version=”1.0”>
<DD>
<RE>11111111-1</RE>
<TD>33</TD>
<F>67</F>
<FE>2002-06-11</FE>
<RR>12345678-5</RR>
<RSR>Comprador S.A.</RSR>
<MNT>24365</MNT>
<IT1>Caja de Zapatos</IT1>
<CAF>... </CAF>
<TSTED>2002-06-11T07:34:15</TSTED>
</DD>
Figura A.6: Ejemplo de Datos en timbre electrónico (ver detalle de CAF en figura A.5)
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 18 de 30
Servicio de Impuestos Internos
Sección Firma
La sección Firma (<FMRT>) corresponde a la firma digital del contribuyente emisor (con la llave
privada generada y entregada por el SII para ese propósito) sobre Datos (<DD>)
Firma = Firma Contribuyente(Datos)
Según se indicó en A.1.2. el SII entregará sólo llaves para algoritmo de firmas digitales SHA1+RSA
por lo que el valor de “Firma” queda definido de la siguiente forma:
<FRMT algoritmo=”SHA1withRSA”>
...
</FRMT>
Donde:
- SHA1withRSA: Indica que la firma fue generada usando el algoritmo de digest SHA1 y el
algoritmo criptográfico de firma RSA. El valor es la cadena de caracteres ASCII
“SHA1withRSA”.
- Valor Firma (<FMRT>) : Contiene el valor de la firma. Este valor es la codificación en
Base64 del valor de la firma usando el formato DER-encoded PKCS#1.
En Figura A.7 se muestra un ejemplo de “Firma” para el caso SHA1 y RSA.
<
G3=dhiawT5a4/... =09UjhGfsR7l/
FRMT algoritmo=”SHA1withRSA”>
</FRMT>
Figura A.7: Ejemplo de Firma SHA1+RSA
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 19 de 30
Servicio de Impuestos Internos
A.2.4 Consideraciones para la Generación y Firma del Timbre Electrónico.
Los valores de claves públicas, firmas, digest y certificados que se incluyen en los XML descritos
anteriormente para el CAF y Timbre Electrónico, van codificadas en base 64 (como se define en el
RFC 2045 Sección 6.8) y se imprimen a lo más 76 caracteres por línea.
Es importante verificar que las glosas incluidas en el timbre electrónico: Razón Social del Receptor
(tag <RSR>) y Nombre del Item 1 (tag <IT1>) incluyan sólo caracteres codificados de acuerdo al
estándar ISO-8859-1, de lo contrario el SII podría obtener un resultado negativo al verificar la firma
electrónica del timbre y por lo tanto declarar no válido el documento que se esté fiscalizando. El
contribuyente debe cuidar que las librerías que utiliza para firmar no realicen transformaciones sobre la
codificación de los caracteres (por ejemplo a la codificación UTF-8).
Se debe tener presente que en XML se han predefinido de manera estándar 5 representaciones para
caracteres con significado especial dentro de la estructura del XML (predefined entities).
Las entidades predefinidas y su representación estándar son :
Carácter Especial Representación Alternativa
& &amp; &#38;
< &lt; &#60;
> &gt; &#62;
“ &quot; &#34;
‘ &apos; &#39;
Por ejemplo:
La Razón Social Receptor: Empresas A&B Limitada (21 caracteres)
Debe tener la Codificación XML: Empresas A&amp;B Limitada (25 caracteres)
El resto de los caracteres especiales (acentos, eñes, etc.) deben ser codificados de acuerdo a lo
especificado en el set de caracteres ISO-8859-1. Si no se respeta esta convención el archivo con el
envío de DTEs será rechazado al validar el schema, con el error “Invalid Character”.
Para efecto de calcular el digest de la firma digital del timbre electrónico y de la autorización de folios
se eliminan los caracteres de fin de línea y los blancos y/o tab entre TAGS, así como la referencia a
NameSpaces. El digest se calcula sobre el string resultante.
En resumen para generar y firmar correctamente un timbre electrónico, se debe tener presente lo
siguiente:
• El CAF se incluye tal como fue entregado por el SII, sin ningún tipo de modificaciones.
• Los campos de caracteres incluidos en el TED (razón social receptor y descripción del
primer ítem) se deben codificar respetando las entidades predefinidas por XML y el set de
caracteres ISO-8859-1.
• La información incluida en el TED debe coincidir con la información de Encabezado y
Detalle del DTE.
• La firma del TED se realiza sobre el string resultante de eliminar todos los caracteres que
están entre el tag de cierre de un elemento y el tag de inicio del siguiente, sin modificar la
información que va entre el tag de inicio y el tag de fin de los elementos terminales.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 20 de 30
Servicio de Impuestos Internos
Es importante respetar esta indicaciones, de lo contrario la verificación del timbre electrónico resultará
incorrecta.
Debido a que el Timbre Electrónico se debe imprimir en un código de barras 2D (PDF417) y a las
restricciones de espacio asociadas, las firmas que el Timbre Electrónico incluye deben regirse
estrictamente por lo especificado en el presente documento y no por el estándar XMLDSIG como es el
caso de la firma del DTE y envío de DTE.
Por ejemplo para el siguiente Timbre Electrónico, donde \b representa un blanco, \t representa un
tabulador y \n representa un salto de línea:
<TED version=”1.0”> \n
\t <DD> \n
\t\t <RE>11111111-1</RE> \n
\t\t <TD>33</TD> \n
\t\t <F>122</F> \n
\t\t <FE>2002-06-11</FE> \n
\t\t <RR>12345678-5</RR> \n
\t\t <RSR>Empresas A&amp;B Limitada</RSR> \n
\t\t <MNT>24365</MNT> \n
\t\t <IT1>Cajón de Manzanas</IT1> \n
\t\t <CAF version=”1.0”> \n
\t\t <DA> \n
\t\t\t <RE>11111111-1</RE> \n
\t\t\t <RS>Ejemplo S.A.</RS> \n
\t\t\t <TD>33</TD> \n
\t\t\t <RNG> \n
\t\t\t\t <D>125</D> \n
\t\t\t\t <H>160</H> \n
\t\t\t </RNG> \n
\t\t\t <FA>2002-05-14</FA> \n
\t\t\t <RSAPK> \n
\t\t\t\t <M>zf/B…cwx</M> \n
\t\t\t\t <E>QBcs</E> \n
\t\t\t </RSAPK> \n
\t\t\t <IDK>3</IDK> \n
\t\t </DA> \n
\t\t <FRMA>yTfHE...ydmh9fgsj3rv86=</FRMA>\n
\t </CAF> \n
\t <TSTED>2002-06-11T07:34:15</TSTED> \n
\t </DD> \n
\t <FRMT algoritmo=”SHA1withRSA”>GkdhiwT5a4…09UjhGfsR7l/=</FRMT> \n
</TED> \n
El digest (y por lo tanto la firma) se calculan sobre el string:
<DD><RE>11111111-1</RE><TD>33</TD><F>122</F><FE>2002-06-11</FE><RR>12345678-
5</RR><RSR>Empresas A&amp;B Limitada</RSR><MNT>24365</MNT><IT1>Cajón de
Manzanas</IT1><CAF version="1.0"><DA><RE>11111111-1</RE><RS>Ejemplo
S.A.</RS><TD>33</TD><RNG><D>125</D><H>160</H></RNG><FA>2002-05-
14</FA><RSAPK><M>zf/B…cwx</M><E>QBcs</E></RSAPK><IDK>3</IDK></DA><FRMA>yTfHE
...ydmh9fgsj3rv86=</FRMA></CAF><TSTED>2002-06-11T07:34:15</TSTED></DD>
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 21 de 30
Servicio de Impuestos Internos
A.2.5 Reglas Para La Generación e Impresión Del Timbre PDF417
El SII ha establecido las siguientes reglas en la generación e impresión del código PDF417
Impresión del timbre
– Impresora láser o inyección tinta con una resolución mínima de 300 DPI
– Color de impresión: Negro
– Quiet Zone: Para evitar que líneas o textos cercanos al código puedan ser interpretados como
parte de éste, el código debe tener una Quiet Zone (espacio en blanco) de mínimo 0,25 pulgadas
alrededor de cada uno de sus cuatro lados.
– Truncated: Esta opción que permite omitir alguna parte del código, pero que aumenta su
sensibilidad al daño, no debe usarse
Generación del Timbre
– Para evitar problemas con los caracteres especiales que pudiera contener el timbre electrónico,
al generar el código PDF417 se debe utilizar el modo de codificación binario (Byte Compaction
Mode)
– Error Correction Level (ECL): Dada la cantidad de información, se debe utilizar nivel 5.
– X Width (X Dim): Es el ancho del elemento impreso del código, barra o espacio, más angosto y
se expresa en mils (milésimas de pulgada). Se debe usar un valor de X Dim mínimo de 6,7
mils.
– Row Height (Y Dim): Es la dimensión vertical, expresada en mils, de una fila del código
PDF417. Se debe usar una relacion (3:1) respecto al valor X Dim.
– Recomendamos ajustar los parámetros para obtener un codigo de barras impreso de un tamaño
máximo de 3 cms de alto x 9 cms de ancho.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 22 de 30
Servicio de Impuestos Internos
ANEXO 3: Uso de XML en Envíos de Documentos Tributarios
Electrónicos (DTEs).
En el presente ANEXO se hace una breve Introducción descriptiva del XML y se describe en texto
explicativo la siguiente información XML de los documentos.
1. Formato XML y Base64.
2. Envío de DTE: conjunto de Documentos Tributarios Electrónicos que los contribuyentes enviarán
al SII.
3. Carátula de Identificación de un Envío: Resumen de la información enviada al SII, por un
contribuyente, en un Envío de DTE
4. Documento Tributario Electrónico (DTE): Factura Electrónica u otro documento tributario
electrónico generado por un contribuyente autorizado por el SII
5. Timbre Electrónico del DTE: Firma digital que los contribuyentes emisores deben incluir en cada
DTE, para que el SII pueda verificar la validez de la versión impresa.
6. Código de Autorización de Folios (CAF): Información del rango de folios que el SII ha autorizado
a un contribuyente para utilizar en la foliación de los DTEs que emita.
A 3.1. Formato XML y Base64
Al generar el archivo XML se debe insertar saltos de línea al final de cada tag y opcionalmente
indentar los tags. Se debe evitar enviar el archivo XML como un único texto continuo (sin saltos de
línea). Ver ejemplos:
XML con formato correcto XML incorrecto
<IdDoc>
<TipoDTE>33</TipoDTE>
<Folio>1097372</Folio>
<FchEmis>2004-05-04</FchEmis>
</IdDoc>
<Emisor>
<RUTEmisor>77777777-7</RUTEmisor>
<RznSoc>RUT DE PRUEBA</RznSoc>
<GiroEmis>Ventas</GiroEmis>
<Ciudad>Santiago</Ciudad>
</Emisor>
<IdDoc><TipoDTE>33</TipoDTE><Folio>1097372</Folio>
<FchEmis>2004-05-04</FchEmis></IdDoc><Emisor><RUT
Emisor>77777777-7</RUTEmisor><RznSoc>RUT DE PRU
EBA</RznSoc><GiroEmis>Ventas</GiroEmis><Ciudad>
Santiago</Ciudad></Emisor>
En particular, para facilitar el procesamiento de la información recibida, el SII valida que las 2 primeras
líneas del envío contengan el set de caracteres y el schemaLocation, por ejemplo:
<?xml version="1.0" encoding="ISO-8859-1"?> ( línea 1 correcta, contiene el set de caracteres
utilizado: ISO-8859-1)
<EnvioDTE xmlns="http://www.sii.cl/SiiDte" xmlns:xsi="http://www.w3.org/2001/XML Schema-
instance" xsi:schemaLocation="http://www.sii.cl/SiiDte EnvioDTE_v10.xsd" version="1.0">
(línea 2 correcta, contiene el schemaLocation="http://www.sii.cl/SiiDte EnvioDTE_v10.xsd")
Respecto a los campos del tipo Base64, esto es la firma y datos del Certificado (X509 Certificate), de
acuerdo al estándar estas líneas deben tener un máximo de 76 caracteres, debiendo insertarse saltos de
línea según corresponda.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 23 de 30
Servicio de Impuestos Internos
Base64 con formato correcto Base64 incorrecto
<X509Certificate>
MIIEgjCC...AkGA1UEBhMC
Q0wxHTA...QQHFAhTYW50
AWFnbzE...MBIGA1UEChQ
ZXJ0Awz...pY2Fkb3JhMRcw
</X509Certificate>
<X509Certificate> MIIEgj....Rcw</X509Certificate>
A 3.2. Envío de DTE
El conjunto de uno o más documentos tributarios electrónicos a enviar al SII se agruparán en un
mensaje XML con la siguiente estructura:
A.3.3. Carátula de Identificación de un Envío
Junto al grupo de documentos a enviar (EnvioDTE) se debe incluir un resumen de la información
enviada al SII en una carátula o “sobre” que especifica el origen, destino y contenido del envío.
<Caratula version=”1.0”>
<RutEmisor>... </RutEmisor> /* RUT Contribuyente Emisor de los DTE
<RutEnvia>... </RutEnvia> /* RUT Persona que envía los DTE
<RutReceptor>... </RutReceptor> /* RUT Contribuyente Receptor de los DTE
<FchResol>... </FchResol> /* Fecha Resolución SII que autoriza al emisor
<NroResol>... </NroResol> /* Nº de resolución SII que autoriza al emisor
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 24 de 30
Servicio de Impuestos Internos
<TmsFirmaEnv>... </TmsFirmaEnv> /* Fecha y hora de firma del envío
/* en formato AAAAMMDDHHMMSS
<SubTotDTE>... </SubTotDTE> /* Uno o más Subtotales
... /* por tipo de DTE
<subTotDTE>... </SubTotDTE>
</Caratula>
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 25 de 30
Servicio de Impuestos Internos
Subtotal por Tipo de Documentos Enviados
Dentro de la carátula o resumen del envío se especifica el número de cada uno de los documentos
tributarios enviados
<SubTotDTE>
<TipoDTE>... </TipoDTE> /* Tipo de DTE
<NroDTE>... </NroDTE> /* Número de DTE del tipo
/* incluidos en el envio
</SubTotDTE>
A.3.4. Documento Tributario Electrónico (DTE)
Factura Electrónica u otro documento tributario electrónico generado por un contribuyente autorizado
por el SII. Incluye documento propiamente tal y firma del documento completo.
<DTE version=1.0”>
<Documento ID=””>
<Encabezado>... </Encabezado>
<DetalleFactura>... </DetalleFactura>
<DescuentoRecargoGlobal>... </DescuentoRecargoGlobal>
<Referencia>... </Referencia>
<TED>... </TED> /* Timbre Electrónico DTE
<TmstFirma> ... </TmstFirma> /* TimeStamp firma del DTE
</Documento>
<Signature>... </Signature> /* Firma digital sobre
/* <Documento>... </Documento>
</DTE>
El Atributo ID del tag <Documento>, debe corresponder a un identificador único del DTE, por ejemplo
el tipo de documento concatenado con el folio. Este identificador único es referenciado en el atributo
URI del tag <Reference> de la firma electrónica sobre Documento.
Por ejemplo si tenemos el siguiente identificador único para un DTE:
<Documento ID=”F0000000187T33”>
Se le debe referenciar de la siguiente forma en la sección firma:
<Reference URI=”#F0000000187T33”>
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 26 de 30
Servicio de Impuestos Internos
A.3.3.1 Firma Digital del DTE
Todo documento va acompañado de una firma digital del contenido del documento, calculada con la
llave privada de un certificado digital otorgado por una empresa certificadora de identidad acreditada
por el SII.
La firma digital del DTE, así como la del envío de DTE, está basada en el estándar XMLDSIG, pero
con algunas restricciones respecto a la obligatoriedad y a los algoritmos de firma y hash permitidos.
Para validar adecuadamente la firma digital del DTE, el SII requiere que se incorpore la siguiente
información de firma electrónica en cada DTE:
<Signature xmlns="http://www.w3.org/2000/09/xmldsig#">
<SignedInfo>
<CanonicalizationMethod
Algorithm="http://www.w3.org/TR/2001/REC-xml-c14n-20010315" />
<SignatureMethod
Algorithm="http://www.w3.org/2000/09/xmldsig#rsa-sha1" />
<Reference URI="#XXXXX">
<DigestMethod Algorithm="http://www.w3.org/2000/09/xmldsig#sha1" />
<DigestValue>... </DigestValue>
</Reference>
</SignedInfo>
<SignatureValue>... </SignatureValue>
<KeyInfo>
<KeyValue>
<Valores Llave Publica>
</KeyValue>
<X509Data>
<X509Certificate>... </X509Certificate>
</X509Data>
</KeyInfo>
</Signature>
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 27 de 30
Servicio de Impuestos Internos
A.3.3.2 Valores Llave Pública del DTE
Si la llave es RSA
<RSAKeyValue>
<Modulus>... </Modulus>
<Exponent>... </Exponent>
</RSAKeyValue>
Si la llave es DSA
<DSAKeyValue>
<P>... </P>
<Q>... </Q>
<G>... </G>
<Y>... </Y>
</DSAKeyValue>
A.3.3.3. Documentación Adicional.
La descripción detallada del documento propiamente tal, y de su schema XML puede encontrarse en la
Documentación técnica del sistema, en la sección de la Factura Electrónica, de la web del SII
(www.sii.cl).
• Formato De Documentos Electrónicos. Se describen en detalle la estructura y los tipos de datos
que conforman un DTE.
• Formato XML de Documentos Electrónicos. Se incluye el Schema que define el xml de un
DTE.
Más información respecto al estándar de firma digital utilizado, XML Digital Signature, ir a
http://www.w3.org/Signature/
A.3.3.4. Tamaño Máximo de Envíos de Información al SII
Debido a que al momento de recibir la información el SII debe validar tanto el formato XML
del envío así como la firma electrónica sobre el mismo, se ha establecido los siguientes límites
para los envíos de información, que permiten asegurar un óptimo procesamiento de la
información tanto a los emisores como al SII:
• Envío de DTEs: El envío de DTEs puede contener un máximo de 2.000 documentos
• Envíos de Información Electrónica de Compras y Ventas: El Envío de la IEC o de
la IEV puede contener como máximo 30.000 líneas de detalle.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 28 de 30
Servicio de Impuestos Internos
ANEXO 4: Intercambio de Información entre Contribuyentes
Electrónicos
En respuesta a un envío de documentos tributarios, el contribuyente receptor electrónico debe responder
con un comprobante de recepción de envío y, en los casos que corresponda, con un comprobante de
rechazo de documentos. Ambas respuestas, respetando el schema XML que para estos efectos definió el
SII y que se encuentra publicado en su página web.
<RespuestaEnvioDTE>
<Resultado>
<Caratula> /* Identificación del emisor y receptor
<RecepcionEnvio> /*Respuesta al Envio
<RecepcionDTE> /* Respuesta recepción DTE individuales
<ResultadoDTE> /* Respuesta Aceptación/Rechazo DTE individuales
<Signature> /* Firma electrónica sobre la Respuesta
</RespuestaEnvioDTE>
El envío de documentos tributarios entre contribuyentes debe cumplir con lo indicado en la
sección A.3.1 en cuanto a la inclusión de saltos de línea entre tags, al contenido de las 2 primeras
líneas y a evitar enviar el XML como un único texto continuo.
Asimismo, la firma electrónica de un envío de DTEs y la firma electrónica de la respuesta están
basadas en el estándar XMLDSIG, tal como se explica en la sección A.3.3.1
Las etiquetas <RecepcionEnvio> y <ResultadoDTE> son excluyentes, o sea, en una Respuesta sólo se
debe incluir sólo una de ellas.
4.1 Respuesta de Recepción de un envío de DTEs
Esta respuesta se utiliza para dar acuse de recibo de los documentos, pero no implica la aceptación
comercial de dichos documentos. En la misma respuesta al envío es posible detallar la respuesta de
recepción individual por cada DTE, particularmente útil en el caso de Rechazar la recepción de algún
documento en particular.
4.2 Respuesta de Aprobación/Rechazo Comercial de DTEs
Esta respuesta es para detallar la aceptación o rechazo comercial de uno más documentos electrónicos.
El formato de esta respuesta debe indicar los datos del documento y en el caso de Rechazos indicar una
glosa que describa el motivo.
Una descripción completa del formato de intercambio se encuentra en un documento aparte que está
publicada en la web SII. (http://www.sii.cl/factura_electronica/descripcion_formato.htm )
4.3 Reglas para Intercambio de Información entre Emisores Electrónicos
El intercambio de información entre contribuyentes autorizados se efectuará por el medio que las partes
acuerden, sin embargo deberán tener habilitado como mínimo la posibilidad de recibir y enviar
información por e-mail, en formato MIME, con un único archivo adjunto que contenga una Respuesta
de Recepción DTEs, o una Respuesta de Resultado DTE, todos ellos en el formato XML establecido
por el SII.
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 29 de 30
Servicio de Impuestos Internos
SII. Factura Electrónica. Instructivo Emisión Doctos. Versión 15.10.09
Pág. 30 de 30
Cada emisor electrónico tendrá registrada en el SII una casilla de email para recibir las
respuestas de intercambio. Esta información puede ser consultada a través del web SII, en la
Consulta entre Contrayentes Autorizados.
ANEXO 5: Compatibilidad y Restricciones de Uso de Opciones
Habilitadas en la WEB
Para un correcto funcionamiento de las opciones de factura electrónica que el SII ha dejado
disponible en su sitio web, es necesario tener en consideración lo siguiente:
5.1 Navegadores Soportados
Las opciones disponibles en la sección Factura Electrónica y Otros Documentos Electrónicos
de www.sii.cl, han sido probadas con los siguientes navegadores:
• Microsoft Internet Explorer versión 5.5 y 6.0
• Netscape versión 6.0 y 7.0
• Mozilla versión 1.6
Lo navegadores fueron evaluados en los siguientes sistemas operativos: MS Windows 98, NT,
2000 y XP.
5.2 Política de Uso de Web Services
Para facilitar la operación de los contribuyentes autorizados, el SII permite actualmente operar
en forma automática (de computador a computador) con las siguientes funciones:
• Autenticación con certificado digital ante www.sii.cl
• Upload Automático
• Consulta Estado de Envío
• Consulta Estado DTE
El SII se reserva el derecho de suspender unilateralmente, en forma temporal o definitiva, el
acceso a estas funciones ante la detección de cualquier anormalidad que a su parecer
contravenga el uso idóneo y responsable de dichas opciones. En particular, es importante tener
presente que estas opciones no fueron habilitadas para uso masivo y están concebidos
exclusivamente para apoyar la emisión y recepción de documentos tributarios electrónicos
