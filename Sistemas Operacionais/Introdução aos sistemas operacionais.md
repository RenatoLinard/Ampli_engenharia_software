# Sistemas Operacionais: Uma Visão Abrangente

## Introdução 

Esta seção explora as diversas aplicações dos sistemas operacionais, destacando como diferentes tipos 
são empregados em várias situações na área de Tecnologia da Informação.

Os conceitos fundamentais dos sistemas operacionais, como segurança, permissão de acesso, armazenamento 
de dados e recuperação de informações, permeiam todas as vertentes da TI. Dominar esses conceitos aprimora 
as habilidades dos profissionais de TI em suas esferas de atuação.

Os Sistemas Operacionais evoluíram em paralelo ao progresso dos computadores. Inicialmente, sem sistemas 
operacionais, os computadores eram manipulados manualmente. Atualmente, esses sistemas desempenham 
diversas funções, assumindo o controle efetivo do hardware e facilitando tanto o usuário quanto os 
programadores.

## Definição, Conceitos e Breve Histórico dos Sistemas Operacionais

De acordo com Tanenbaum (2003), o sistema operacional é uma parte crucial de qualquer sistema computacional. 
Sem eles, os sistemas funcionariam, mas o usuário teria que compreender detalhes de hardware, tornando 
o processo complexo.

Um sistema computacional é composto por hardware e software. Os hardwares são os componentes físicos, 
enquanto o software consiste em programas instalados no hardware para executar tarefas específicas.

O sistema operacional controla o computador, gerenciando recursos de hardware e facilitando a interação 
entre hardware e software. Ele conecta eficientemente o usuário do computador aos componentes físicos, 
garantindo a integridade e segurança dos dados.

Conforme Machado (1997), ao ligar, o computador executa o sistema operacional, que gerencia recursos até 
o desligamento. O propósito é efetuar o gerenciamento eficiente e produtivo do computador.

### Breve Histórico dos Sistemas Operacionais

A evolução dos sistemas operacionais acompanhou o avanço da arquitetura dos computadores. As gerações 
incluem válvulas na primeira (1945-1955), transistores na segunda (1955-1965) e Circuitos Integrados na 
terceira (1965-1980). A terceira geração introduziu a multiprogramação e o conceito de compartilhamento 
de tempo.

A quarta geração (1980 até o presente) marcou a era dos computadores pessoais, com MS-DOS e Unix. O 
desenvolvimento de interfaces gráficas iniciou a evolução para o Windows.

# Principais Funções e Serviços dos Sistemas Operacionais 

**As funções dos sistemas operacionais são: estender a máquina e gerenciar os recursos (TANENBAUM, 2003).** 

## Estender a Máquina 

O sistema operacional como máquina estendida esconde a complexidade do hardware do programador, proporcionando 
abstração. Um exemplo é considerar cada dispositivo físico como um arquivo.

## Gerenciar os Recursos 

O gerenciamento de recursos é essencial para controlar e compartilhar ordenadamente os recursos do 
computador. Suas funções incluem garantir a ordem na distribuição de recursos, monitorar a utilização, 
mediar conflitos e garantir atendimento de requisições.

O sistema operacional controla e compartilha recursos do computador de forma ordenada, garantindo 
integridade das operações em andamento.

## Principais Serviços do Sistema Operacional 

1. **Carregamento e Execução de Programas:**
   - Facilita o carregamento e execução de programas na memória.

2. **Sistema de Arquivos:**
   - Permite criação, leitura, escrita e exclusão de arquivos, organizando e gerenciando dados eficientemente.

3. **Interface de Acesso a Periféricos:**
   - Oferece interface para acessar periféricos, facilitando interação com dispositivos externos.

4. **Monitoramento de Recursos:**
   - Implementa mecanismos de monitoramento para otimizar o desempenho do sistema.

5. **Armazenamento e Manutenção do Estado do Sistema:**
   - Fornece meios para armazenar e manter o estado do sistema, assegurando consistência e continuidade.

# Evolução dos Sistemas Operacionais 

## Introdução 

Nesta seção, exploramos a estrutura interna, os tipos e aprendemos sobre sistemas operacionais 
monoprogramáveis, multiprogramáveis e com múltiplos processadores.

Os sistemas operacionais modernos gerenciam eficientemente vários programas simultâneos, graças à 
capacidade multitarefa.

## Núcleo do Sistema Operacional 

O sistema operacional é essencialmente constituído por um conjunto de rotinas chamado kernel. O kernel 
é responsável pelo gerenciamento dos recursos do computador.

As principais funções do kernel, conforme Siqueira (2018), incluem tratamento de interrupções, 
gerenciamento de processos, memória, sistemas de arquivos, dispositivos de entrada/saída, auditoria e 
segurança do sistema.

