# TechNova-Cloud-v2.0
## 1. ¿Cuántas líneas de código habéis ahorrado al usar grupos?
Como se ha mplementado el xs:attributeGroup para id, rack, estado un xs:group he conseguuido ahorrar 12 líneas de código. Ya no se repite "servidor" y solo se añade una vez. Al añadir xs:attributeGroup, se invoca a todo el bloque.
## 2. ¿Qué error os da VS Code si intentáis poner dos servidores con el mismo ID?
Si se intenta duplicar un id en el XML, el validador de VS Code mostrará un error de tipo Sintáctico/Semántico parecido a este:

"There is a duplicate key sequence 'srv-web-01' for the 'ID_Servidor_Unico' key identity constraint."
(Existe una secuencia de clave duplicada 'srv-web-01' para la restricción de identidad).

O si usamos el tipo xs:ID estándar de XML:

"The ID 'srv-web-01' is already defined."

Esto sucede porque el procesador XML crea una tabla de símbolos en memoria y detecta la colisión antes incluso de terminar de leer el documento.
