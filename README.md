# Análisis de Homicidios por Siniestros Viales en CAB

## Introducción
En este proyecto, simulamos el rol de un Data Analyst en el equipo de analistas de datos de una empresa consultora que trabaja para el Observatorio de Movilidad y Seguridad Vial (OMSV) bajo la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires (CABA). Se nos solicitó la tarea de realizar un análisis de datos sobre homicidios en siniestros viales ocurridos en CABA entre 2016 y 2021.

Es tarea fundamental brindar información que permita a las autoridades locales tomar medidas para reducir la cantidad de víctimas fatales en accidentes de tráfico. Se entregará un informe detallado de las tareas realizadas, las metodologías adoptadas y las conclusiones clave. Además, se creará un dashboard interactivo para facilitar la interpretación de los datos y su análisis.

## Contexto
Los incidentes viales, también denominados incidentes de tráfico, siniestros viales o accidentes de tránsito, representan situaciones donde vehículos se ven involucrados en espacios públicos. Estos eventos pueden generarse por diferentes situaciones, como colisiones entre automóviles, motocicletas, bicicletas o peatones, atropellos, impactos contra objetos fijos o incluso caídas de vehículos. Las consecuencias abarcan desde daños materiales hasta lesiones graves o, lamentablemente, la muerte para los involucrados. Los siniestros viales son una preocupación importante en la Ciudad Autónoma de Buenos Aires debido al alto volumen de tráfico y la densidad poblacional. La población de CABA corroborada en el último censo realizado (2022) es de 3,120,612 habitantes en una superficie de 200 km².

## Datos
Se trabajó con la Base de Víctimas Fatales en Siniestros Viales en formato Excel, que contiene dos pestañas de datos: "HECHOS" y "VICTIMAS". Estas incluyen información sobre los eventos, víctimas, edad, sexo, modo de desplazamiento, etc. El análisis se basó en la exploración y limpieza de datos utilizando Python y Pandas.

## Tecnologías Utilizadas
Python y Pandas se emplearon para la extracción, transformación y carga ETL de datos. Para el análisis exploratorio de datos EDA se utilizaron librerías como Seaborn, Matplotlib, numpy y pandas. Por último, para la creación del dashboard se utilizó PowerBi.

## Proceso de trabajo
### ETL y EDA
Se realizó un proceso ETL para estandarizar nombres de variables, analizar y eliminar nulos y duplicados así como columnas redundantes. Posteriormente, se llevó a cabo un análisis exploratorio para identificar patrones y tendencias que ayuden a tomar medidas preventivas.

### Análisis de los Datos
El análisis integral de los datos sobre siniestros viales en la Ciudad Autónoma de Buenos Aires (CABA) revela patrones y tendencias significativas:

#### Datos Generales:
- El conjunto de datos cuenta con 707 registros y 25 columnas, proporcionando información detallada sobre accidentes, víctimas, ubicación y detalles temporales.

#### Características Temporales:
- Los accidentes parecen distribuirse de manera relativamente uniforme a lo largo de los años, meses y días, con un promedio de 1.06 víctimas por incidente.
- Analizando cada año en particular, el 2020 fue un año donde disminuyó mucho la tasa de siniestros viales, esto puede ser consecuencia de la cuarentena impuesta por las autoridades en base a la pandemia de COVID-19.

#### Ubicación y Franja Horaria:
- La mayoría de los accidentes ocurren en las franjas horarias de 6:00 a 12:00 y de 18:00 a 24:00 horas, y la Comuna 1 es la más afectada.
- Las avenidas son escenarios comunes de accidentes, representando el 62% de las víctimas, con un pico los sábados.

#### Edad:
- La edad promedio de las víctimas es de aproximadamente 42 años.
- La mayoría de las víctimas tienen edades comprendidas entre 20 y 40 años, destacando la importancia de dirigir estrategias de seguridad vial a este grupo.

#### Género:
- El 76.6% de las víctimas son masculinas, siendo este género predominante en todos los roles, ya sea conductor, pasajero o peatón.