Os sistemas operacionais restringem ações dos programas para garantir segurança e estabilidade. Os modos 
de acesso determinam os privilégios de execução, ocorrendo em modo usuário e kernel.

## Modelos das Principais Arquiteturas dos Sistemas Operacionais

### Sistemas Monolíticos

Desenvolvidos como módulos compilados separadamente, agrupados em um executável. Exemplo 
notável é o MS-DOS.

### Sistemas em Camadas

Organizam-se como uma hierarquia de camadas construídas uma sobre a outra.

### Máquinas Virtuais

Criam um nível intermediário entre o sistema operacional e o hardware, permitindo várias máquinas 
virtuais independentes.

### Modo Cliente-Servidor

Ênfase na implementação da maioria das funções em modo usuário, com o kernel concentrando-se na 
comunicação entre cliente e servidor.

## Classificação dos Sistemas Operacionais

Conforme Machado e Maia (2007), os sistemas operacionais podem ser monoprogramáveis, multiprogramáveis 
e com múltiplos processadores.

1. **Monoprogramáveis/Monotarefa:**
   - Executam um único programa por vez, alocando todos os recursos da máquina para o programa em 
   execução. Exemplo: MS-DOS.

2. **Multiprogramáveis/Multitarefa:**
   - Compartilham recursos entre vários programas, evitando ociosidade da CPU. Classificação baseada 
   no número de usuários e maneira de gerenciamento de aplicações.

    - **Número de

 Usuários:**
        - *Monousuários:* Um usuário utiliza os recursos.
        - *Multiusuário:* Múltiplos usuários compartilham recursos.

    - **Maneira de Gerenciamento de Aplicações:**
        - *Sistema Batch:* Processamento por lotes de registros.
        - *Sistemas de Tempo Compartilhado:* Permite execução simultânea de vários programas.
        - *Sistemas de Tempo Real:* Prazos rigorosos para execução de tarefas.

3. **Sistemas com Múltiplos Processadores:**
   - Integram duas ou mais CPUs em um único sistema, permitindo execução simultânea de diversos programas.

### Classificação dos Sistemas com Múltiplos Processadores

#### 1. Sistemas Fortemente Acoplados:

   - **Simétricos:**
     - Processadores compartilham memória e usam o mesmo sistema operacional, permitindo paralelismo.

   - **Assimétricos:**
     - Um processador principal controla o sistema e distribui tarefas.

#### 2. Sistemas Fracamente Acoplados:

   - Funcionam de forma independente, cada um com seu próprio sistema operacional e gestão de recursos.

Esta classificação oferece uma visão abrangente das configurações de sistemas com múltiplos processadores, 
considerando o nível de acoplamento entre os componentes e a autonomia operacional de cada sistema.

# Características e composição dos sistemas operacionais

## Tipos de Sistemas Operacionais

Com o avanço dos computadores, incorporando maior eficiência e praticidade em sua arquitetura, os sistemas 
operacionais precisam evoluir para atender às necessidades dos dispositivos.

### Sistemas Operacionais Embarcados
Esses sistemas são empregados em dispositivos portáteis, como smartphones, televisores e micro-ondas. 
Possuem características de sistemas operacionais de tempo real, no entanto, apresentam limitações de 
memória e consumo de energia. Um exemplo notável é o WebOS.

### Sistemas Operacionais Mobile
Encontrados em celulares e tablets, esses sistemas são simples e permitem a comunicação de dados sem fio. 
Exemplos incluem Android e iOS.

### Sistemas Operacionais na Nuvem
Nesse modelo, todos os serviços, como bancos de dados e redes, são executados pela internet. Os dados do 
usuário são armazenados na nuvem. Um exemplo notável é o Chrome OS.

### Sistemas Operacionais de Cartões Inteligentes
Estes são os menores sistemas operacionais, dispositivos do tamanho de um cartão de crédito que 
contêm um chip de CPU.

## Sistema Operacional Unix

O Unix foi inicialmente desenvolvido em assembly, mas para facilitar sua adaptação a diferentes 
plataformas, foi reescrito em linguagem C.

Trata-se de um sistema multiprogramável e multiusuário que suporta multiprocessadores e implementa 
memória virtual. Sua escrita em uma linguagem de alto nível o torna de fácil compreensão e portabilidade 
para diversas plataformas. A flexibilidade do Unix permite sua utilização em diversas aplicações, oferecendo 
suporte a protocolos de rede, um sistema de arquivos e uma interface simples e uniforme com os 
dispositivos de entrada/saída.

O sistema é baseado em uma estrutura monolítica, onde as funções são executadas no modo núcleo. Ele é composto por:

