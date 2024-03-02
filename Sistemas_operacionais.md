# Introdução 

Nesta seção, abordaremos as diversas aplicações dos sistemas operacionais e 
como diferentes tipos são empregados em diversas situações.

Os conceitos fundamentais dos sistemas operacionais, tais como segurança, 
permissão de acesso, armazenamento de dados, recuperação de informações, 
entre outros, permeiam todas as vertentes da área de Tecnologia da Informação. 
O domínio desses conceitos aprimora as habilidades do profissional de TI em 
sua esfera de atuação.

Os Sistemas Operacionais têm evoluído em paralelo ao progresso dos computadores. 
Inicialmente, inexistiam sistemas operacionais, e os computadores eram 
manipulados manualmente. Atualmente, esses sistemas desempenham diversas funções 
e oferecem serviços que facilitam tanto o usuário quanto os programadores em 
suas atividades, assumindo o controle efetivo do hardware disponível.

# Definição, Conceitos e Breve Histórico dos Sistemas Operacionais

Conforme Tanenbaum (2003), o sistema operacional é uma parte crucial de qualquer 
sistema computacional. Sem eles, os sistemas funcionariam, mas o usuário teria 
que compreender detalhes de hardware para operar o computador, tornando o 
processo bastante complexo.

Um sistema computacional é composto por hardware e software:

- Os hardwares são os componentes físicos do computador, incluindo a CPU 
(Unidade Central de Processamento), o processador, a memória, o mouse, o 
teclado, o monitor, entre outros.

- Por outro lado, o software consiste em programas (conjunto de instruções) 
instalados no hardware para executar tarefas específicas.

O sistema operacional é um software incumbido de controlar o computador, 
visando gerenciar os recursos de hardware, tais como processador, memória e 
periféricos (como teclado, mouse e impressora), dados, entre outros. Sua 
principal finalidade é facilitar a interação entre o hardware e o software, 
atuando como elo essencial entre o usuário do computador e os componentes físicos, 
além de desempenhar a crucial função de conectar eficientemente o hardware e o 
usuário do sistema.

Conforme Machado (1997), ao ser ligado, o computador inicia executando o 
sistema operacional, que se mantém ativo, gerenciando os recursos de hardware 
e software até o momento em que o computador é desligado. O propósito 
fundamental do sistema operacional é efetuar o gerenciamento eficiente e 
produtivo do computador, simplificando sua utilização. Além disso, o sistema 
operacional tem a responsabilidade de assegurar a integridade e a segurança dos 
dados durante todo o processo de processamento e armazenamento na memória.

## Breve histórico dos sistemas operacionais

Conforme Tanenbaum (2003), a evolução dos sistemas operacionais ocorreu em 
paralelo com o avanço da arquitetura dos computadores. A primeira geração de 
computadores abrangeu o período de 1945 a 1955, caracterizada pelo uso de 
válvulas e painéis de programação. Nessa fase, as máquinas eram volumosas, 
lentas e compostas por válvulas, ocupando espaços inteiros, com as operações 
conduzidas por uma única pessoa através de painéis de programação.

Nesse contexto, não havia sistemas operacionais nem linguagens de programação, 
e as máquinas se dedicavam principalmente a cálculos matemáticos como 
logaritmos, voltados para aplicações militares.

De acordo com Tanenbaum (2003), a segunda geração de computadores abrangeu 
o período de 1955 a 1965, caracterizada pelo uso de transistores e pela 
implementação de sistemas em lote, conhecidos como sistemas Batch em inglês. 
Nessa fase, emergiram os mainframes, computadores de grande porte. Contudo, 
apenas instituições de grande porte, como bancos e universidades, tinham acesso 
a essas tecnologias devido aos elevados custos envolvidos.

Outro fato é o surgimento das primeiras linguagens de programação Fortran e Assembly.

Conforme Tanenbaum (2003), a terceira geração de computadores abrangeu o 
período entre 1965 e 1980, caracterizada pela adoção de Circuitos Integrados e 
pelo desenvolvimento de sistemas de Multiprogramação. Nesta fase, os fabricantes 
de computadores disponibilizavam duas linhas de produtos distintas: os computadores 
científicos de grande porte, orientados a palavras, utilizados para cálculos 
numéricos na ciência e engenharia; e os computadores comerciais orientados a 
caracteres, empregados por instituições financeiras e companhias de seguros.

Entretanto, o desenvolvimento e a manutenção desses produtos apresentavam custos 
elevados. A fim de superar esse desafio, a IBM desenvolveu o OS/360. Essas 
máquinas compartilhavam uma arquitetura e conjunto de instruções idênticos, 
possibilitando sua utilização tanto para aplicações científicas quanto 
comerciais, oferecendo assim uma relação custo-benefício mais vantajosa.

