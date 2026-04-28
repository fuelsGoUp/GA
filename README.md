# Trabalho do Grau A

Editor de objetos

Feito por Vitor Hugo Silva

Instruções:

WASD move a camera, TAB muda o cubo selecionado, R modo de rotação usando as teclas X,Y,Z para rotacionar, T modo de translatação usando as teclas I,K,J,L,U,O para translatar a posição do selecionado, S para escalar usando UP e DOWN para aumentar ou diminuir a escala e P para perspectiva ortografica ou camera.

Detalhes tecnicos:

A maioria das instruções do programa como o LoaderObj e callbacks são executadas pela CPU, enquanto a GPU é encarregada de criar e transformar os vertices, criar os shaders e iluminação e assim dando output dos pixels na tela, existe algumas tarefas no qual a CPU trabalha com a GPU, sendo elas, arrays de vertices da CPU para a memoria da GPU, pointes para dizer a GPU como ler dados do vertex e tambem instruções da CPU para a GPU de quando executar outras funções como desenhar os vertices.

MeshData e Objeto são structs para armazenar dados de vertices, assim servindo como uma bandeja de dados para carregar na GPU, e o Objeto serve para representar objetos 3D com VAO com propriedades.

de shaders temos vertex e fragment, o vertex é um shader de vertice para calcular gl_Position que é uma projeção, já o fragment é para a iluminação Phong, com a diferenciação entre wireframe e normal.

LoaderOBJ para abrir arquivos do diretorio com nome obj"n", cria arrays de posição e normal e retorna MeshData com array e contagem com os valores v de vertices, vn de normais e f para faces, sendo faces dividias em v/vt/vn.

Antes do Main cria um shader no qual define a fonte de vertex e fragment e anexa em program, e compila.