- **Kernel:** O núcleo do sistema operacional, dividido em duas partes:
    - **Dependente do hardware:** Formada por conjuntos de instruções específicas para lidar com 
    interrupções e situações excepcionais. Esta parte precisa ser reescrita ou adaptada durante a 
    instalação do sistema.
    - **Independente do hardware:** Não está vinculada ou dependente de uma plataforma específica onde 
    está sendo executada. Essa parte do sistema é responsável por tarefas como o tratamento de chamadas 
    de sistema (system calls), a gestão de processos, a gestão de memória e outras funções.

- **Shell:** Responsável pela interação do sistema operacional com o usuário por meio da linha de comando. 
Sua função é ler e interpretar os comandos, criando processos conforme necessário.

- **Sistema de Arquivos:** Responsável pela organização dos dados armazenados por meio de arquivos e diretórios.

- **Aplicações:** Refere-se às aplicações utilizadas pelo usuário.

## Sistema Operacional Linux

O sistema operacional Linux foi desenvolvido por Linus Torvalds, inspirado nas características do sistema 
Minix. O termo "Linux" refere-se especificamente ao kernel do sistema.

Os programas que interagem com o kernel foram desenvolvidos pela Fundação GNU. Vale destacar que o Linux, 
por si só, é apenas o kernel, sendo necessário incluir ferramentas como o compilador de código-fonte 
para seu pleno funcionamento. Por essa razão, é correto denominá-lo como GNU/Linux.

O sistema cresceu rapidamente com a contribuição de diversos colaboradores ao redor do mundo, 
participando do desenvolvimento do kernel, utilitários e aplicativos. Atualmente, é utilizado tanto para 
fins acadêmicos quanto comerciais, podendo ser obtido sem custos, juntamente com o código-fonte.

Reconhecido por sua flexibilidade e adaptabilidade às necessidades do usuário, o Linux também destaca-se 
por sua compatibilidade com diversos hardwares, oferecendo alta estabilidade e desempenho.

Sua estrutura é baseada no modelo monolítico, compartilhando características e composição com o UNIX.

O Linux possui várias distribuições disponíveis, e cada uma apresenta características específicas para 
atender às diversas necessidades dos usuários.

Licenciado pela GNU, o Linux permite que os usuários o baixem e utilizem em quantas máquinas desejarem. 
Com código-fonte aberto, proporciona uma administração efetiva do sistema por meio da linha de comando, 
além de oferecer um ambiente gráfico adaptável às preferências do usuário.

## Sistema Operacional Windows

Lançado inicialmente em 1981 como MS-DOS com interface em linha de comando e tinha as caracteristicas de ser 
monoprogramavel e monousuario.

A microsoft decidiu dar ao MS-DOS uma interface grafica chamada windows. As primieiras versões do windows não 
eram sistemas operacionais e sim uma interface grafica execuntando sobre o MS-DOS.

O windows 95 foi lançado e quase todas as caracteristicas da parte do MS-DOS foram transfeirdos para a parte do windows 
porem sem eliminar totalmente o MS-DOS, logo apos foi lançado o windows 98 que tinha poucas diferenças em relação ao 95.

O windows 2000 é uma evolução do NT lançado em 93 com um diferencial de oferecer serviços orientados e ambientes 
distribuidos  e de rede. Escrito em C proporcianando robustez,  confiabilidade, facilidade de manutenção do sistema, 
portabilidade e desempenho.

A estrutura do windows 2000 pode ser divida em duas parte:

   - modo nuclueo: gerencia memoria, processos, sistemas de arquivos
   - modo usuario: onde ficam os subsistemas do ambiente e interagem atravez de mensagens

# Sistema Operacional Windows

Lançado inicialmente em 1981 como MS-DOS, com uma interface em linha de comando, o Windows tinha características de ser 
monoprogramável e monousuário.

A Microsoft decidiu adicionar uma interface gráfica ao MS-DOS, chamada Windows. As primeiras versões do Windows não eram 
sistemas operacionais completos, mas sim uma interface gráfica que rodava sobre o MS-DOS.

O Windows 95 foi lançado, transferindo quase todas as características da parte do MS-DOS para a parte do Windows, porém 
sem eliminar completamente o MS-DOS. Logo após, foi lançado o Windows 98, que apresentava poucas diferenças em relação ao 95.

O Windows 2000 é uma evolução do NT, lançado em 1993, com o diferencial de oferecer serviços orientados e ambientes 
distribuídos e de rede. Escrito em C, proporciona robustez, confiabilidade, facilidade de manutenção do sistema, portabilidade e desempenho.

A estrutura do Windows 2000 pode ser dividida em duas partes:

- Modo núcleo: gerencia memória, processos e sistemas de arquivos.
- Modo usuário: onde ficam os subsistemas do ambiente e interagem por meio de mensagens.
