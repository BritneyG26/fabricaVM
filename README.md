# Fábrica de chocolate
### Introducción

La máquina virtual de chocolate es una simulación de los porcesos fundamentales para producir chocolate. Este sistema virtual permite simular la gestión de ingredientes principales como el cacao en polvo, leche en polvo, azúcar, manteca de cacao e ingredientes adicionales como almendras, avellanas, etc. 

El objetivo de la máquina es procesar diferentes ingredientes de manera secuencial para crear productos como chocolate con leche y avellanas o chocolate negro con naranja, entre otros. 

Esta máquina permite la simulación paso a paso del proceso productivo de una fábrica de chocolate, reflejando el estado actual de los ingredientes, y garantizando que se mantengan actualizados después de cada operación.


### Estructura del código
El código está estructurado en una clase llamada FabricaChocolate. En ella se definen los atributos que vendrían representando los tanques con los ingredientes principales para hacer chocolate y la cantidad que hay en cada tanque. 

![Codigo](https://github.com/BritneyG26/fabricaVM/blob/main/cap1.png)

- Funcion procesar_instrucciones:
  
La función recibe una línea de texto que representa una instrucción.

\- Se verifica si la instrucción contiene la palabra "añadir" y si la encuentra se llama al método añadir_ingrediente con la cantidad y el ingrediente.

\- Si encuentra la palabra "crear" se llama al método mezclar_ingredientes, que se encarga de mezclar los ingredientes.

\- Si se encuentra la palabra "cantidad" se actualiza la cantidad de chocolate producido, suamndo la cantidad especificada.

![Codigo](https://github.com/BritneyG26/fabricaVM/blob/main/cap2.png)

- Función añadir_ingredientes

Esta función se encarga de gestionar la adición de distintos ingredeintes a la máquina de chocolate. 
La función evalúa el tipo de ingrediente que se quiere añadir utilizando la condicional if.

Hay diferentes secciones para cada ingrediente:
1. Cacao en polvo donde comprueba si hay cacao en polvo disponible y si hay suficiente, se resta la cantidad utilizada. Si no hay, pone Error.
2. Lo mismo pasa con la leche en polvo, azúcar y manteca de cacao. Cada ingrediente tiene su porpia sección que verifica la disponibilidad y realiza la resta.
3. Ingredientes adicionales donde si el ingrediente no coincide con ningunon de los tipos anterioires, se considera como un ingrediente adicional. Comprueba si hay la cantidad suficiente y realiza la resta. Si no hay, pone Error.

![Codigo](https://github.com/BritneyG26/fabricaVM/blob/main/cap3.png)

- Función ejecutar

Esta función es el núcleo operativo de la máquina de chocolate. Se encarga de iniciar la máquina, porcesar instrucciones del archivo de texto y generar log de todas las acciones realizadas. Puede verse como el ciclo de procesamiento que recibe las intrucciones y las ejecuta de manera secuencial, como si estuviera desapilando las intrucciones hasta que no quede ninguna.

![Codigo](https://github.com/BritneyG26/fabricaVM/blob/main/cap4.png)

Al final, la máquina porcesa todas las instrucciones y actualiza los refistros que quedan disponibles.

![Codigo](https://github.com/BritneyG26/fabricaVM/blob/main/cap5.png)

### Funcionamiento de la máquina virtual 

La máquina virtual sigue un flujo de trabajo automatizado:
1. Lectura de intrucciones. La máquina toma las instrucciones desde un archivo de texto. Este archivo contiene líneas de texto que especifican tanto los ingredientes a añadir como las acciones a realizar y la creación de chocolate de un tipo específico. Cada línea es interpretada y procesada de manera secuencial, simulando las operaciones de una fábrica real.
2. Procesamiento de ingredientes. Según las intrucciones de entrada, la máquina extrae los ingredientes necesarios de sus tanques. Para cada ingrediente solicitado, la máquina verifica si hay suficiente cantidad disponible en el inventario. Si hay, la cantidad es descontada del total.
3. Producción de chocolate. Cuando se reciben las instrucciones de creación, la máquina mezcla los ingredientes necesarias para el tipo de chocolate solicitado (como chocolate negro o chocolate con leche).
4. Control de inventario. La máquina lleva un registro de la cantidad de cada ingrediente después de cada operación, actualizando el inventarioy generando un informe al final.
5. Registro de actividad. La máquina genera un registro detallado de cada paso, que incluye los ingredientes añadidios, la cantidad de chocolate porducido y cualquier mensaje de error por falta de ingredientes.

Con esto, se permite el funcionamiento de la máquina para que actúe de manera automática, simulando un entorno de producción de chocolate en una fábrica.











