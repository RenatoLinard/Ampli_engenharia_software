# Introdução

Nesta seção, serão apresentados os conceitos, características, hierarquia e os estados dos processos e 
threads, bem como a criação e o término de processos.

Os processos são tarefas ou programas em execução, e o Sistema Operacional é responsável por 
administrá-los por meio do gerenciador de processos.

Existem os processos iniciados pelo usuário e também os processos iniciados por outros processos.

# Processos: Conceito e Criação 

Nos computadores, os processadores funcionam como uma linha de produção, executando vários programas ao mesmo
tempo de forma sequencial. A CPU é responsável por alternar os programas, executando-os por frações de 
segundo, para que cada um tenha acesso ao processamento, dando a ilusão ao usuário de paralelismo.

O paralelismo, ou pseudoparalelismo, é a falsa impressão de que os programas estão sendo executados ao 
mesmo tempo, mas o que realmente acontece é que o processo de um programa é suspenso temporariamente para
dar lugar ao processamento de outro.

Um modelo foi desenvolvido para lidar com o paralelismo de forma mais fácil, organizando os programas 
executáveis em processos sequenciais. Um processo pode ser entendido como um programa em execução, incluindo
não apenas o código em si, mas também informações importantes como o valor do contador de programa atual,
registradores e variáveis.

A alternância entre processos, que ocorre constantemente na CPU, é conhecida como multiprogramação. Isso 
significa que, em um ambiente multiprogramado, a CPU não está dedicada a executar apenas um único processo
de cada vez. Em vez disso, ela alternadamente executa diversos processos em rápida sucessão, o que dá a 
impressão de que múltiplos programas estão sendo executados simultaneamente.

A diferença entre programa e processo é importante para que o modelo seja entendido.

A analogia utilizada para exemplificar a diferença entre processo e programa é fazer um bolo. Para fazer 
um bolo, são necessários todos os ingredientes e a receita. A receita pode ser considerada como o programa
, os ingredientes são os dados de entrada e a pessoa que prepara o bolo é o processador.

Os processos são as atividades que a pessoa faz durante a preparação do bolo: ler a receita, buscar os 
ingredientes, misturar a massa e colocar o bolo para assar, que é o processo final desse programa "receita 
de bolo".

Continuando com o exemplo, imagine que o filho da pessoa que está fazendo o bolo tenha se machucado. A 
pessoa guarda em que parte do processamento parou e vai socorrer o filho. Ela pega o kit de primeiros 
socorros e lê o procedimento para tratar do machucado do filho. Neste momento, vemos o processador (a pessoa) 
alternando de um processo (fazer o bolo) para outro processo com prioridade maior (socorrer o filho), 
cada um com seu programa – receita versus procedimento de tratamento do machucado. Assim que o filho 
estiver medicado, então a pessoa retornará a fazer o bolo do ponto em que parou.

Podemos considerar então que um processo é uma atividade que contém um programa, uma entrada, uma saída e
um estado. A seguir, veremos a criação de processos e os estados dos processos.

Os serviços que os Sistemas Operacionais podem implementar incluem:

- Auditoria e segurança do sistema
- Contabilização do uso dos recursos
- Contabilização de erros
- Gerenciamento de impressão
- Comunicação de eventos
- Serviços de rede
- Interface de comandos (shell)

## Criação de Processos

Os sistemas operacionais devem oferecer formas para que os processos sejam criados. Portanto, existem 
quatro eventos que fazem com que um processo seja criado:

1. **Inicio do sistema:** Quando o sistema é inicializado, são criados vários processos. Os de primeiro 
plano interagem com o usuário e suas aplicações, enquanto os de segundo plano possuem alguma função 
específica, como atualizar emails quando uma mensagem é recebida. Para visualizar os processos no Windows, 
utiliza-se o comando Ctrl + Alt + Del e no Linux, o comando `ps`.

2. **Execução de uma chamada ao sistema de criação por um processo em execução:** Por exemplo, quando um 
processo está fazendo um download e aciona outro para armazenar os dados.

3. **Requisição do usuário para criar um novo processo:** Isso acontece quando o usuário digita algum 
comando ou clica em algum ícone para abrir um programa.

4. **Inicio de um job em lote:** Esses são criados em mainframes (computadores de grande porte).

## Término de Processos

Após a criação, um processo pode ser finalizado nas seguintes condições:

1. **Saída normal (voluntária):** O processo finaliza após concluir seu trabalho de forma adequada.

2. **Saída por erro (voluntária):** Ocorre quando um processo tenta acessar um arquivo que não existe, 
e o sistema emite uma chamada de saída. Em alguns casos, uma caixa de diálogo pode ser exibida perguntando 
se o usuário deseja tentar executar novamente.

