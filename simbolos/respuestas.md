Compilamos el objeto visibility.o, y después ejecutamos nm visibility.o. Nos aparecen los siguientes símbolos, que voy describiendo uno por uno.

0000000000000000 t add_abs  

En la posición 000... está definida la función add_abs, no accesible desde afuera.

000000000000002a T main 

En la posición ...0002a está la función main, accesible.

(Sin posición de memoria) U printf   

La función printf no está definida.

0000000000000000 r val1    

En la posición 000... está definida la constante val1, no accesible desde fuera.

0000000000000004 R val2

Val2 es una constante sí accesible desde fuera.

0000000000000000 d val3 

Val3 es una variable no accesible desde afuera.

0000000000000004 D val4

Val4 es una variable sí accesible desde afuera.

