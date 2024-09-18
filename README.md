# Ajustamento das observações 2 ---> AVALIAÇÃO FINAL


## Aqui é apresentado o código utilizado no seminário e o problema da prova.


## Primeiramente, identificamos o problema e iniciamos uma investigação aprofundada sobre o tema. A compreensão da complexidade inerente ao assunto demandou um extenso período de estudo e análise crítica, durante o qual consultamos uma variedade de artigos acadêmicos. Devido à natureza intrincada do tópico, foi essencial dedicar um tempo considerável à leitura e interpretação dos materiais consultados para obter um entendimento mais robusto e fundamentado.
## O primeiro passo, foi entender como seria feito o ajustamento do modelo matemático identificado. Utilizamos o método combinado sem injunções. Todo o passo a passo está descrito no arquivo jupyter notebook
## Os problemas de todos os alunos estão neste repositório.

##Controle de Qualidade do Ajustamento
##Seminário em Grupo da turma de CA412 - Ajustamento de Observações II 2024.1
###Docente:
ERISON ROSA DE OLIVEIRA BARROS erison.barros@ufpe.br

###Dicentes:
JOAO IGOR MENDONÇA SIQUEIRA joao.igormendonca@ufpe.br
MELQUIZEDEK LUIDSON NUNES DANTAS melquizedek.dantas@ufpe.br
RAFAEL MARTINS DA SILVA rafael.martinss@ufpe.br
THIAGO GAMA DE LIMA thiago.gama@ufpe.br

##Introdução
Qualquer dado experimental pode carregar consigo um erro aleatório e este por sua vez é impossível de ser eliminado por conta da medida de precisão do instrumento e a forma que o método de medida foi utilizado. Por conta disso, para o aumento da qualidade dos dados, mede-se o maior número de observações para melhor ajustamento do que o mínimo necessário para a solução do problema. Com essa redundância no sistema matemático gerado ocorrerá inconsistência devido aos erros nos valores observados.

Assim assumimos que existe um erro aleatório em cada observação efetuada, para que desta forma podemos aplicar o Método dos Mínimos Quadrados (MMQ). Que é o critério mais utilizado para o ajustamento de observações geodésicas (Ghilani e Wolf, 2006). Este método adota como solução única para sistemas de equações redundantes e inconsistentes, aquela que minimiza a soma do quadrado dos resíduos, ponderada pelos respectivos pesos das observações (DALMOLIN, 2002). Entretanto, o método dos mínimos quadrados pressupõe que apenas erros aleatórios contaminam as observações (KAVOURAS, 1982).

Ao longo dos anos foram desenvolvidas diversas técnicas para detecção e identificação de erros não aleatórios nas observações, tanto antes quanto após o ajustamento ter sido realizado. Serão trabalhadas aqui as técnicas Qui-Quadrado e data-snooping, proposto por Baarda (1968).

##Histório do método
O método Qui-Quadrado, redescoberto por Karl Pearson no início do século XX, representou um grande avanço na análise estatística. Pearson buscava desenvolver ferramentas para analisar dados e testar hipóteses sobre distribuições de frequência. Em seu trabalho, ele investigou um critério de probabilidade em qualquer teoria de um sistema de erros observados e aplicá-lo à determinação da qualidade do ajuste no caso da frequência de corte (Pearson, 1900), demonstrando a versatilidade do método.

O processo de data-snooping tem como objetivo a identificação de desvios significativos do padrão esperado, sugerindo a presença de erros grosseiros em dados após a realização de ajustes estatísticos. Ao rejeitar a hipótese nula (H₀), indicando que o modelo não se ajusta perfeitamente aos dados, os geodesistas empreendem uma busca sistemática por esses erro.

Essa prática, comum em diversas áreas da ciência, visa encontrar a observação específica onde ocorreu o erro grosseiro. O Baarda propõe em seu livro uma metodologia para identificar essas observações, sugerindo o cálculo de um conjunto de valores e a reavaliação das observações que excederem um determinado limite.

Essa abordagem demonstra a importância da detecção e correção de erros para garantir a qualidade dos resultados em análises geodésicas.

Embora o próprio Baarda comente que a técnica não garante a identificação de todos os erros, especialmente se houver múltiplos erros simultâneos e a reavaliação das observações pode ser custosa em termos de tempo e recursos.

Modelos Matemáticos e funcionais
Qui-quadrado:
![image](https://github.com/user-attachments/assets/9c859db4-b0c5-4c8f-bbd9-62d44cb87909)

 
Segundo Gemael (1994), é o qui-quadrado amostral, é a variância da observação de peso unitário a priori e é o grau de liberdade no ajustamento.
E os parâmetros ajustados são rejeitados nos testes estatísticos caso não cumpra essa condição imposta.

Data-snooping:
 
 é resíduo predito da observação

 é desvio padrão dos residuos

 é a correção normalizada

 é extraida da curva normal

Segundo Santos (2009), caso algum erro seja detectado e identificado, as observações são descartadas do processo e o vetor dos parâmetros calculados não é atualizado.
