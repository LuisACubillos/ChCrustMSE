# ChCrustMSE

Evaluación de Estrategias de Manejo para las pesquerías de crustáceos bentónicos chilenos: a) langostino colorado, b) langostino amarillo, y c) camarón nailon.

En este proyecto participan:

* María José Cuevas: Codificación, evaluación y análisis de resultados.
* Alejandro Yáñez: evaluación de stock, codificación y análisis de resultados.
* Mauricio Urbina: evaluación de stock, codificación y análisis de resultados.
* Juan Carlos Quiroz, evaluación de estrategias de manejo, codificación, evaluación de desempeño y análisis de resultados.
* Luis A. Cubillos: Gestor del proyecto, conceptualización, evaluación de estrategias de manejo, codificación, evaluación de desempeño y análisis de resultados.

## Nota

Los códigos están escritos en [ADMB](http://www.admb-project.org/) templates ([Fournier et al. 2012](https://doi.org/10.1080/10556788.2011.597854)), y alojados en la carpeta [srcadmb] por pesquerías. La pesquería de cada crustáceo contiene un estimador por unidad de pesquería, cuya codificación original (TPL y DAT) han sido documentados por investigadores del [Instituto de Fomento Pesquero](https://www.ifop.cl/busqueda-de-informes/).

### Requerimientos

* Un comilador C++
* ADMB-12.0 o superior

### Clonación

	cd ~
	git clone https://github.com/luisacubillos/ChCrustMSE
	cd ChCMSE


### Instucciones

Los códigos de cada pesquería están alojados en la carpeta "scradmb" (por ejemplo, "scradmb/lcolsur/") y contiene dos carpetas:

* Carpeta "sam": contiene el código ".tpl" y los datos ".dat" del estimador o modelo de evaluación de stock.

* Carpeta "mo" contiene el código ".tpl" y los datos ".dat" que contiene una función que permite activar las simulaciones con el modelo operativo.
