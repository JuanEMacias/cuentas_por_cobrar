<h1 align="center"> Análisis de cuentas por cobrar 📝  </h1>

## Descripción
***
En este proyecto se trabaja con un conjunto de datos de cuentas por cobrar, siendo que el objetivo es centrarse en las cuentas o facturas en disputa. Estas facturas son aquellas que los clientes por alguna razón se niegan a pagar ya que se pide que se les libre de la responsabilidad del pago de las mismas. 
En este caso, vamos a examinar que factores son los que influyen más para que los clientes tomen dicha postura y poder identificar que caracteristicas tienen dichos clientes para que el área de cobranza obtenga un mejor panorama para tomar mediadas preventivas ante las facturas en disputa. 


Las tareas llevadas a cabo son:
*	Llevar a cabo el análisis exploratorio de datos
*	Identificar cuentas en disputa
*	Realización de clústeres para identificar características de facturas en disputa


## Descripción de los datos 
El dataset comprimido `WA_Fn-UseC_-Accounts-Receivable` contiene las siguientes columnas:

- `countryCode`: Códifgo del país del cliente 	
- `customerID`: Número de idenitficaión del cliente
- `PaperlessDate`: Fecha de entrega de factura	
- `invoiceNumber`: Número de factura 	
- `InvoiceDate`: Fecha de facturación 	
- `DueDate`: Fecha prevista de pago (aproxiamdamente 30 dias)
- `InvoiceAmount`: Monto de la factura	
- `Disputed`: Indica si la factura está en disputa o no, en caso positivo signiifca que el cliente ha decidido que no es responsable del pago de la factura. 	
- `SettledDate`: Fecha límite de pago	
- `PaperlessBill`: indica si la factura se entregó en papel o de manera electrónica. 	
- `DaysToSettlev`: Días trnascurridos para fecha límite de pago
- `DaysLate`. Indica el número de días de atraso. 

## Tareas 
### 1. Preprocesamiento de datos 
* Explorar los datos y hacer correcciones a los tipos de datos
* Realizamos limpieza de datos analizando valores nulos y duplicados

### 2. Análisis exploratorio
Primero realizamos las gráficas generales para observar la distrubución de los datos;
como por ejemplo la cantidad de facturas a través del tiempo. 

Después agrupamos los datos por país para saber que paises tienen más días de atraso o facturas en disputa y saber si se sigue algún patrón. 

El siguiente insight es para conocer si los clienteslas fechas tenían alguan influencia dentro de la atención, ya que como observamos en el proyecto, hay diferentes fechas en las que se generan facturas en disputa por lo que se consideró interesante explorar la realción entre la fechas y facturas en disputa.

### Pronóstico y predicciones 
Utilizamos la función de pandas `pd.get_dummies(df)`  para lograr convertir las variables de dataframe a tipo numérico y realizar la agrupación por clusteres.

Posterioemte mediante un dendrograma y una grafica de método del codo realizamos uan agrupación por clústeres con variables del dataset y conocer las características de facturas en disputa, dichas agrupaciones se muestran mediante graficas de dispersión.



## Tecnologías
Los recursos utilizados en este proyecto son:
* Librerías de Python 
	* Pandas 
	* Numpy
	* Matplotlib
	* Seaborn
	* Scikit Learn

* Jupyter Notebooks

Utilizamos las librería de Pandas y Numpy   para el preprocesamiento de los datos tratando valores ausentes  y duplicados así como identificando outliers. 

Para temas de visualización de gráficas se utilizaron las librerías de Matplotlib y Seaborn, principalmente para la distribución de los datos, y gráficos de dispersión, esto debido al poco espacio de memoria que utilizan.


Finalmente, se utilizó la librería de Scikit Learn para obtener la información de los clústeres así como la agrupación de los mismos y la relación entre las diferentes variables. 


  ## Uso del código
  Todos los bloques de código se encuentran en el archivo .ipynb y el set de datos en el arhivo .csv. Para utilizarlo descargar los archivos csv, copie el cuaderno y ejecute los bloques de código.
