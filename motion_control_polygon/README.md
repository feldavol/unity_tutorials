
### Motion Control Basicos Tutorial

#### Introdução
Nesse texto será mostrado como fazer o uso das ferramentas da **OOTII**, **Motion Control** e **Camera Control**  em um modelo 3D da  desenvolvedora Synty Studios pacote Polygon City Characters.

#### Importação
Crie um novo projeto 3D e comece importando os pacotes de asset store em seus assets de acordo com o que  segue abaixo.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/01.PNG)

Agora que você entrou em assets procure e importe os pacotes a seguir. Caso não tenha você pode fazer a compra dele diretamente na Asset Store

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/02.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/03.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/04.PNG)

#### Preparação de Cenário
Dentro do projeto na Unity crie uma pasta Plugins e mova para ela as pastas ootii, polygon town e _TerrainAutoUpgrade

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/05.PNG)

Agora crie um objeto vazio e dentro dele ponha um plane e 4 cubes, apenas para ter um cenário simples

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/06.PNG)

O plane se chamará ‘Ground’ e terá as seguintes configurações

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/07.PNG)

Os cubos se chamaram ‘Walls” e cada um terá as configurações a seguir

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/08.PNG)

Primeira ‘Wall”

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/09.PNG)

Segunda ‘Wall’

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/10.PNG)

Terceira ‘Wall”

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/11.PNG)

Quarta ‘Wall’

#### Preparação de Personagem

Agora escolha um dos personagens dentro do prefab da Polygon de acordo com a imagem aberto você pode escolher qualquer um, sem se preocupar muito

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/12.PNG)

Depois de escolher o personagem  e arrastar ele pra “Scene” mude o nome do objeto para Player e escolha um controller para o animator dele de preferência  use o ‘Humanoid’ que vem com o motion control, depois disso adicione o componente “Motion Controller”

![Image of Motion Controll
Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/13.PNG)

Perceba que ao adicionar o Motion Controller ele também adiciona um Action Controller por ser uma dependência dele, deixaremos o Actor Controller no padrão e não mexemos nele aqui.  Clique em “Setup Input Entries” para configurar automaticamente o “Input Manager” do Unity, isso vai configurar de acordo com as necessidades do Motion Controller.

 `CASO QUEIRA FAZER UMA CONFIGURAÇÃO RÁPIDA PARA O MOVIMENTO DO PERSONAGEM É SO ESCOLHER UM DOS MOVEMENT STYLE DO MOTION CONTROLLER CADA UM COM UMA JOGABILIDADE DIFERENTE.`
 
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/14.PNG)

 Note que o Animator,Input Source e Camera Rig estão vazios, bem deixaremos eles assim por enquanto pois o motion controller os acha automaticamente na Scene durante a execução.
 
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/15.PNG)

Mas é claro que pra ele achar esses caras eles precisam existir então vamos criá-los crie 2 objetos vazios e os nomeie Input Source e Camera Rig, (O animator será a partir do componente que está usando o motion control)

##### Input Source

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/16.PNG)

No objeto “InputSource’ vamos adicionar o componente ‘Unity Input Source’ e caso tenha algum controle e queira usar é só ligar’ is Xbox Enabled’

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/17.PNG)

##### Camera Rig & Camera Controller

Na camera Rig arraste a Main Camera pra dentro dela(Lembre se ZERAR todos os valores de transformers da Main Camera), agora no objeto Camera Rig adicione o componente ‘Camera Controller.

`PERCEBA QUE NO CAMERA CONTROLLER EXISTEM  3 STYLES , VOCÊ PODE ESCOLHER UM DELES SE QUISER, CADA UM É UMA VISTA DIFERENTE `

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/18.PNG)

No camera Controller é importante adicionar o Input Source (apesar de ele encontrar sozinho) e o Anchor que é o objeto que a câmara irá focar então ponha o objeto player nele. Agora configure o ‘Anchor Offset’ de acordo com a imagem abaixo. Depois vamos da uma olhada no que tem na aba ‘Advanced’

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/19.PNG)

Aqui podemos adicionar diferente “Camera Motors”(são os tipos de comportamento da câmera) e podemos configurá-los de acordo, mas veremos isso em outra ocasião

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/19a.PNG)

Volte para basic e escolha o camera style “3rd Person Style” isso nos atendera bem.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/20.PNG)

Volte em advance e veja quais são os Motors que esse Style adicionou caso queira você pode configurá-los como quiser.

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/20a.PNG)

Para configurá-los é só clicar em um deles que a caixa com as configurações daquele motors estará disponível para você ajustar como preferir

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/20b.PNG)

##### Animações

Agora volte para o Player e em motion controller clique em advanced 

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/21.PNG)

Perceba que em advanced temos um Motion Layers clique no + para adicionar uma nova Motion Layers com o nome de Locomotion

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/21a.PNG)

Agora que você criou a Motion Layer clique nela e perceba a aba Motions aqui ficaram a animações bse do nosso personagem

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/21c.PNG)

Clique agora no + de Motions

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/21d.PNG)

Com isso agora você terá essa janela, com todas as animações do Motion Controller

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/22.PNG)


Nós usaremos as animações de acordo com as marcadas na imagem

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/22a.PNG)

Por enquanto a única que configuramos é a Walk Run Strafe com Walk Speed  =  2 e Run Speed = 5 caso queira algo mais rápido sinta-se livre mas não exagere.

`ALGUMAS PESSOAS GOSTAM QUE A MOVIMENTAÇÃO BASE SEJA RUN CASO VOCÊ SEJA UMA DELAS É SÓ HABILITAR ‘Default to Run’`

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/23.PNG)

#### Proximo do FIM
Agora vamos transformar nosso player em um prefab então crie uma pasta Prefab e arrete ele pra dentro dela , como esse personagem é originalmente um prefab do POLYGON aparecerá um POPUP , clique para criar um Original Prefab

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/EXTRA.PNG)

Pronto temos um personagem com os movimentos básicos de movimentação, comando mais complexos e outras funções do motion control serão exploradas mais no futuro

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/24.PNG)

MOVE  - w a s d  ou setas 
JUMP - space
RUN  - SHIFT (Se walk for Default)
WALK  - SHIFT (Se Run for Default) 
Running Jump - durante a corrida Space
