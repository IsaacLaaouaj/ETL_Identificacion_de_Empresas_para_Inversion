Isaac Mohamed Laaouaj Madrouni 

1. Explicación y justificación de valores a escoger 

Como alumno analizando un conjunto de datos de empresas, mi objetivo es identificar compañías  destacadas  según  ciertos  criterios  financieros  y  operativos.  Aquí  está  mi razonamiento para seleccionar valores específicos de las columnas del dataset: 

**Ticker y Company**: Estos son datos básicos que identifican a cada empresa. El 'Ticker' es el símbolo único de la acción en el mercado de valores, mientras que 'Company' es el nombre de la empresa. Ambos son esenciales para cualquier análisis posterior. 

**Exchange** Indica en qué bolsa de valores se negocia la acción. Es útil para entender en qué mercado opera principalmente la empresa y bajo qué regulaciones financieras se encuentra. 

**Industry**: Saber la industria permite entender el contexto del negocio de la empresa, sus competidores y los desafíos del mercado en el que opera. 

**Zen Score**: Si es un indicador compuesto del rendimiento de la empresa, podría dar una rápida idea de su salud general y eficiencia operativa. 

**Market Cap** (Capitalización de Mercado): Nos proporciona una medida del tamaño total de la empresa en el mercado. Las empresas con una alta capitalización de mercado suelen ser más estables y seguras para invertir. 

**Price y 1d %**: El precio actual de la acción y su cambio porcentual en un día nos dice una visión de la actividad reciente del mercado para esa acción. 

**EBITDA**:  Este  indicador  (Ganancias  antes  de  intereses,  impuestos,  depreciación  y amortización) muestra la rentabilidad operativa de la empresa antes de ciertas deducciones contables y financieras. 

**P/E Ratio** (Price to Earnings Ratio): Muestra cuánto están dispuestos a pagar los inversores por  cada  dólar  de  ganancias.  Un  P/E  bajo  puede  indicar  una  acción  subvalorada  (o problemas  en  la  empresa),  mientras  que  un  P/E  alto  puede  indicar  expectativas  de crecimiento futuro. 

**D/E Ratio** (Debt to Equity Ratio): Muestra la proporción de financiamiento de la empresa a través  de  deuda  versus  capital  propio.  Un  ratio  alto  puede  indicar  un  alto  nivel  de endeudamiento. 

**EPS** (Earnings Per Share): Es una medida directa de la rentabilidad de la empresa. Un EPS positivo indica ganancias, y cuanto mayor sea el número, más rentable es la empresa. 

**Employees**: El número de empleados puede dar una idea del tamaño de la empresa y su capacidad operativa. 

**Foundation**: La fecha de fundación puede dar una idea de la madurez y estabilidad de la empresa.  Las  empresas  más  antiguas  pueden  tener  más  experiencia  y  recursos,  pero también pueden enfrentar desafíos de modernización. 

Al  analizar  estos  datos,  busco  empresas  que  sean  estables,  rentables  y  con  buena perspectiva  de  crecimiento.  Por  ejemplo,  prefiero  empresas  con  un  P/E  bajo,  pero  no demasiado  bajo,  un  EPS  positivo,  y  una  capitalización  de  mercado  considerable.  La diversificación en diferentes industrias también es clave para mitigar riesgos específicos del sector. 

2. Extracción de datos 

Para la extracción de los datos financieros se han utilizado: 

- [www.wallstreetzen.com:](http://www.wallstreetzen.com/) Para valores del Ticker,Company, Exchange, Industry, Zen Score, Market Cap, Price, 1d %, EBITDA, P/E, D/E, mediante “web scraping” con la herramienta de Selenium y BS: 

![](Aspose.Words.b64a2492-d145-4216-9d5f-0c3f97139980.002.png)

Para ello se ha tenido que iterar página por página mediante Selenium y BeautifulSoap. Además he tenido que añadir un tiempo random de entre 2 a 5 segundos para prevenir que la página me bloquee. 

![](Aspose.Words.b64a2492-d145-4216-9d5f-0c3f97139980.003.png)

Y la data frame saliente ha sido el siguiente: 

![](Aspose.Words.b64a2492-d145-4216-9d5f-0c3f97139980.004.png)

- Google finance: Para el año de fundación y el número de empleados a través de Selenium. 
3. Cálculo del EPS 

El "EPS" o Earnings Per Share (Ganancias por Acción) es una medida de la rentabilidad de una empresa y se calcula dividiendo las ganancias netas de la empresa por el número total de acciones en circulación. 

Para calcular el EPS directamente, necesitamos conocer las ganancias netas de la empresa y el número total de acciones en circulación. Pero como ya tenemos el P/E ratio y el precio por acción, podemos calcular el EPS utilizando esta fórmula: 

EPS = Precio por acción / PE ratio 

![](Aspose.Words.b64a2492-d145-4216-9d5f-0c3f97139980.005.png)

De  esta  forma  ya  tenemos  la  parte  del  beneficio  neto  total  de  una  compañía  que  le corresponde a cada una de las acciones que constituyen su capital social. 

4. Justificación de las 10 mejores empresas para invertir 

Después de filtrar las empresas según: 

- Que sea de creación posterior al año 2000 
- Que haya pagado dividendos alguna vez en los últimos años 
- Que, actualmente, tenga un PER (Price To Earnings Ratio) inferior a 30 
- Que, actualmente, tenga beneficio por acción (EPS, Earnings Per Share) positivo. 

He decidido que en base a la información que tenemos, hay que escoger en base a: 

**Market Cap**: Priorizamos la capitalización de mercado porque proporciona una evaluación rápida del tamaño y la influencia de una empresa en su sector. Las empresas con una gran capitalización de mercado suelen tener una mayor estabilidad y poder en sus respectivos mercados. 

**P/E Ratio**: Usamos el P/E Ratio como un filtro para asegurarnos de que las empresas seleccionadas no solo son grandes, sino que también están valoradas de manera razonable en relación con sus ganancias. 

**EPS**: Al considerar solo empresas con un EPS positivo, nos aseguramos de que las empresas seleccionadas sean rentables, lo que es un indicador clave de salud financiera. 

**Zen Score**: Si esta métrica proporciona una visión general del rendimiento y la salud de una empresa, incluirla en nuestro análisis refuerza la selección, ya que consideramos un indicador compuesto además de las métricas financieras individuales. 

Este enfoque nos asegura escoger lo mejor de la empresa en (Market Cap), su valoración (P/E Ratio), rentabilidad (EPS) y un indicador compuesto de rendimiento (Zen Score). 

Las escogidas son: 

![](Aspose.Words.b64a2492-d145-4216-9d5f-0c3f97139980.006.png)


Este archivo README proporciona una visión general del proyecto de inversión para el equipo de la UAX. Es importante asegurarse de que todas las herramientas y procesos estén adecuadamente documentados para que los colaboradores puedan seguir fácilmente los pasos necesarios. Además, cualquier cambio en los criterios de selección o en las fuentes de datos debe reflejarse actualizando este documento.
