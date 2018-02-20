# Procesos Estocásticos en R
Synergy Vision  
`r Sys.Date()`  
<script src="https://cdn.datacamp.com/datacamp-light-latest.min.js"></script>

--- 
title: "Procesos Estocásticos en R"
subtitle: "Ciencia de los Datos Financieros"
author: "Synergy Vision"
date: "2018-02-20"
knit: "bookdown::render_book"
documentclass: krantz
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
colorlinks: yes
lot: yes
lof: yes
fontsize: 12pt
monofontoptions: "Scale=0.8"
keep_md: yes
site: bookdown::bookdown_site
description: ""
url: 'http\://synergy.vision/Procesos-Estocasticos-en-R/'
github-repo: synergyvision/Procesos-Estocasticos-en-R/
cover-image: images/cover.png
---





# Prefacio {-}

<a href="https://synergy.vision/LibrosInteractivos/" target="_blank"><img src="images/cover.png" style="display: block; margin: auto;" /></a>


![Creative Commons License](images/by-nc-sa.png)  
La versión en línea de este libro se comparte bajo la licencia [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/).

## ¿Por qué  leer este libro? {-}

Este libro es el resultado de enfocarnos en proveer la mayor cantidad de material sobre Probabilidad y Estadística Matemática con un desarrollo teórico lo más explícito posible, con el valor agregado de incorporar ejemplos de las finanzas y la programación en `R`. Finalmente tenemos un libro interactivo que ofrece una experiencia de aprendizaje distinta e innovadora.

El un mundo abierto, ya no es tanto el acceso a la información, sino el acceso al conocimiento. Este libro es la base teórica para nuestro Diplomado en Probabilidades y Estadística Matemática aplicado a las Finanzas. Aunque es un material de corte general, hay ejemplos específicos traido de las finanzas. En el Diplomado nos enfocamos en el participante, el propósito es que el instructor ocupa a lo sumo el 20% del tiempo y el resto del tiempo los participantes se dedican a practicar y resolver ejercicios, tanto teóricos como de programación y modelaje en `R` al nivel de un curso de Postgrado. Ésta es la base de un programa en Ciencia de los Datos Financieros.

Es mucha la literatura, pero son pocas las opciones donde se pueda navegar el libro de forma amigable y además contar con ejemplos en `R` y ejercicios interactivos, además del contenido multimedia. Esperamos que ésta sea un contribución sobre nuevas prácticas para publicar el contenido y darle vida, crear una experiencia distinta, una experiencia interactiva y visual. El reto es darle vida al contenido asistidos con las herramientas de Internet.

Finalmente este es un intento de ofrecer otra visión sobre la enseñanza y la generación de material más accesible. Estamos en un mundo multidisciplinado, es por ello que ahora hay que generar contenido que conjugue en un mismo lugar las matemáticas, estadística, finanzas y la computación.

Lo dejamos público ya que las herramientas que usamos para ensamblarlo son abiertas y públicas.

## Estructura del libro {-}

TODO: Describir la estructura

## Información sobre los programas y convenciones {-}

Este libro es posible gracias a una gran cantidad de desarrolladores que contribuyen en la construcción de herramientas para generar documentos enriquecidos e interactivos. En particular al autor de los paquetes Yihui Xie xie2015.

## Prácticas interactivas con R {-}

