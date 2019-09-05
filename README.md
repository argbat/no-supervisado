# Practicos de no supervisado.

## Relgas de asociacion.

### Como correr la notebook.
Descargar del sitio https://grouplens.org/datasets/movielens/ el archivo ml-20m.zip. Descomprimirlo y quedarse con los archivos movies.csv y ratings.csv y colocarlos en el mismo directorio de la notebook.

Luego corrarer la notebook con jupyter.

### Conclusion.

Nos quedamos con reglas donde el Lift sea mayor a 0.7.

Seleccionamos Lift como metrica ya que nos ayuda a descartar casos en que el Confidence no nos aporta informacion, por ejemplo en casos tales como: conf({Rey Leon}=>{Toys Story})=0.8 y prob({Toys Story}) = 0.8. Dicho de otr forma, en el caso del ejemplo que se haya comprado {Toys Story} no esta condicionado de forma alguna con que sepamos que se haya comprado {Rey Leon}.

El Lift también tiene una interpretación probabilística. Si el Lift es 1, significa que la confianza de la regla es igual al soporte de "{Toys Story}"; en otras palabras significa que "{Rey Leon}" y "{Toys Story}" son independientes. Debemos recordar que el soporte es la frecuencia relativa del item set. La confianza es la probabilidad empírica de que ocurra el consecuente, dado que ocurrió el antecedente en la regla. Y el Lift refleja el aumento de la probabilidad de que ocurra el consecuente, cuando nos enteramos de que ocurrió el antecedente.
