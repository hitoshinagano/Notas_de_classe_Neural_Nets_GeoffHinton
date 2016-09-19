# Notas de classe Neural Nets Prof. GeoffHinton

Algumas notas de classes sobre a matéria, observações e também algumas dúvidas.

## Aula 2c

Nessa aula é apresentado um diagrama, conforme abaixo:

<img src="https://github.com/hitoshinagano/Notas-de-classe-Neural-Nets-Geoff-Hinton/blob/master/figuras/Figura_aula_2c.png" width="350">

Complementando a explicação do Prof. Hinton fiz a seguinte figura, na qual desenho um plano.

<img src="https://github.com/hitoshinagano/Notas-de-classe-Neural-Nets-Geoff-Hinton/blob/master/figuras/plano_e_seus_dois_lados.png" width="500">

Um plano perpendicular ao vetor vermelho (linha grossa em vermelho), que separa o espaço em dois lados:

1. conjunto dos pontos cujo produto interno **w**.**x** é positivo (lado A)
2. outro conjunto dos pontos cujo produto interno **w**.**x** é negativo (lado B)

Se ponto **x** tivesse sido classificado corretamente, o vetor **w** não precisaria ser atualizado. 
Por exemplo, se **x** fosse da classe 0 e o produto interno sendo negativo, então nada precisaria ser feito e **w** não precisaria ser alterado. 

Ao contrário, no exemplo do Prof. Hinton, **x** é da classe 1, e está classificado incorretamente. Pelas regras de atualização do perceptron, será efetuado **w**<-**w**+**x**. 
A atualização de **w**<-**w**+**x** gera um novo plano (em verde), sendo que o lado C corresponde a uma classificação dos pontos positivos, enquanto que o lado D aos pontos negativos. 

<img src="https://github.com/hitoshinagano/Notas-de-classe-Neural-Nets-Geoff-Hinton/blob/master/figuras/apos_soma_w_com_x.png" width="500">

Veja que a atualização de **w**<-**w**+**x** faz com que **w** se "aproxime" de x. (**w** é "puxado" no sentido de **x**). Essa aproximação faz aumentar as chances do produto interno se tornar positivo. De fato, se dois vetores tem um ângulo maior que 90 graus, somar **x** ao vetor **w**, fará o ângulo diminuir. 

Assim é a dinâmica do perceptron. O vetor **w** ora é puxado no sentido de **x**, ou empurrado para longe de **x** (caso onde o erro de classificação ocorre ao contrário do exemplo descrito acima, ou seja quando o ponto **x** é classe 0, mas é classificado como 1), dependendo dos erros de classificação encontrados.
