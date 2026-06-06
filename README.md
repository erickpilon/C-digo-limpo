Código Limpo (Clean Code)

Capítulo 2: Nomes Significativos (Meaningful Names)
No segundo capítulo, Martin nos lembra que a nomeação é a espinha dorsal da 
comunicação dentro do nosso código. Nomes bem escolhidos são como uma janela para a 
intenção do autor, eliminando a necessidade de explicações extras. A clareza na escolha 
dos nomes é o que realmente separa um código amador de um trabalho profissional.
Para atingir essa clareza, Robert Martin nos oferece alguns princípios de ouro. O primeiro e 
mais crucial é revelar a intenção. O nome de uma variável, função ou classe deve 
responder imediatamente: por que ela existe? O que ela faz? Como é usada? Se você 
precisa de um comentário para explicar um nome, ele falhou em seu propósito principal. 
Além disso, é vital evitar a desinformação. Não use palavras que já têm um significado 
técnico específico se o seu objeto não se encaixa nele (por exemplo, chamar algo de 
accountList se não for, de fato, uma lista de contas).
data, info ou variáveis numeradas como 
Outro ponto chave é a necessidade de fazer distinções significativas. Nomes genéricos 
como: a1 e a2 não agregam valor e só geram confusão. Se dois nomes são diferentes, a diferença entre eles deve ser óbvia para quem lê. 
O autor também destaca a importância de usar nomes pronunciáveis e buscáveis. Se 
você não consegue pronunciar um nome, a comunicação sobre o código com sua equipe se 
torna um desafio. Da mesma forma, nomes de uma única letra ou "números mágicos" 
(valores soltos no código) tornam a busca e a refatoração em grandes bases de código um 
verdadeiro pesadelo. Quando falamos de programação orientada a objetos, a regra é clara: classes devem ter 
nomes de substantivos (como de verbos (como Cliente ou postarPagamento ou Conta ), enquanto métodos devem ter nomes deletarPagina ). Por fim, o princípio de uma palavra por conceito sugere que a equipe deve escolher um termo padrão para uma ação abstrata 
e mantê-lo em todo o projeto, evitando misturar sinônimos como obter para operações idênticas em contextos diferentes como: buscar , 
recuperar e obter.
"A diferença entre um programador inteligente e um programador profissional é que o 
profissional entende que a clareza é rei." 

Capítulo 4: Comentários (Comments)
No quarto capítulo, Robert Martin adota uma postura que pode parecer um tanto radical 
para muitos iniciantes: ele argumenta que "comentários são, na melhor das hipóteses, 
um mal necessário". A ideia central é que, muitas vezes, usamos comentários para 
compensar nossa incapacidade de expressar nossas intenções de forma clara através do 
próprio código. A grande verdade sobre os comentários é que eles tendem a mentir com o tempo. À 
medida que o código evolui e é modificado, os comentários raramente são atualizados na 
mesma velocidade, tornando-se obsoletos e enganosos. O código, por outro lado, é a única 
fonte real da verdade. Por isso, a principal recomendação é: explique-se no código. Em vez 
de escrever um comentário para justificar uma lógica complexa ou uma "gambiarra", 
invista esse tempo refatorando o código para que ele se torne autoexplicativo.
Apesar dessa visão crítica, o autor reconhece que existem comentários bons, embora 
sejam raros. Estes incluem: comentários legais (como avisos de direitos autorais e licenças), 
comentários informativos (que explicam o retorno de uma expressão regular complexa, por 
exemplo), explicações de intenção (quando a decisão arquitetural por trás de um algoritmo 
não é óbvia) e avisos de consequências (alertas sobre efeitos colaterais, como um teste que 
demora muito para ser executado). Marcações temporárias como 
TODO também são aceitáveis, desde que sejam gerenciadas e limpas regularmente.
Em contrapartida, os comentários ruins devem ser eliminados sem piedade. Isso inclui: 
comentários redundantes (que repetem o que o nome da função já diz), comentários 
ruidosos (informações óbvias que apenas poluem o arquivo) e marcadores de posição 
excessivos (como // ************ ). A prática mais condenada, no entanto, é deixar código 
comentado no repositório. Com a chegada dos sistemas de controle de versão (como o Git), 
não há justificativa para manter código morto no arquivo; ele deve ser simplesmente apagado.

Capítulo 5: Formatação (Formatting)
O quinto capítulo aborda a formatação do código não apenas como uma questão 
estética, mas como uma forma vital de comunicação. Um código bem formatado mostra 
atenção aos detalhes e transmite profissionalismo. Enquanto a funcionalidade de um 
software pode mudar de uma versão para outra, a legibilidade do código tem um impacto 
duradouro em sua manutenção e evolução.
A formatação vertical é explicada através da "Metáfora do Jornal". Um arquivo de código
fonte deve ser lido como um artigo de jornal bem estruturado. O topo do arquivo deve 
apresentar os conceitos de alto nível e, à medida que a leitura avança para baixo, os 
detalhes de implementação devem se tornar mais granulares. A densidade e a distância 
vertical também são cruciais: conceitos fortemente relacionados devem estar próximos uns 
dos outros. Variáveis locais devem ser declaradas o mais perto possível de onde são 
utilizadas, e funções dependentes (a função que chama e a função que é chamada) devem 
estar adjacentes. Além disso, o autor sugere que arquivos menores (entre 200 e 500 linhas) 
são significativamente mais fáceis de compreender do que arquivos monolíticos.
Em relação à formatação horizontal, a regra de ouro é evitar linhas excessivamente longas 
que exijam rolagem horizontal por parte do leitor. Um limite razoável sugerido é de 
aproximadamente 120 caracteres por linha. A indentação é tratada como um elemento 
sagrado, pois ela revela visualmente a hierarquia e o escopo do código. A indentação nunca 
deve ser quebrada, mesmo em funções curtas de uma única linha. O uso inteligente de 
espaços em branco também é recomendado para associar termos fortemente 
relacionados e separar aqueles que possuem relação mais fraca.
O ponto culminante do capítulo sobre formatação é a importância das regras de equipe. 
Mais importante do que as preferências individuais de cada desenvolvedor é o consenso do 
time. A equipe deve concordar com um estilo único de formatação e aplicá-lo de forma 
consistente em todo o projeto. Não importa se a chave de abertura de um bloco fica na 
mesma linha ou na linha seguinte; o que realmente importa é que a padronização evite o 
"atrito visual" e permita que qualquer membro da equipe leia o código de forma fluida.
