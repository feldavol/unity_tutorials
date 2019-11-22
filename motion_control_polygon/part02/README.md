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

Vamos montar nosso comportamento simples visando apenas acionar um diálogo quando um objeto entra em um trigger. Por enquanto sem usar comandos adicionais apenas.

Entre em Composites.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26.PNG)

E selecione Sequencer.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26a.PNG)

Depois adicione um Condition.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26b.PNG)

E um Action.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26c.PNG)

Você terá isso, veja que nosso sequencer e o nosso **START**,  ou seja a raiz da nossa árvore. 

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26d.PNG)

Selecione o START e na caixa no canto superior esquerdo acione a check box de Dynamic.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26e.PNG)

Agora aperte na caixa do Condition (A que tem o  **?**) e clique em **Assign Condition Task**

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26f.PNG)

Você terá essa tela clique na busca.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26g.PNG)

E busque por **Trigger**, você vai selecionar em System Events o **Check Trigger**

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26h.PNG)

Em condition agora você terá a caixa abaixo. Escolha **Check Trigger Type** com **Trigger Enter** e marque a checkbox do **Specified Tag Only** 

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26j.PNG)

Vai aparecer um **Object Tag** selecione a Tag **Player**

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26k.PNG)

Agora selecione a caixa do action( A que tem o **!**) e clique em **Assign Action Task**

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26l.PNG)

Você terá essa janela clique na busca e procure por **Dialogue**

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26m.PNG)

Selecione a **Star Dialogue Tree**

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26n.PNG)

Agora na janela do Action você terá um Start Dialogue Tree, você perceberá que o **Dialogue Tree Controller** está vazio.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26o.PNG)

Clique e arraste na sua Dialogue Tree para esse campo, de acordo com a imagem a seguir.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26p.PNG)

E agora faça as ligações dos blocos com o a partir do seu bloco compositor sequencer e você terá algo parecido com isso.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/26q.PNG)

## Preparando Dialogue Canvas
Entre nas pastas seguir

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/27.PNG) ![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/27a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/27b.PNG) ![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/27c.PNG)

E selecione o prefab **@DialogeUGUI** e coloque ele na cena

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/27d.PNG)

Execute  e se aproxime do seu NPC se tudo esiver correto, você terá isso.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/28.PNG)

Com isso você tem um diálogo simple e funcional na sua cena. 
Agora vamos tentar melhorar isso tornar mais variado e funcional.

## EXTRA 

### Novas Dialogues Tree
 Vamos criar novas árvores de diálogo, Você pode repetir o processo da anterior  ou duplicar a já existente e configurar a partir daí.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/29.PNG)

Nessa nova Tree vamos em Brach e selecionar **Multiple Choice** 

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/29a.PNG)

Você terá o seguinte bloco.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/29b.PNG)

Ao clicar nele no canto esquerdo superior você verá um botão de **Add Choice**, eu clique 3 vezes para adicionar 3 alternativas você pode adicionar quantas vezes quiser e esse será o número de opções que você terá **(Só não exagere )**.

Veja que em cada bloco você tem um espaço para o texto um para um áudio e uma assing Condition Task.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/29c.PNG)

Veja como foi montada nossa Tree e se base no exemplo para construir a sua.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/29d.PNG)

Vamos fazer mais uma

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30.PNG)

Agora usando o Branch **Probability Selector**

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30a.PNG)

Ele esse é o bloco dele

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30b.PNG)

Ao clicar nele você verá uma informação que diz para fazer algumas conexões antes

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30c.PNG)

Eis um exemplo de conexões feitas com simples blocos de Fala(** Say ** )

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30d.PNG)

A fazer as conexões clique novamente no bloco do **Probability Selector** veja como está agora. Note que cada conexão tem uma porcentagem e um peso que faz com que elas acontecem com mais facilidade. 

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30e.PNG)

Um exemplo de como uma a Tree deve ficar 

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/30f.PNG)

### Criando mais NPCs
Primeiramente para que o nosso NPC não fique simplesmente parado adicione no **Controller** do **Animator** desse NPC, o mesmo Controller use o mesmo usado na parte 1 para o player que é o  **Humanoid**

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/31.PNG)

Agora duplique esse NPCe expando o objeto

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/31a.PNG)

Selecione o objeto interno dele que está visível e desative ele

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/31b.PNG)

 e depois escolha que estava inativo e ative ele

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/31c.PNG)

Mude a posição de dele para não sobrepor o outro.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/31d.PNG)

E mude também o ** Name ** do ** Dialogue Actor ** dele 

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/31e.PNG)

Clique para editar a Behaviour Tree dele.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/32.PNG)

Clique na **Action** que foi usada para começar o diálogo

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/32a.PNG)

E altere a dialogue tree vinculada nele.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/32b.PNG)

por uma das criadas anteriormente.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/32c.PNG)

Volte e selecione a dialogue tree que você colocou para esse personagem e altere o *Dialogue Actor Parameters* e ponha o desse personagem que você fez .

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/34.PNG)

Repita o processo para outros personagens.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/33.PNG)

 POR ENQUANTO PARA ESSA PARTE É SÓ,MAS ADICIONAREMOS MAIS CONTEÚDO USANDO NODE CANVAS PARA CRIAÇÃO DE DIÁLOGOS