#### Roles y Responsabilidad:
- El 48% de las víctimas desempeñaba el rol de conductor, principalmente en motos.
- Los conductores de automóviles, colectivos y camiones son responsables en el 75% de los casos donde se señala un vehículo como responsable.

#### Distribución Espacial:
- La alta frecuencia de accidentes en avenidas en la mayoría de las comunas de la Ciudad Autónoma de Buenos Aires indica posibles áreas críticas con alto flujo vehicular y, por ende, mayores riesgos de siniestros viales.

#### Patrones Temporales:
- Se observa un aumento en la cantidad de accidentes en diciembre.
- Los picos de accidentes en diferentes meses varían en distintos años. Aunque se puede observar un patrón anual en la distribución de incidentes, destacando un pico significativo en diciembre, este mes experimentó la mayor cantidad de incidentes. Contrastando con esta tendencia, abril surge como el mes con la menor cantidad de incidentes registrados. Este análisis revela una tendencia general de disminución gradual de incidentes desde enero hasta abril, seguida de un aumento constante en los meses de mayo, junio, agosto y noviembre.

#### Relación entre Víctimas y Acusados:
- Las motos son frecuentes víctimas pero raramente acusadas. Los autos, por otro lado, son comunes en ambos roles.

Este análisis integral proporciona una visión completa de la problemática de los siniestros viales en la Ciudad Autónoma de Buenos Aires.

## KPI (Indicadores Clave de Rendimiento)
En el marco del análisis de los siniestros viales y con el objetivo de reducir la cantidad de víctimas fatales, se han definido dos Indicadores Clave de Rendimiento (KPI) que abordan aspectos específicos de la seguridad vial en CABA. Para poder realizar el análisis de los indicadores se crearon Tablas para facilitar dicho proceso.

### KPI 1 - Métrica de Seguridad en Accidentes Vehiculares:
La métrica de seguridad en accidentes vehiculares se configura como un indicador esencial, evaluando el número de víctimas fatales en incidentes de tráfico por cada 100,000 habitantes durante un semestre. La meta consiste en reducir esta métrica en un 10% en el segundo semestre de 2021 en comparación con el primer semestre. El análisis demuestra que al alcanzar una métrica de 1.35, se superó con éxito el objetivo de disminuir en un 10% la tasa de fatalidades, ya que la métrica previa era de 1.73, logrando así una reducción del 22.22%.

### KPI 2 - Incidentes Mortales Involucrando Motociclistas:
El segundo KPI se encarga de supervisar la cantidad de incidentes mortales relacionados con motociclistas. El propósito es reducir en un 7% la cantidad de accidentes mortales de motociclistas durante el último año. No obstante, los resultados indican un aumento del 79.21% en la cifra de fallecimientos de motociclistas en 2021, señalando la necesidad de estrategias adicionales. Es importante tener en cuenta que el año 2020 estuvo marcado por una pandemia y restricciones de movimiento, lo cual impactó la circulación en las calles.

En resumen, es menester ajustar las estrategias existentes y desarrollar nuevas iniciativas para hacer frente a los desafíos identificados por los KPI.

## Reflexiones
### Contextualización de Datos Temporales:
La observación detallada de los datos revela que el año 2020 presenta una disminución significativa en la tasa de siniestros viales, atribuible a las restricciones implementadas durante la cuarentena por la pandemia de COVID-19.

### Roles y Edades de las Víctimas
El grupo de edad entre 20 y 40 años es particularmente vulnerable. Es esencial dirigir las estrategias de seguridad vial específicamente a este segmento de la población para lograr un impacto significativo.

## Sugerencias
### Monitoreo Activo en Diciembre:
Dada la tendencia anual de aumento en diciembre, intensificar las medidas de seguridad y aplicación de la ley durante este mes.

### Participación Comunitaria Continua:
Establecer canales de retroalimentación y colaboración puede fortalecer las iniciativas de seguridad vial.

### Análisis Continuo de Datos:
Establecer un sistema de análisis continuo de datos para detectar patrones emergentes y ajustar estrategias según la evolución de la situación.