3. **Erro fatal (involuntário):** O processo é finalizado devido a um erro de programa, como a execução 
ilegal de uma instrução ou a divisão por zero. Nessas situações, um processo com prioridade máxima 
supervisiona os demais processos e impede a continuação em situações ilegais.

4. **Cancelamento por outro processo:** Um processo com permissão pode emitir uma chamada para cancelar 
outro processo.

# Hierarquia de Processos

Em alguns sistemas, quando um processo cria outro, o processo-pai fica associado ao processo-filho, e o 
filho pode criar outros processos, criando assim uma hierarquia de processos.

No Unix, o processo-pai, filhos e descendentes formam um grupo de processos. Por exemplo, quando o usuário 
envia um sinal de teclado, este sinal é entregue para todos os processos que compõem o grupo de processos 
do teclado. Quando um processo-pai é morto, todos os outros vinculados a ele também são finalizados.

No Windows, não há uma hierarquia de processo clara. Cada processo possui um identificador próprio e, 
quando um cria outro, há uma ligação entre eles, mas essa ligação pode ser quebrada quando um processo-pai 
passa seu identificador para outro processo. Quando o processo-pai é finalizado, os processos vinculados 
a ele não são automaticamente finalizados.

## Estados de Processos

Durante o processamento, os processos podem passar por diferentes estados. Um processo ativo pode estar 
em três estados:

1. **Em execução:** Quando está sendo processado pela CPU, os processos são alternados para utilização do 
processador.

2. **Pronto:** Quando possui todas as condições necessárias para executar e está aguardando. O sistema 
operacional decide a ordem e os critérios para a execução dos processos.

3. **Espera ou bloqueado:** Quando está aguardando um evento externo, como um comando do usuário ou por 
um recurso para executar.

Quatro mudanças podem acontecer entre os estados:

1. **Execução para Bloqueado:** Quando um processo passa a aguardar um evento externo ou uma operação de 
E/S e não consegue continuar o processamento.

2. **Execução para Pronto:** Essa transição é realizada pelo escalonador sem que o processo tenha conhecimento. 
O escalonador de processos tem a função de decidir em qual momento cada processo será executado. Nessa 
segunda transição, o escalonador decide que o processo já teve tempo suficiente para execução.

3. **Pronto para Execução:** Nessa terceira transição, ocorre quando outros processos já tiveram seu tempo 
de execução e o escalonador permite a execução do processo que estava aguardando.

4. **Bloqueado para Pronto:** Quando o evento externo ou a operação de E/S ocorre, o processo retorna para 
a fila de processamento.

# Threads

Threads, ou "segmentos de execução", são unidades menores de processamento que podem ser executadas de 
forma independente dentro de um processo. Enquanto os processos representam programas em execução com seus 
próprios espaços de memória e recursos, as threads compartilham os mesmos espaços de memória e recursos 
dentro de um processo, possibilitando que sejam criadas e destruídas mais rapidamente, pois não exigem a 
alocação de novos espaços de memória.

Os processos podem conter uma ou mais threads dentro de si, compartilhando os mesmos recursos do processo.

A utilização das threads é fundamental nas aplicações modernas devido à necessidade de lidar com múltiplas 
atividades simultâneas. Aplicações compostas por threads possuem atividades sendo executadas em paralelo, 
o que melhora o desempenho e a eficiência do sistema. Outra vantagem das threads é na criação e destruição 
por não terem recursos vinculados a elas.

Quando uma aplicação processa muitas informações de E/S, o uso das threads acelera a execução das aplicações.

## Implementação de Processos 

A implementação do modelo de processos em sistemas operacionais envolve manter um quadro de processos 
contendo informações cruciais sobre cada processo em execução, como estado, contador de programa, ponteiro 
da pilha, alocação de memória e status dos arquivos abertos. Essas informações permitem que o sistema 
operacional reinicie um processo a partir do ponto em que ele foi interrompido, garantindo uma execução 
eficiente e concorrente de múltiplos processos.

## Implementação de Threads

A implementação de threads pode ocorrer no espaço do usuário, no núcleo do SO ou em uma implementação híbrida.

1. **Thread de usuário:** São criadas e gerenciadas no espaço de usuário que as criou, pela própria 
aplicação do usuário, sem que o SO tenha conhecimento direto delas. Não há necessidade de transição para 
o modo kernel do SO. Sua vantagem é a agilidade e eficiência.

2. **Thread do núcleo:** São implementadas e gerenciadas pelo núcleo do SO. Possuem uma menor performance, 
pois o gerenciamento é feito através de chamadas ao sistema.

3. **Threads híbridas:** São implementadas tanto no espaço do usuário quanto no núcleo do sistema 
operacional. Nesse modelo, o sistema operacional tem conhecimento das threads criadas pela aplicação e 
realiza seu gerenciamento. Uma das principais vantagens desse tipo de implementação é a flexibilidade que ela proporciona.
