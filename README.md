# Análisis de las variables que influyen en grado de abandono de una compañía
## 1. Introducción
Las empresas actuales disponen de infinidad de datos de sus empleados, pero en muy pocas ocasiones son capaces de analizarlos para mejorar tanto la productividad de dichos empleados como, reducir el porcentaje de abandono y lo mas importante, mejorar el bienestar de todos os trabajadores. Se pasa mucho tiempo al día en las oficinas y trabajando con los compañeros. El poder analizar como van evolucionando los indicadores mas relevantes hace que las empresas puedan anticiparse a ciertas situaciones e implementar mediadas por el bien de todos los empleado y el beneficio de la compañía.

Podemos considerar que todas las compañías tienen cuatro tipos de datos sobre los empleados:
* *Datos Personales*: Se trata de datos personales de cada empleado. Por lo general son datos públicos que el empleado puede facilitar para dichos estudios.
* *Datos Profesionales*: Los datos profesionales son aquellos que el empleado facilita al incorporarse en la compañía y periódicamente suele actualizar el departamento de Recursos Humanos.
* *Datos Económicos*: Realmente son datos profesionales, pero dada la importancia en este tipo de análisis los trataremos como un grupo aparte.
* *Datos de Satisfacción y desempeño*: Los datos de evaluación, muchas veces son los mas interesantes, porque muestra mediante encuestas y formularios la valoracion o grados de satisfacción de los empleados o sus responsables.

Para el presente estudio vamos a partir de un Dataset obtenido de la plataforma kaggle. Este Dataset lo elaboraron empleados de IBM para poder realizar estudios a nivel estadísticos. No se trata de datos reales, con lo que la conclusiones no representarán ninguna conclusión real de ningún tipo o grupo de compañía. Tan solo se quiere mostrar el potencial que tienen estas herramientas para poder analizar dichos datos.
A continuacion se irá describiendo las acciones realizadas en cada una de las fases del proyecto que estarán realizadas sobre Notebook de Jupyter:

## 2. Carga y tratamiento del Dataset
El en proceso de carga del Dataset, se realizará la carga y se realizará las modificaciones necesarias para adaptalos a las necesidades del proyecto y orientado a poder disponer de un Dataset de los datos de los empleados de una compañía del sector de las TIC española.

A continuación se muestran las variables de las que disponemos para poder realizar el análisis de los datos.

| Datos Personales | Datos Profesionales | Datos Económicos| Datos de Satisfacción y desempeño|
| --- | --- |--- |--- |
| *Edad* | *Titulación* |*Ingresos mensuales* |*ParticipacionLaboral* |
| *Distancia a casa* | *Especialización* | *Tarifa hora* |*Conciliacion-Laboral-Personal* |
| *Género* | *Puesto*| *Tarifa mes* |*Calificación Desempeño* |
|  | *Departamento* | *Horas extra* | *Satisfacción General* |
|  | *Rol laboral* | *Porcentaje aumento salario* | *Satisfacción Personal* |
|  | *Antigüedad empresa* | *Nº Reparto acciones* | *Satisfacción Laboral* |
|  | *Antigüedad puesto* | |*Abandono*|
|  | *Frecuencia Viajes* | |
|  | *Años trabajados* | |
|  | *Empleos anteriores* | |
|  | *Formacion año anterior* | |
|  | *Años sin promoción* | |
|  | *Años Jefe actual* | |

## 3. Exploración y Análisis de datos
La explotación y análisis de datos se contempla desde los siguientes enfoques:
- Análisis general de las variables por grupos.
- Análisis de datos estadísticos.
- Análisis del grado de correlación.
- Análisis de distribución de valores.
- Análisis de distribución de conjunto de datos
- Análisis de variables de alto impacto
  - Composición de los empleados de la compañía.
  - Porcentaje de igualdad de género y análisis de retribución.
  - Relación de la formación y experiencia con el desempeño.
  - Análisis del grado de abandono

El resumen de las conclusiones mas importantes a las que se ha llegado en esta fase de exploración y análisis de los datos del DataSet utilizado son las siguientes:

- Plantilla con empleados jóvenes y con bastante experiencia y formación.
- El grado de satisfacción de los empleados es bastante alto.
- Los aumentos salariales son altos (11-25 % anuales).
- las promociones de puestos son anuales, de media.
- Igualdad de género: Aunque existe un cierto equilibrio en la distribición de género de los empleados de la compañía, a medida que el puesto es mas alto va descendiendo el porcentaje de mujeres. 
- Porcentaje de Abandono: El porcentaje de abandono se produce en empelados con poca edad (18-23) y con sueldos bajos. Los puestos mas afectados por el abandono son los de administración y técnicos.
- La Distribución de los ingresos no parece la adecuada ya que hay un grupo de empleados con sueldos muy bajos, mientras que el resto de los empleados de la compañía disfrutan de sueldos altos con incrementos salariales periódicos y elevados.

## 4. Análisis avanzado de datos
En el notebook TFM3 se realizará un análisis avanzado de datos en el que se tratan los siguinetes puntos:
- Relación edad, ingresos mensuales y grado de abandono.
- Modelado (Técnica sobremuestreo)
- Análisis de Varianza (ANOVA)
Tras el análisis avanzado de datos pudimos obtener las siguinetes conclusiones:

- Analizando la entropía podemos observar que en el caso de los ingresos mensuales la entropía es menor que en el caso de la edad. Por este motivo podemos considerar que el grado de abandono está mas relacionado con la edad que con los Ingresos mensuales.
- Tras entrenar el dataset con varios modelos obtenemos que el modelo rbfSVM es el que tiene mayor precisión y recall.
- Con el análisis de la varianza podemos observar que las variables Años trabajados e Ingresos mensuales son las que mas relacionadas están con el porcentaje de abandono.

## 5. Entornos de desarrollo
- Lenguaje de programación:  python 3
- Entono de desarrollo interactivo: IPython Notebook
- Entorno de desarrollo: google colaboratory
- Entorno de validación: Maquina virtual facilitada por Kschool