Vamos a utilizar el paquete [Datacamp Tutorial](https://github.com/datacamp/tutorial) que utiliza la librería en JavaScript [Datacamp Light](https://github.com/datacamp/datacamp-light) para crear ejercicios y prácticas con `R`. De esta forma el libro es completamente interactivo y con prácticas incluidas. De esta forma estamos creando una experiencia única de aprendizaje en línea.

<div data-datacamp-exercise data-height="300" data-encoded="true">eyJsYW5ndWFnZSI6InIiLCJwcmVfZXhlcmNpc2VfY29kZSI6ImIgPC0gNSIsInNhbXBsZSI6IiMgQ3JlYSB1bmEgdmFyaWFibGUgYSwgaWd1YWwgYSA1XG5cblxuIyBNdWVzdHJhIGVsIHZhbG9yIGRlIGEiLCJzb2x1dGlvbiI6IiMgQ3JlYSB1bmEgdmFyaWFibGUgYSwgaWd1YWwgYSA1XG5hIDwtIDVcblxuIyBNdWVzdHJhIGVsIHZhbG9yIGRlIGFcbmEiLCJzY3QiOiJ0ZXN0X29iamVjdChcImFcIilcbnRlc3Rfb3V0cHV0X2NvbnRhaW5zKFwiYVwiLCBpbmNvcnJlY3RfbXNnID0gXCJBc2VnJnVhY3V0ZTtyYXRlIGRlIG1vc3RyYXIgZWwgdmFsb3IgZGUgYGFgLlwiKVxuc3VjY2Vzc19tc2coXCJFeGNlbGVudGUhXCIpIn0=</div>







## Agradecimientos {-}

A todo el equipo de Synergy Vision que no deja de soñar. Hay que hacer lo que pocos hacen, insistir, insistir hasta alcanzar. Lo más importante es concretar las ideas. La idea es sólo el inicio y solo vale cuando se concreta.


\BeginKnitrBlock{flushright}<p class="flushright">Synergy Vision, Caracas, Venezuela</p>\EndKnitrBlock{flushright}








<!--chapter:end:index.Rmd-->


# Acerca del Autor {-}

Este material es un esfuerzo de equipo en Synergy Vision, (<http://synergy.vision/nosotros/>).		 

El propósito de este material es ofrecer una experiencia de aprendizaje distinta y enfocada en el estudiante. El propósito es que realmente aprenda y practique con mucha intensidad. La idea es cambiar el modelo de clases magistrales y ofrecer una experiencia más centrada en el estudiante y menos centrado en el profesor. Para los temas más técnicos y avanzados es necesario trabajar de la mano con el estudiante y asistirlo en el proceso de aprendizaje con prácticas guiadas, material en línea e interactivo, videos, evaluación contínua de brechas y entendimiento, entre otros, para procurar el dominio de la materia.
  		  
Nuestro foco es la Ciencia de los Datos Financieros y para ello se desarrollará material sobre: **Probabilidad y Estadística Matemática en R**, **Programación Científica en R**, **Mercados**, **Inversiones y Trading**, **Datos y Modelos Financieros en R**, **Renta Fija**, **Inmunización de Carteras de Renta Fija**, **Teoría de Riesgo en R**, **Finanzas Cuantitativas**, **Ingeniería Financiera**, **Procesos Estocásticos en R**, **Series de Tiempo en R**, **Ciencia de los Datos**, **Ciencia de los Datos Financieros**, **Simulación en R**, **Desarrollo de Aplicaciones Interactivas en R**, **Minería de Datos**, **Aprendizaje Estadístico**, **Estadística Multivariante**, **Riesgo de Crédito**, **Riesgo de Liquidez**, **Riesgo de Mercado**, **Riesgo Operacional**, **Riesgo de Cambio**, **Análisis Técnico**, **Inversión Visual**, **Finanzas**, **Finanzas Corporativas**, **Valoración**, **Teoría de Portafolio**, entre otros.

Nuestra cuenta de Twitter es (https://twitter.com/bysynergyvision) y nuestros repositorios están en GitHub (https://github.com/synergyvision).
  		  
 **Somos Científicos de Datos Financieros**

<!--chapter:end:000-author.Rmd-->

\mainmatter

# Introducción 

Conocer en qué se invierte es un problema fundamental en la gestión del capital propio o de terceros, es el problema primario en la gestión de inversiones. La gestión de inversiones es un campo con muchos avances que, hoy en día, demanda métodos basados en las ciencias. En particular las matemáticas, probabilidades y la computación.

Un primer avance en la solución de este problema es ofrecido por Harry Markowitz en 1952 e inaugura una nueva era en la aplicación de los métodos matemáticos para obtener carteras de inversión con características especiales, para conocer la relación entre el riesgo y el rendimiento. Este avance es reconocido con el precio Nobel en Economía en 1990 e inaugura la era de las Finanzas Cuantitativas, las Finanzas Computaciones, las Matemáticas Financieras, la Ingenería Financiera, entre otras prácticas.

Markowitz desarrolla  un modelo que considera los retornos de cada instrumento como una variable aleatoria y combina estas variables aleatorias para obtener el riesgo y el rendimiento de dicha combinación. Esta combinación de intrumentos es lo que denominamos portafolios y el objeto de Markowitz es encontrar los portafolios óptimos. Los portafolios óptimos son combinaciones de activos financieros que generan el mayor rendimiento posible con el menor riesgo. La combinación de activos nos lleva a la idea de la diversificación y su efecto en la gestión del riesgo, ya que ahora también es importante la relación que existe entre los instrumentos como un factor determinante del riesgo de la cartera.

Si los instrumentos tienen una correlación positiva, el riesgo no disminuye, sin embargo si la correlación es negativa es posible, mediante la diversificación, disminuir el riesgo de la cartera.

En la práctica es muy complejo obtener instrumentos no correlacionados, ya que los mercados tienen a seguir ciclos alcistas o bajistas y los instrumentos tienen a moverse de forma acompasada. Es decir, que la diversificación no necesariamente logra el objetivo de disminuir el riesgo de la cartera.

Con estos avances ahora el rendimiento no se discute de forma aislada, el rendimiento siempre viene acompañado del riesgo y ahora la selección del inversionista debe considerar ambas variables para tomar su decisión. Este terreno es un campo con muchos avances ya que se aplican diversos métodos de optimización, de simulación o de medición del riesgo para conseguir las carteras que cumplen con la mejor relación para el inversionista.

Este trabajo pretende abordar el campo de la distribución del capital en activos financieros que cumplen con ciertas condiciones partiendo de los datos disponibles. En este trabajo partiremos de la historia de los instrumentos para obtener sus características y conformar portafolios óptimos de acuerdo a la metodología de Markowitz. Adicionalmente se desarrollarán herramientas para facilitar el procesamiento de los datos y obtener dichos portafolios.

## Motivation

La historia reciente de los mercados, se caracteriza por la presencia de varias burbujas o grandes choques en los mercados. En el mercado americano, iniciemos desde 1999-2000 con la burbuja de las empresas tecnológicas que surgen con el auge de Internet y tienen como objetivo el desarrollo de la nueva economía virtual, hoy día es evidente que Amazon y Google son las grandes empresas que capitalizaron gran parte del potencial, el gran impacto generado por la caida de las Torres Gemelas en Septiembre del 2001 y luego la gran crisis inmobiliaria durante el 2007-2008 de la cual se ha recuperado apenas en 2015-2016. Hoy de nuevo, en el año 2017, estamos en presencia de un mercado alcista que alcanza nuevo territorio, ha alcanzado nuevos altos históricos y es inevitable la pregunta: ¿Estamos en presencia de una nueva burbuja?. Esta pregunta no tiene el objetivo de predecir que el mercado va a caer en algún momento, de hecho lo normal es que lo haga, el mercado cumple ciclos contínuamente y no tiene nada de innovador señalar que va a caer cuando hace altos históricos. El mercado se mueve en ondas. Lo que nos interesa de esta dinámica es cómo construir carteras de inversión que puedan sobrevivir estos choques, estos mercados bajistas y al mismo tiempo aprovechar al máximo los mercados alcistas.

Desde 1952 y más notablemente desde 1990 que recibe el premio Nobel de Economía, Harry Markowitz es señalado como el padre de la Teoría Moderna de Portafolio. Su objetivo es definir una metodología que partiendo de un grupo de activos, se generan las carteras eficientes. Mucho ha ocurrido desde que la Economía reconoce como un área de desarrollo la aplicación de los modelos Matemáticos para ofrecer luz sobre la dedicación óptima del capital.

Este reconocimiento al aporte de la ciencia en la Economía genera dos grandes líneas de trabajo que intenta responder dos preguntas fundamentales: ¿Dónde coloco el capital y en qué cantidad? y ¿Cuál es el precio de un activo financiero?. Este trabajo elabora sobre la primera pregunta. La segunda pregunta tiene que ver con el trabajo de Black, Scholes y Merton sobre la Valoración de opciones y derivados financieros, que también reciben el premio Nobel de Economía en 1997, apenas hace 20 años. Esta línea de trabajo donde se conjugan varias disciplinas como las Finanzas, Matemáticas, Estadística y más recientemente la Computación, genera un nuevo sector de Analistas Financieros Multidisciplinados que denominaremos Científicos de Datos Financieros.

La demanda principal a estos analistas consiste en partir de los datos y generar inferencias sobre los mismos aplicando la ciencia y la tecnología. Gran parte del trabajo de Markowitz ha sido la aplicación de métodos de optimización de portafolios con el uso de las computadoras y asistido por sistemas.

Las grandes burbujas y choques al mercado generan una gran preocupación sobre la gestión apropiada del riesgo y al mismo tiempo un entendimiento de la relación entre el riesgo que se asume y los beneficios posibles. El rendimiento es el resultado de una inversión después de un período de tiempo específico, podemos ganar o perder cuando realizamos una inversión, entonces el rendimiento es la variación (porcentual) del valor de un activo financiero en un período de tiempo. La variación del valor en términos absolutos es la ganancia o pérdida en valor monetario. Por otra parte el riesgo, en este caso, se puede definir como el grado de variabilidad de dicho rendimiento, esta es la medida propuesta por Markowitz y más recientemente han surgido nuevas medidas como el Valor en Riesgo (VaR) o el VaR Condicional (CVaR).

Usualmente para rendimientos iguales, en teoría, y de acuerdo a la teoría de decisiones racionales bajo incertidumbre, un inversionista debería preferir la inversión con menor riesgo y por otra parte para riesgos iguales, en general, deberíamos preferir la inversión de mayor rendimiento.

En este trabajo vamos a concentrarnos en la primera pregunta y nos basaremos en las aspiraciones del inversionista para conocer cuales instrumentos pueden formar parte de la cartera y en qué cantidad son requeridos para alcanzar un objetivo de inversión que combina la medida de rentabilidad y la medida de riesgo.

Los gerentes e inversionistas se enfrentan a situaciones donde deben escoger entre distintas alternativas de inversión basándose en estas dos variables principales, a saber, el rendimiento y el riesgo. Las preguntas son diversas y típicas como por ejemplo:

\begin{itemize}
\item ¿Cuál inversión es preferible? ¿Una con rendimiento promedio $8\%$ y riesgo (desviación estándar) de $4\%$ o una con $8\%$ y $3\%$ respectivamente?
\item ¿Cuál inversión es preferible? ¿Una con rendimiento promedio $8\%$ y riesgo (desviación estándar) de $4\%$ o una con $10\%$ y $4\%$ respectivamente?
\item ¿Cuál inversión es preferible? ¿Una con rendimiento promedio $8\%$ y riesgo (desviación estándar) de $4\%$ o una con $10\%$ y $5\%$ respectivamente?
\item ¿Cómo disminuyo el riesgo de una cartera de inversión, si deseo mantener el rendimiento?
\item ¿Cómo aumento la rentabilidad de una cartera de inversión, sin aumentar el riesgo?
\item ¿Cuál es al balance óptimo entre activos de inversión para lograr un máximo rendimiento al menor riesgo posible?
\end{itemize}

El problema fundamental es encontrar el balance adecuado entre un grupo de activos para alcanzar el máximo rendimiento con el mínimo riesgo.

Debido a los ciclos y choques que reciben los mercados, el mundo de hoy está retado a trabajar en un ambiente donde la incertidumbre sobre el desempeño de las inversiones es un hecho palpable y sin embargo desde el punto de vista de los inversionistas o accionistas es necesario ofrecer proyecciones de desempeño que si no se cumplen generan un cuestionamiento sobre el profesionalismo de los gerentes del portafolio o de productos.

Esto nos lleva a la valoración del riesgo debido a la incertidumbre inherente a los instrumentos de inversión, inclusive a nivel regulatorio la evaluación del riesgo con métodos más rigurosos ya empieza a ser necesario.

El trabajo de tesis consiste en la investigación documental del estado del arte en la conformación de portafolios de inversión y la aplicación de sus métodos, partiendo del trabajo de Harry Markowitz como base, con el objetivo de entender el desempeño de estas carteras en cada burbuja o choque que han recibido los mercado y además comparar algunas combinaciones de medidas de riesgo y rendimiento. Adicionalmente vamos a continuar la construcción de una aplicación Web interactiva para aplicar los métodos y valernos lo más posible de las diversas librerías construidas en R para este fin.




<!--chapter:end:010-introduction.Rmd-->

\cleardoublepage 

# (APPENDIX) Apéndice {-}

# Software Tools

For those who are not familiar with software packages required for using R Markdown, we give a brief introduction to the installation and maintenance of these packages.

## R and R packages

R can be downloaded and installed from any CRAN (the Comprehensive R Archive Network) mirrors, e.g., https://cran.rstudio.com. Please note that there will be a few new releases of R every year, and you may want to upgrade R occasionally.

To install the **bookdown** package, you can type this in R:


```r
install.packages("bookdown")
```

This installs all required R packages. You can also choose to install all optional packages as well, if you do not care too much about whether these packages will actually be used to compile your book (such as **htmlwidgets**):


```r
install.packages("bookdown", dependencies = TRUE)
```

If you want to test the development version of **bookdown** on GitHub, you need to install **devtools** first:


```r
if (!requireNamespace('devtools')) install.packages('devtools')
devtools::install_github('rstudio/bookdown')
```

R packages are also often constantly updated on CRAN or GitHub, so you may want to update them once in a while:


```r
update.packages(ask = FALSE)
```

Although it is not required, the RStudio IDE can make a lot of things much easier when you work on R-related projects. The RStudio IDE can be downloaded from https://www.rstudio.com.

## Pandoc

An R Markdown document (`*.Rmd`) is first compiled to Markdown (`*.md`) through the **knitr** package, and then Markdown is compiled to other output formats (such as LaTeX or HTML) through Pandoc.\index{Pandoc} This process is automated by the **rmarkdown** package. You do not need to install **knitr** or **rmarkdown** separately, because they are the required packages of **bookdown** and will be automatically installed when you install **bookdown**. However, Pandoc is not an R package, so it will not be automatically installed when you install **bookdown**. You can follow the installation instructions on the Pandoc homepage (http://pandoc.org) to install Pandoc, but if you use the RStudio IDE, you do not really need to install Pandoc separately, because RStudio includes a copy of Pandoc. The Pandoc version number can be obtained via:


```r
rmarkdown::pandoc_version()
## [1] '1.19.2.1'
```

If you find this version too low and there are Pandoc features only in a later version, you can install the later version of Pandoc, and **rmarkdown** will call the newer version instead of its built-in version.

## LaTeX

LaTeX\index{LaTeX} is required only if you want to convert your book to PDF. The typical choice of the LaTeX distribution depends on your operating system. Windows users may consider MiKTeX (http://miktex.org), Mac OS X users can install MacTeX (http://www.tug.org/mactex/), and Linux users can install TeXLive (http://www.tug.org/texlive). See https://www.latex-project.org/get/ for more information about LaTeX and its installation.

Most LaTeX distributions provide a minimal/basic package and a full package. You can install the basic package if you have limited disk space and know how to install LaTeX packages later. The full package is often significantly larger in size, since it contains all LaTeX packages, and you are unlikely to run into the problem of missing packages in LaTeX.

LaTeX error messages may be obscure to beginners, but you may find solutions by searching for the error message online (you have good chances of ending up on [StackExchange](http://tex.stackexchange.com)). In fact, the LaTeX code converted from R Markdown should be safe enough and you should not frequently run into LaTeX problems unless you introduced raw LaTeX content in your Rmd documents. The most common LaTeX problem should be missing LaTeX packages, and the error may look like this:

```latex
! LaTeX Error: File `titling.sty' not found.

Type X to quit or <RETURN> to proceed,
or enter new name. (Default extension: sty)

Enter file name: 
! Emergency stop.
<read *> 
         
l.107 ^^M

pandoc: Error producing PDF
Error: pandoc document conversion failed with error 43
Execution halted
```

This means you used a package that contains `titling.sty`, but it was not installed. LaTeX package names are often the same as the `*.sty` filenames, so in this case, you can try to install the `titling` package. Both MiKTeX and MacTeX provide a graphical user interface to manage packages. You can find the MiKTeX package manager from the start menu, and MacTeX's package manager from the application "TeX Live Utility". Type the name of the package, or the filename to search for the package and install it. TeXLive may be a little trickier: if you use the pre-built TeXLive packages of your Linux distribution, you need to search in the package repository and your keywords may match other non-LaTeX packages. Personally, I find it frustrating to use the pre-built collections of packages on Linux, and much easier to install TeXLive from source, in which case you can manage packages using the `tlmgr` command. For example, you can search for `titling.sty` from the TeXLive package repository:

```bash
tlmgr search --global --file titling.sty
# titling:
#	 texmf-dist/tex/latex/titling/titling.sty
```

Once you have figured out the package name, you can install it by:

```bash
tlmgr install titling  # may require sudo
```

LaTeX distributions and packages are also updated from time to time, and you may consider updating them especially when you run into LaTeX problems. You can find out the version of your LaTeX distribution by:



```r
system('pdflatex --version')
## MiKTeX-pdfTeX 2.9.5900 (1.40.17) (MiKTeX 2.9 64-bit)
## Copyright (C) 1982 D. E. Knuth, (C) 1996-2016 Han The Thanh
## TeX is a trademark of the American Mathematical Society.
## compiled with zlib version 1.2.8; using 1.2.8
## compiled with libpng version 1.6.21; using 1.6.21
## compiled with poppler version 0.42.0
## compiled with jpeg version 8.4
```

<!--chapter:end:400-apendice.Rmd-->

# Referencias {-}




<!--chapter:end:500-references.Rmd-->

