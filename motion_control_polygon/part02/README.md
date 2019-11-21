#  Motion Control Tutorial PARTE 2

Continuando a série de tutoriais envolvendo Motion Control para criar uma cena viva e interativa. Nessa segunda parte usaremos **Dialogue Tree** e **Behaviour Tree** dentro do asset **Node Canvas** para criar um diálogo com NPC, isso será feito passo a passo para seu melhor entendimento.

Link parte 01
* [Motion Control PARTE 01 - MOVIMENTAÇÃO](https://github.com/feldavol/unity_tutorials/tree/master/motion_control_polygon/part01)

##  Node Canvas
  Node Canvas é um conjunto de 3 ferramentas desenvolvidas pela **PARADOX NOTION** sendo as 3 incluídas nesse pacote.
* Behaviour Tree - Ferramenta de acionamento e controle de comportamento.
* Dialogue Tree - Ferramenta de fluxo de diálogo.
* State Machine - Ferramenta de controle de estado.

## Importação

O pacote que deve ser importado é de acordo com a imagem a seguir.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/01.PNG)

E então a seguinte pasta deve aparecer nos seus assets.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/02.PNG)

## Criando Dialogue Trees

Primeiro crie um Game Object chamado **Dialogues** é nele que colocaremos os objetos de diálogo da cena.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/03.PNG)

Depois para criar um diálogo vá em Tools> Paradox Notion>Create>Dialogue Tree Object.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/04.PNG)

Em seguida mova a Dialogue Tree para dentro do Objeto Dialogues de antes.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/05.PNG)

Agora vamos editar essa Dialogue Tree. Clique no objeto Dialogue Tree e depois clique em Edit Dialogue Tree.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/06.PNG)

E então teremos a seguinte tela.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/08.PNG)

 Clicando com o botão direito de nesta tela teremos a seguinte pop up e nela o botão Say é o mais importante ou pelo menos o mais usado já que essa é a tela de diálogos.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/09.PNG)

Logo abaixo temos um botão de Task Action que aciona uma ação durante o diálogo.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/10.PNG)

Logo em seguida temos a pasta Branch que é uma pasta onde podemos encontrar tipos de caixa para diálogo diferente.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/11.PNG)

Como as que temos a seguir cada uma tem uma função diferente:
* Multiple Choice  - Diálogo com múltipla escolha
* Multiple Task Condition - Caixa com múltiplas ações
* Probability Selector - Caixa de que seleciona um ramo ligado a ele de acordo com a chance de acontecer aquele ramo pode variar 
* Task Condition - Executa um ramo se uma condição for verdadeira

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/11a.PNG)

A pasta Control e para controlar o fluxo do diálogo e decide se será pulado uma parte ou o diálogo encerra.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/12.PNG)

O FINISH encerra o diálogo e JUMP pula para uma outra parte do diálogo de acordo com a identificação que tem nas caixas de diálogo

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/12a.PNG)

Em Nested você pode usar  para vincular uma Sub Dialogue Tree em uma Diálogo

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/13.PNG)

Usando o Botão abaixo.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/13a.PNG).

` Essas são as opções que temos para criar um diálogo,  não explorarei todos aqui mas uma parte será usada `

### Montando um Diálogo

Crie uma caixa Say ela você verá que nela temos um START em cima dela, E por ela que o Dialogo se da inicio.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/14.PNG)
Clicando nessa caixa você verá o uma caixa no canto esquerdo superior nela temos
* Uma caixa onde podemos adicionar um texto.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/14a.PNG)

* Uma caixa para adicionar um áudio que será tocado quando aquele diálogo for chamado 

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/14b.PNG)

* Uma selection Box onde você pode selecionar um interlocutor como base ele vem apenas com um **INSTIGATOR**

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/14c.PNG)

Para adicionar novo interlocutores volte no Game Object  com a Dialogue Tree e em Dialogue Actor Parameters clique em Add Actor Parameter.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/07.PNG)

Ao adicionar você verá que aparece 2 parâmetros 1 para você colocar o nome do actor e um campo para Dialogue Actor.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/15a.PNG)

Para adicionar um Dialogue Actor aqui precisamos ter um personagem que tenha esse componente, vamos adicionar ele no nosso Player que fizemos na primeira parte deste tutorial.Clique nele e então em Add Componente.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16.PNG)

Bosque por Dialogue Actor.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16a.PNG)

