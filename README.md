## Herramientas

Para realizar este análisis se usaron las siguientes librerías:

*   Pandas
*   Matplotlib
*   Seaborn
*   Numpy

## Introducción

El propósito de este informe es hacer un análisis para identificar la perdida de clientes. Para ello se usaran las técnicas que se mostraron en el módulo que ayudaran a detectar patrones claves y diseñar estrategias que sean efectivas para la retención de los clientes.

## Limpieza y Tratamiento de Datos

Primero se exportó el set de datos, el cual es un archivo JSON que está alojado en el link de GitHub que se definió en la variable '**url**'. Después se pasó a la función '**read_json**' y se almacenó en la variable 'datos' para su manipulación.

Para asegurarnos que el set de datos este listo para ser trabajado se tiene que realizar un tratamiento para que al analizarlo no se presente ninguna incoherencia o inconsistencia. Esta lista contiene los pasos que se llevaron a cabo:

*   Se normalizaron los datos en las columnas que tienen la información anidada y se concatenó en un nuevo DataFrame nombrado '**datosNormalizado**'.
*   Se verifica que no haya valores nulos en las columnas para evitar que afecte la precisión del análisis.
*   Se cambiaron los nombres de las columnas y su tipo para que sea más accesible y fácil de entender.
*   Se verifica que no haya ningún cliente duplicado, ya que el id es único.
*   Se crea una columna adicional para los cargos diarios. Se tomó la columna de cargos mensuales y se dividió entre 30 para obtener el valor diario.
*   Finalmente se guardó el set de datos procesados en un CSV.

## Análisis Exploratorio de Datos

Despues de realizar el analisis del set de datos sobre la evasion de clientes, estos son algunos de los graficos relevantes que se obtuvieron que ayudaron a detectar patrones sobre la evasion:

1. Evasion por contrato: <br><img src="https://drive.google.com/uc?id=1yHZwJDcABD6HvNNVVo_Pi81LhYPbzyP7" width="500"><br>
Se puede observar que los clientes que tienen contratos mensuales suelen ser lo que abandonan y para los de un año a dos se reduce.
2. Evasion por metodo de pago: <br><img src="https://drive.google.com/uc?id=1Bzko9_TeKrW1PSYpk-amSErdDhGpYRyF" width="600"><br>
Se observa que los clientes con metodo de pago por transferencia, tarjeta de credito y por correo se mantienen vigentes. Por otro lado, los clientes con cheques electronicos abandonan.
3. Evasion por servicio de internet: <br><img src="https://drive.google.com/uc?id=15hq820-IrrozrQ2LaW6A5S4weCd9F9LB" width="600"><br>
Al observar la grafica se puede ver que hay una gran cantidad de abandonos al usar el servicio de fibra optica, es decir, la gente se siente mas comoda con el servicio de internet DSL.
4. Evasion de clientes por tiempo de contrato: <br><img src="https://drive.google.com/uc?id=1TszXLVqqPlNq5ZlHp5zsRqrdue26AZ4s" width="600"><br>
Al analizar el tiempo de contrato se puede ver que los clientes antes de los 12 años tienden a abondonar. Despues del año se reduce lo que muestra mayor fidelidad.
5. Evasion de clientes por cargos totales: <br><img src="https://drive.google.com/uc?id=1jN8LoBDPIJp9IaG315fjHswl9jL5VaIc" width="600"><br>
Se puede observar que hay una gran concentración de clientes que se fueron con un cargo total muy bajo, cercano a 0, lo cual puede indicar que abandonaron poco después de empezar el servicio.

## Conclusiones e Insights

Se puede concluir que:

*   Los clientes muestran mayor fidelidad en contratos mayor a un año.
*   Los clientes prefieren los métodos de pago por transferencia, pago con crédito y por correo.
*   Los clientes prefieren el servicio de internet DSL.
*   Los clientes con un tiempo de contrato menor a 12 meses tienden a abandonar.
*   Los clientes suelen abandonar poco después de empezar el servicio.

## Recomendaciones

Después de terminar con el análisis se recomiendan las siguientes estrategias:

1.   Mejorar los contratos anuales con beneficios y descuentos.
2.   Implementar promociones de paquetes de internet con el servicio DSL.
3.   Implementar ideas para retener a los clientes vigentes con tiempo de contrato menor a 12 meses.
4.   Eliminar el uso de cheques electrónicos e implementar el uso de pagos por transferencia y con crédito.
5.   Agregar programas de fidelización para clientes con antigüedad.
