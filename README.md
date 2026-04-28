# Trabalho do Grau A

Editor de objetos

Feito por Vitor Hugo Silva

Instruções:

WASD move a camera, TAB muda o cubo selecionado, R modo de rotação usando as teclas X,Y,Z para rotacionar, T modo de translatação usando as teclas I,K,J,L,U,O para translatar a posição do selecionado, S para escalar usando UP e DOWN para aumentar ou diminuir a escala e P para perspectiva ortografica ou camera.

A maioria das instruções do programa como o LoaderObj e callbacks são executadas pela CPU, enquanto a GPU é encarregada de criar e transformar os vertices, criar os shaders e iluminação e assim dando output dos pixels na tela, existe algumas tarefas no qual a CPU trabalha com a GPU, sendo elas, arrays de vertices da CPU para a memoria da GPU, pointes para dizer a GPU como ler dados do vertex e tambem instruções da CPU para a GPU de quando executar outras funções como desenhar os vertices.