No componente Dialogue actor você verá alguns parâmetros.



![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16b.PNG)

* Primeiro o Nome do Actor.


![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16c.PNG)

* Depois Portait, que é uma imagem que aparecerá quando esse actor for acionado A.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16d.PNG)


* A cor do texto que esse Actor terá.

![Image of Motion Controll.
Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16e.PNG)

* As configuração de posição do diálogo desse actor.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16f.PNG)

* Agora voltando na Dialogue Tree mude o nome  do actor para qual você desejar e adicione o  Dialogue Actor do player.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/17.PNG)

Agora com o Dialogue Actor criado podemos ver como possível interlocutor para as caixas de diálogo.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/18.PNG)

Agora vamos duas caixas de diálogo .

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/19.PNG)

E uma caixa de controle FINISH.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/19a.PNG)

Escolha seu Player como um interlocutor e escreva um diálogo.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/19b.PNG)

Ponha Instigator e ponha a resposta para o diálogo.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/19c.PNG)

Você deve ter algo parecido com isso.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/19d.PNG)

Agora precisamos adicionar algumas coisas ao Player 

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/20a.PNG)

Troque a Tag do Player e clique em ADD COMPONENT

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/20b.PNG)

Em seguida adicione um *Rigidbody* e um * capsule colíder* a deixei com as configurações a seguir.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/20c.PNG)


## Configurando NPCs
Crie um Game Object chamado NPCs e ponha ele na posição (0,0,0)


![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/21.PNG)

Vamos na pasta de Characters do Polygon Town e escolha um que você preferir.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/22.PNG)

Coloque ele dentro do Game Object NPC e mude a posição do X e Z só pra ele nao ficar em cima do player.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/22a.PNG)

Agora nesse objeto vamos adicionar alguns outros componentes.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/22b.PNG)

Um dialogue Actor com o nome que você quiser

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/22c.PNG)

Depois uma sphere collider marcada como Trigger e com a configuração abaixo.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/22d.PNG)

Agora você vai adicionar esse Dialogue actor na sua dialogue tree igual você fez com o player só clicar em add actor parameter na dialogue tree

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/23.PNG)

e arrastar ele para o espaço do dialogue actor.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/23a.PNG)

Ponha o nome do interlocutor ele deve ficar algo parecido com isso.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/23b.PNG)

Agora vamos adicionar um novo componente no NPC que você adiciono.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/24.PNG)

Vamos adicionar uma Behaviour Tree junto dela vem um Blackboard que serve para adicionar variáveis.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/24a.PNG)

Agora clique em create new para criar uma nova behaviour tree.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/24b.PNG)

Você verá esse pop up, Você terá duas opções asset ou bound.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/24c.PNG)

Asset você criar um arquivo que pode ser reutilizado em outros prefabs.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/24d.PNG)

Ou Bound que é para esse objeto específico.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/24e.PNG)
` Usaremos Bound!! ` 

A tela do Behaviour Tree é bem parecida com a do Dialogue Tree Aperte o botão direito.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25.PNG)
E você terá essa tela.
* **Action** insere um bloco para criar uma ação que o dono dessa tree vai fazer

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25a.PNG)

* **Condition** insere um bloco para criar uma condição para que algo aconteça.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25b.PNG)

* **Composites** servem para controlar o fluxo dos blocos.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25c.PNG)

` Cada Composites tem uma característica diferente que faz com que você possa criar diversas lógicas para comportamento diferente abaixo tem a lista com todos `

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25d.PNG)

* **Decorators**  servem para adicionar um novo comportamento para um ramo da tree.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25e.PNG)

` Assim como os Composites existem vários decorators e cada um com uma peculiaridade abaixo tem a lista com todos `

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25f.PNG)

* **Nested**  com ele você pode criar um nó que leva para outra Behaviour Tree ou State machine

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25h.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25i.PNG)

## Montando Behaviour Tree









![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26c.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26d.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26e.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26f.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26g.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26h.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26i.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26j.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26k.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26l.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26m.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26n.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26o.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26p.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26q.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/27.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/27a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/27b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/27c.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/27d.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/28.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/29.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/29a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/29b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/29c.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/29d.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30c.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30d.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30e.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30f.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/31.PNG)

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/31a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/31b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/31c.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/31d.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/31e.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/32.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/32a.PNG)

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/32b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/32c.PNG)

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/33.PNG)

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/34.PNG)

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/35a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/35.PNG)







