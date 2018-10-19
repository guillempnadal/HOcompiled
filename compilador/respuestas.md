1. Respondido antes de compilar. Paso 1 (pre-procesador): va a agregar las líneas de código de calculator.h a calculator.c. Paso 2 (compilación I): va a traducir el código a assembler. Paso 3 (compilación II): va a traducir de assembler a binario. Paso 4 (linkeo): va a construir un archivo ejecutable a partir del codigo binario.

2. Agregó las líneas de código de calculator.h, pero como éstas incluían un #include stdio.h, también agregó todas las líneas de código de stdio.h.

3. Primero se define la funcion main. En la definicion se llama ("call") a las funciones add_numbers y printf. Después se define la función add_numbers. Printf no se define.

4. En la posición de memoria 000000000000003f tenemos la función add_numbers, que está definida (T). En la posición 0000000000000000 tenemos la función main, también definida (T). Y sin posición de memoria, porque no está definida (U), tenemos la función printf. Todas estas funciones son accesibles desde afuera (T, U mayúsculas): cuando linkee este archivo, todo el conjunto de cosas que acceden al archivo van a tener acceso a estas funciones.

5. En el ejecutable, la función printf sigue sin estar definida, pero aparece @@GLIBC_2.2.5, que indica que hay que ir a buscar esa fucnión a la librería GLIBC_2.2.5. El linker por sí solo se dio cuenta de esto.





