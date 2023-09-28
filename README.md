# T1_Software_Basico

## Introdução 
<br>
O primeiro trabalho da disciplina consiste em adicionar novas funções à uma biblioteca para o processamento de imagens. Para isso, deverá ser criada uma aplicação de demonstração que utiliza pelo menos 3 imagens como entrada, aplica diferentes filtros e gera diversas imagens como saída apresentando a funcionalidade de cada um dos filtros implementados em cada uma das imagens.
As imagens de entrada deverão ser uma coloridas com precisão de 24 bits por pixel (R, G, B), onde cada componente possui um valor de intensidade
de 0 a 255. As imagens utilizadas como entrada deverão possuir tamanhos variados (acima de 512x512 pixels) e no máximo uma das imagens poderá
ser quadrada. Para a manipulação de imagens, está sendo fornecida uma biblioteca que permite ler e escrever imagens no formato PPM (Portable Pix Map).

## Definição  dos  filtros  a  serem  implementados

Os  seguintes  filtros  para  o  processamento  de  imagens  deverão  ser  implementados:

## 1.	Imagem em tons de cinza 
para converter uma imagem para tons de cinza deve-se extrair a componente luminˆancia, calculado com base em valores ponderados dos canais R, G e B de cada pixel por meio da fórmula:
 Y  = R    0.299 + G    0.587 + B    0.114
 Deve-se copiar o mesmo resultado de cada pixel para todas as componentes da imagem destino.

## 2.	Operação  threshold 
inicialmente,  deve-se  converter  a  imagem  para tons de cinza. Posteriormente, para cada pixel da imagem, deve-se verificar  se  o  seu  valor  está  abaixo  do  limiar  (threshold)  definido  pelo usuário.    
Se  estiver,  o  valor  do  pixel  resultante  será  0  (preto),  caso contrario  será  255  (branco).   
Deve-se  copiar  o  mesmo  resultado  para todas as componentes da imagem destino.

## 3.	Filtro  Sobel 
é  um  filtro  utilizado  para  a  detecção  de  bordas  em  uma imagem,  onde  é  utilizado  um  operador  de  convolução  com  dimensão 3x3.   Nesse  filtro,  em  uma  versão  simplificada  ignora-se  os  pixels  da periferia  da  imagem  resultante  (não  recebem  valor).    Cada  pixel  da imagem resultante é calculado por meio da aplicação de duas matrizes (vertical  e  horizontal)  que  são  convoluídas  com  a  pixels  da  imagem original.  O  pixel  gerado  a  partir  da  aplicação  do  operador é  o  central a  partir  das  matrizes.  O  valor  final  do  pixel é  dado  por  Gx2 + Gy2, e pode ser aproximado por Gx + Gy . Esse filtro deve ser aplicado independentemente em cada componente da imagem.


## 4.	Filtro Roberts Cross 
assim como o filtro anterior, esse pode ser utilizado  para  detecção  de  bordas  em  uma  imagem,  sendo  utilizado  um operador  com  dimensão  2x2.  O  funcionamento é  idêntico  ao  filtro  anterior,  com  diferença  apenas  na  dimensão  e  valores  dos  operadores  de convolução.  O pixel gerado a partir da aplicação do operador é o superior  esquerdo  a  partir  das  matrizes.  O  valor  final  do  pixel é  dado  por Gx2 + Gy2, e pode ser aproximado por Gx  +  Gy .  Esse filtro deve ser aplicado independentemente em cada componente da imagem.

