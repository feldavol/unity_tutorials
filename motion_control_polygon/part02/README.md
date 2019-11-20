#  Motion Control Tutorial PARTE 2

Continuando a série de tutoriais envolvendo Motion Control para criar uma cena viva e interativa. Nessa segunda parte usaremos **Dialogue Tree** e **Behaviour Tree** dentro do asset **Node Canvas** para criar um diálogo com NPC, isso será feito passo a passo para seu melhor entendimento.

Link parte 01
* [Motion Control PARTE 01 - MOVIMENTAÇÃO](https://github.com/feldavol/unity_tutorials/tree/master/motion_control_polygon/part01)

##  Node Canvas
  Node Canvas é um conjunto de 3 ferramentas desenvolvidas pela **PARADOX NOTION** sendo as 3 incluídas nesse pacote.
Behaviour Tree - Ferramenta de acionamento e controle de comportamento
Dialogue Tree - Ferramenta de fluxo de diálogo
State Machine - Ferramenta de controle de estado

## Importação

O pacote que deve ser importado é de acordo com a imagem a seguir

![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/01.PNG)

E então a seguinte pasta deve aparecer nos seus assets
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/02.PNG)


![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/03.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/04.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/05.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/06.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/07.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/08.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/09.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/10.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/11.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/11a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/12.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/12a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/13.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/13a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/14.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/14a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/14b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/14c.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/15.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/15a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16c.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16d.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16e.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/16f.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/17.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/18.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/19.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/19a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/19b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/19c.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/19d.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/20a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/20ab.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/20c.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/21.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/22.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/22a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/22b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/22c.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/22d.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/23.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/23a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/23b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/24.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/24a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/24b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/24c.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/24d.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/24e.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25a.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25b.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25c.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25d.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25e.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25f.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25h.PNG)
![Image of Motion Controll Tutorial](https://raw.githubusercontent.com/feldavol/unity_tutorials/master/motion_control_polygon/images/part02/25i.PNG)
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