Segundo Tanenbaum (2003), uma das técnicas desenvolvidas durante a terceira 
geração foi a multiprogramação, cujo propósito era possibilitar a execução 
simultânea de diversos programas, compartilhando os recursos de memória.

A demanda por respostas mais ágeis no processamento deu origem ao conceito de 
compartilhamento de tempo, também conhecido como timesharing. Essa abordagem 
envolve a divisão do tempo da CPU em intervalos para a execução de cada 
programa. Nesse período, foi concebido um sistema operacional capaz de 
suportar múltiplos usuários conectados simultaneamente, conhecido como 
Multics. Embora o projeto do Multics tenha introduzido conceitos inovadores, 
foi apenas nos anos subsequentes que surgiu o Unix, um sistema operacional 
verdadeiramente multitarefa e multiusuário.

A quarta geração de computadores, que se estende desde 1980 até a presente 
data, marca a era dos computadores pessoais. O rápido desenvolvimento dos 
circuitos integrados ou microchips (circuitos eletrônicos) foi o catalisador 
para a introdução dos computadores de uso pessoal.

Desde então, houve uma significativa evolução em termos de agilidade e 
praticidade desses dispositivos, que se tornaram mais compactos, velozes e 
acessíveis financeiramente. Os sistemas operacionais predominantes durante essa 
geração foram o MS-DOS e o Unix. Foi nesse período que se iniciou a 
utilização de interfaces gráficas, sendo o MS-DOS a base para a evolução que 
resultou no conhecido sistema operacional Windows.

# Principais funções e serviços dos sistemas operacionais 

**As funções dos sistemas operacionais são: estender a máquina e gerenciar os 
recursos (TANENBAUM, 2003).** 

## Estender a maquina 

A função do sistema operacional como uma máquina estendida é esconder a 
complexidade do hardware do programador, conhecida também como abstração.

Um exemplo notável desse comportamento é a abordagem do sistema operacional ao 
considerar cada dispositivo físico como um arquivo. Ao manipular esses arquivos 
por meio de comandos de leitura/escrita ou abrir/fechar, os quais podem ser 
bastante complexos devido à quantidade de parâmetros envolvidos, o sistema 
operacional assume a responsabilidade de controlar diretamente o dispositivo 
em relação ao hardware.

## Gerenciar os recursos 

O gerenciamento de recursos no sistema operacional é essencial para controlar 
de maneira organizada e compartilhada os recursos do computador, como memória, 
processador e dispositivos de E/S. Suas principais funções incluem garantir a 
ordem e justiça na distribuição de recursos, monitorar a utilização, mediar 
conflitos entre programas e usuários, e garantir o atendimento de requisições 
de recursos de acordo com prioridades estabelecidas.

Esse gerenciamento ocorre por meio do compartilhamento temporal, onde programas 
aguardam sua vez de utilizar um recurso determinado, e do compartilhamento 
espacial, permitindo que vários programas utilizem partes específicas do 
mesmo recurso simultaneamente. Isso resulta em maior eficiência e otimização 
no uso dos recursos do sistema.

O sistema operacional controla e compartilha recursos do computador de forma 
ordenada. Por exemplo, ao editar um texto e gravar dados simultaneamente, evita 
que ambos os programas acessem a memória ao mesmo tempo para evitar perda de 
dados e conflitos. Isso garante a integridade das operações em andamento.

## Principais serviços do sistema operacional 

O sistema operacional oferece diversos serviços essenciais para aplicativos de 
usuários e para si mesmo (MACHADO, 1997):

1. **Carregamento e Execução de Programas:**
   - Facilita o carregamento de programas na memória e a execução dos mesmos.

2. **Sistema de Arquivos:**
   - Permite a criação, leitura, escrita e exclusão de arquivos, proporcionando 
   organização e gerenciamento eficiente dos dados.

3. **Interface de Acesso a Periféricos:**
   - Oferece uma interface para acessar periféricos como impressoras, scanners, 
   câmeras e pen drives, facilitando a interação com dispositivos externos.

4. **Monitoramento de Recursos:**
   - Implementa mecanismos de monitoramento para identificar possíveis gargalos 
   no sistema, permitindo otimizações para melhor desempenho.

5. **Armazenamento e Manutenção do Estado do Sistema:**
   - Fornece meios para armazenar e manter o estado do sistema, assegurando 
   consistência e continuidade das operações.
