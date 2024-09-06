# Proyecto de Limpieza y Análisis de Datos

## Descripción del Proyecto

Este proyecto consistió en la limpieza, análisis exploratorio y visualización de dos bases de datos: 

1. **Customer Flight Activity**: Información sobre la actividad de vuelo de los clientes.
2. **Customer Loyalty History**: Información detallada sobre el perfil de los clientes, incluyendo su estado civil, género, salario, nivel educativo, entre otros.

## Pasos Realizados

### 1. Limpieza de Datos

- **Datos Nulos**: Se identificaron y trataron valores nulos en columnas clave.
  - En las columnas `Cancellation Month` y `Cancellation Year`, los valores nulos fueron imputados con la constante `"None"`, ya que se consideró que estos valores nulos representaban clientes que no habían cancelado su membresía.
  
- **Salarios Negativos**: Se identificaron y eliminaron las filas que contenían valores negativos en la columna `Salary`, ya que estos valores eran inconsistentes con la realidad y podían distorsionar el análisis.
  
- **Imputación de Datos Faltantes**: Para los valores nulos en la columna `Salary`, se decidió imputar los datos utilizando el método `KNNImputer`, que toma como referencia los valores de los vecinos más cercanos para completar los datos faltantes.

### 2. Análisis Exploratorio de Datos (EDA)

Se realizó un EDA exhaustivo para entender mejor las características de los datos, identificar patrones y posibles relaciones entre las diferentes variables.

### 3. Unión de las bases de datos

Se realizó la unión de las dos bases de datos de acuerdo a las instrucciones de la evaluación a través de un merge. 

### 4. Visualizaciones de Datos

Para facilitar la interpretación de los datos y sus relaciones, se crearon varias visualizaciones, que incluyen gráficos de distribución, gráficos de dispersión, boxplots y gráficos de barras, entre otros. Estas visualizaciones ayudaron a identificar patrones entre las distintas variables del dataset.

### 5. Evaluación de diferencias

Para saber si existe una diferencia significativa en la cantidad de vuelos reservados segun el nivel educativo

## Librerías Utilizadas

- **Pandas**: Para la manipulación y limpieza de los datos.
- **Seaborn** y **Matplotlib**: Para la creación de visualizaciones.
- **Scikit-learn**: Para la imputación de datos nulos usando el `KNNImputer`.
- **SciPy**: Para pruebas estadísticas y análisis.

## Los Datos

### Customer Flight Analysis.csv

Este archivo contiene información sobre la actividad de vuelo de los clientes, incluyendo el número de
vuelos reservados, la distancia volada, puntos acumulados y redimidos, y costos asociados a los puntos
redimidos

- Loyalty Number: Este atributo representa un identificador único para cada cliente dentro del programa de lealtad de la aerolínea. Cada número de lealtad corresponde a un cliente específico.
- Year: Indica el año en el cual se registraron las actividades de vuelo para el cliente.
- Month: Representa el mes del año (de 1 a 12) en el cual ocurrieron las actividades de vuelo.
- Flights Booked: Número total de vuelos reservados por el cliente en ese mes específico.
- Flights with Companions: Número de vuelos reservados en los cuales el cliente viajó con
acompañantes.
- Total Flights: El número total de vuelos que el cliente ha realizado, que puede incluir vuelos
reservados en meses anteriores.
- Distance: La distancia total (presumiblemente en millas o kilómetros) que el cliente ha volado
durante el mes.
- Points Accumulated: Puntos acumulados por el cliente en el programa de lealtad durante el mes,
con base en la distancia volada u otros factores.
- Points Redeemed: Puntos que el cliente ha redimido en el mes, posiblemente para obtener
beneficios como vuelos gratis, mejoras, etc.
- Dollar Cost Points Redeemed: El valor en dólares de los puntos que el cliente ha redimido durante el mes.


### Customer Loyalty History.csv

Este archivo proporciona un perfil detallado de los clientes, incluyendo su ubicación, nivel educativo,
ingresos, estado civil, y detalles sobre su membresía en el programa de lealtad (como el tipo de tarjeta,
valor de vida del cliente, y fechas de inscripción y cancelación).

- Loyalty Number: Identificador único del cliente dentro del programa de lealtad. Este número permite
correlacionar la información de este archivo con el archivo de actividad de vuelos.
- Country: País de residencia del cliente.
- Province: Provincia o estado de residencia del cliente (aplicable a países con divisiones provinciales o estatales, como Canadá).
- City: Ciudad de residencia del cliente.
- Postal Code: Código postal del cliente.
- Gender: Género del cliente (ej. Male para masculino y Female para femenino).
- Education: Nivel educativo alcanzado por el cliente (ej. Bachelor para licenciatura, College para
estudios universitarios o técnicos, etc.).
- Salary: Ingreso anual estimado del cliente.
- Marital Status: Estado civil del cliente (ej. Single para soltero, Married para casado, Divorced para
divorciado, etc.).
- Loyalty Card: Tipo de tarjeta de lealtad que posee el cliente. Esto podría indicar distintos niveles o
categorías dentro del programa de lealtad.
- CLV (Customer Lifetime Value): Valor total estimado que el cliente aporta a la empresa durante
toda la relación que mantiene con ella.
- Enrollment Type: Tipo de inscripción del cliente en el programa de lealtad (ej. Standard).
- Enrollment Year: Año en que el cliente se inscribió en el programa de lealtad.
- Enrollment Month: Mes en que el cliente se inscribió en el programa de lealtad.
- Cancellation Year: Año en que el cliente canceló su membresía en el programa de lealtad, si aplica.
- git Cancellation Month: Mes en que el cliente canceló su membresía en el programa de lealtad, si aplica.