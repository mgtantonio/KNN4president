# KNN4president
El tiempo es aleatorio

Lo que más hay que mirar yo creo que es el estado del arte. A continuación se ven los artículos relaccionados que encontramos y la relacción que tienen con nuestro tabajo:

1. "Convolutional LSTM Network: A Machine Learning Approach for Precipitation Nowcasting", by "SHI, Xingjian and Chen, Zhourong and Wang, Hao and Yeung, Dit-Yan and Wong, Wai-kin and WOO, Wang-chun"
    
    Citado 1787 veces según Google Scholar
    Plantean el problema de la predicción temporal, desde la perspectiva del machine learning, como un problema de predicción de una "secuencia espacio-temporal" en la que la entrada y la predicciçión son secuencias espacio-temporales.
    Proponen una red LSTM Convolucional y la usan para construir un modelo "end-to-end". Consiguen mejores resultados que con la *fully connected LSTM* y el algoritmo ROVER.
          
    -->**Igual hay que echar un ojo al ROVER ese, que estos dicen que es el estado del arte en predicción "a corto plazo" (nowcasting).**
    "**R**eal-time **O**ptical ﬂow by **V**ariational methods for **E**choes of **R**adar"
    
    Ahora que se esto... ¿Cómo decimos que no usamos ConvLSTM porque no teníamos ni puta idea de que existían?
    
2. "Hourly day-ahead solar irradiance prediction using weather forecasts by LSTM", by "Xiangyun Qing and Yugang Niu"

    Propone un planteamiento de predicción solar por horas cada día usando datos de la predicción meteorilógica.
    Compara el uso de redes LSTM con algoritmos de regresión lineal por mínimos cuadrados y redes neuronales multicapa entrenadas con Backpropagation (BPNN).
    LSTM consigue un 18,34% más de precisión según RMSE, con dos aós de datos de entrenamiento para predecir medio año. LSTM consigue también menor sobreentrenamiento y mayor generalización.
    Usando 10 años de entrenamiento para predecir un año la predicción con LSTM se reduce en un 42,9% contra el BPNN.
  
3. "Current methods and advances in forecasting of wind power generation", by "Aoife M. Foley and Paul G. Leahy and Antonino Marvuglia and Eamon J. McKeogh"
  
  MIRAR BIEN, parece que está tocho (641 citaciones). Artículo de 2012.
  Presenta una revisión profunda de los actualez métodos y avances de la predicción de potencia del viento.En primer lugar, métodos de predicción numérica, desde escala global a local, "ensemble forecasting" (conjunto numérico de pronósticos), upscaling y downscaling processes. En segundo lugar, métodos estadísticos y con enfoque de *machine learning*.  
  Tiene una presentación cojonuda de los actuales métodos de pronóstico y predicción. Distingue entre métodos físicos, estadísticos (los nuestros) e híbridos. Explica que los modelos físicos son buenos para predicciones a gran escala (medias mensuales, por cuatrimestes, anuales), y que los estadísticos dan mejores predicciones a corto plazo, por día o por hora, según otro artículo ([7]).
  
 **Habla de que el RMSE es más fácil de interpretar porque está expresado en las mismas unidades que la predicción.**
   Las técnicas que utiliza son :
   AR, MA, ARMA, ARIMA. También Filtros de Kalman. Redes neuronales artificiales (ANN) y sistemas fuzzy, predictores de gray (11,2%-12,2% mejores que Naive-Bayes) y Support Vector Machines (SVM). Menciona el uso de algoritmos genéticos para optimizar sistemas fuzzy con resultados entre 9,5% y 29c4% de mejora respecto a Naive-Bayes. Habla de métodos PSO (particle swarm optimization) 
   Cosa importante para la discusión: 
    Torres et al. [29] found it was possible to get 20% error reduction compared to persistence(predictor de Naive-Bayes) to forecast average hourly wind speed for a 10 h forecast horizon at a number of locations using nine years of historical data using an ARMA model.
    
    
4. EL puto algoritmo ROVER

    Según [1] tiene mejor ratio de error que la FC-LSTM, pero peor que la ConvLSTM
 
5. "A novel approach for precipitation forecast via improved K-nearest neighbor algorithm", by "Mingming Huang, Runsheng Lin, Shuai Huang, TengfeiXingc
    
    Artículo de 2017. Simplemente dicen que el KNN ha mostrado buenos resultados en predicción meteorológica. proponen el uso de ese algoritmo por su robustez a la hora de elegir la k, especialmente cuando se trata de distribuciones irregulares.
    Meh
    
6. "Fire risk prevention in underground coal gasification (UCG) within active mines: Temperature forecast by means of MARS models", by "Alicjia Krzemien

    Prevención de fuegos en UCGs con predicción de temperatura media usando MARS.
    Pretende conseguir un modelo que prediga con una hora de anticipación la temperatura de la estancia, basándose en diferentes parámetros medidos cada hora durante el experimento. Sin más, como mucho echar un ojo a ver si menciona el por qué usa el MARS:
    
    Lo interesante del MARS es que adjusta los parámetros a los datos (efectivamente, es una regresión), incluyendo no-linealidades, por lo que da mucha ventaja para modelos en los que no sabemos mucho sobre su comportamiento. No hay que hacer presuposiciones sobre el funcionamiento del modelo como en otros algoritmos de regresión o clasificación como en los CART. Menciona a Friedman [9].
    
 7. "Short-term prediction of local wind conditions", by "L Landberg"
    
    91 citaciones. Artículo de 2001. Mencionado el el artículo [3] para explicar los buenos resultados de algoritmos estadísticos a corto plazo.
   
 8. "State-of-the-art Methods and software tools for short-term prediction of wind energy production", by "Gregor Giebel, L. Landberg, Georges Kariniotakis, Richard Brownsword"
 
    164 citaciones. También mencionado por [4] para mencionar los métodos para la predicción a corto plazo. Artículo de 2003, igual está un poco **anticuado**...
    
 9. "Multivariate Adaptive Regression Splines", by "Jerome H. Friedman"
  
    El creador del MARS. También vale mencionar el libro si no.
    
10. "Nearest neighbor pattern classification", by "T. Cover, P.Hart"

    Artículo de 1967 en el IEEE con 11823 citaciones en Google Scholar.
    
29. "Forecast of hourly average wind speed with ARMA models in Navarre (Spain)", by "J.L.Torresa, A. García, M.De Blas, A.De Francisco"

    Afirma cosas interesantes sobre los modelos ARMA. Artículo de 2005
