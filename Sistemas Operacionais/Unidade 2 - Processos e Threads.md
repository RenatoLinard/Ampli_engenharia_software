# Processos

Nesta seção, serão apresentados os conceitos, características, hierarquia e os estados dos processos e 
threads, bem como a criação e o término de processos.

Os processos são tarefas ou programas em execução, e o Sistema Operacional é responsável por 
administrá-los por meio do gerenciador de processos.

Existem os processos iniciados pelo usuário e também os processos iniciados por outros processos.

## Processos: Conceito e Criação 

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

### Criação de Processos

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

### Término de Processos

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

## Hierarquia de Processos

Em alguns sistemas, quando um processo cria outro, o processo-pai fica associado ao processo-filho, e o 
filho pode criar outros processos, criando assim uma hierarquia de processos.

No Unix, o processo-pai, filhos e descendentes formam um grupo de processos. Por exemplo, quando o usuário 
envia um sinal de teclado, este sinal é entregue para todos os processos que compõem o grupo de processos 
do teclado. Quando um processo-pai é morto, todos os outros vinculados a ele também são finalizados.

No Windows, não há uma hierarquia de processo clara. Cada processo possui um identificador próprio e, 
quando um cria outro, há uma ligação entre eles, mas essa ligação pode ser quebrada quando um processo-pai 
passa seu identificador para outro processo. Quando o processo-pai é finalizado, os processos vinculados 
a ele não são automaticamente finalizados.

### Estados de Processos

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

## Threads

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

### Implementação de Processos 

A implementação do modelo de processos em sistemas operacionais envolve manter um quadro de processos 
contendo informações cruciais sobre cada processo em execução, como estado, contador de programa, ponteiro 
da pilha, alocação de memória e status dos arquivos abertos. Essas informações permitem que o sistema 
operacional reinicie um processo a partir do ponto em que ele foi interrompido, garantindo uma execução 
eficiente e concorrente de múltiplos processos.

### Implementação de Threads

A implementação de threads pode ocorrer no espaço do usuário, no núcleo do SO ou em uma implementação híbrida.

1. **Thread de usuário:** São criadas e gerenciadas no espaço de usuário que as criou, pela própria 
aplicação do usuário, sem que o SO tenha conhecimento direto delas. Não há necessidade de transição para 
o modo kernel do SO. Sua vantagem é a agilidade e eficiência.

2. **Thread do núcleo:** São implementadas e gerenciadas pelo núcleo do SO. Possuem uma menor performance, 
pois o gerenciamento é feito através de chamadas ao sistema.

3. **Threads híbridas:** São implementadas tanto no espaço do usuário quanto no núcleo do sistema 
operacional. Nesse modelo, o sistema operacional tem conhecimento das threads criadas pela aplicação e 
realiza seu gerenciamento. Uma das principais vantagens desse tipo de implementação é a flexibilidade que ela proporciona.

## Conclusão

O problema de travamento de um software pode ocorrer tanto devido ao próprio software quanto ao hardware. 
Em tais casos, a abordagem correta é encerrar o processo e verificar se isso terá algum impacto sobre 
outros processos em execução.

A implementação de threads durante a execução de processos agiliza o processamento e melhora o desempenho 
das aplicações, permitindo a execução de duas ou mais tarefas simultaneamente.

# Comunicação entre Processos

No Sistema Operacional, os processos e threads trocam informações entre si ou solicitam a utilização de 
recursos simultaneamente, como arquivos, dispositivos de E/S e memória.

## Execução cooperativa de processos e threads

Em uma aplicação concorrente, onde ocorre a execução cooperativa de processos e threads, é necessário que 
os processos se comuniquem entre si e solicitem o uso de recursos, como memória, arquivos, dispositivos 
de E/S e registros.

Por exemplo, uma região da memória pode ser compartilhada entre vários processos. O Sistema Operacional 
precisa garantir que essa comunicação seja sincronizada para o bom funcionamento do sistema e execução 
correta das aplicações.

Três tópicos devem ser considerados:

1. Como um processo passa informações para outro.
2. Garantia de que os processos não invadam uns aos outros quando estiverem em regiões críticas. Quando 
um processo estiver utilizando uma região da memória, outro precisa aguardar sua vez.
3. Hierarquia necessária quando houver dependências. Se o processo A produz dados e o processo B os 
imprime, o B precisa aguardar o processo A produzir os dados para depois imprimi-los.

### Condições de disputa ou condições de corrida 

Condições de disputa, ou corrida, ocorrem em sistemas concorrentes quando dois ou mais processos ou 
threads estão compartilhando recursos, como uma região da memória, e o resultado final do programa 
depende da sequência específica de execução desses processos. Isso pode levar a comportamentos inesperados 
ou incorretos devido à natureza não determinística das operações concorrentes.

Por exemplo, se dois processos tentarem escrever na mesma região de memória simultaneamente, o resultado 
final pode depender da ordem em que essas operações ocorrem. Se um processo ler um valor antes que outro 
processo o altere, o resultado será diferente do que seria se a leitura ocorresse após a alteração. Essas 
situações podem levar a erros de lógica, corrupção de dados ou outros problemas no programa.

### Regiões críticas

Para evitar condições de disputa e garantir a consistência dos dados em sistemas concorrentes, é essencial 
implementar mecanismos de exclusão mútua. Esses mecanismos são projetados para permitir que apenas um processo 
ou thread tenha acesso exclusivo a uma região crítica da memória compartilhada em um determinado momento, 
enquanto outros processos ou threads aguardam sua vez.

A parte do programa em que um processo ou thread acessa a memória compartilhada é chamada de região 
crítica ou seção crítica.

Para uma boa solução, é necessário satisfazer quatro itens:

1. **Dois ou mais processos jamais estarão ao mesmo tempo em suas regiões críticas:** Isso significa que 
apenas um processo por vez pode estar executando em sua região crítica. Garante que não ocorram condições 
de disputa, onde múltiplos processos tentam acessar ou modificar os mesmos dados compartilhados simultaneamente.

2. **Não se pode afirmar nada sobre o número e a velocidade de CPUs:** Esse item reconhece que a solução 
para o problema de exclusão mútua deve ser independente da arquitetura de hardware subjacente, incluindo o 
número de processadores e suas velocidades. A solução deve funcionar de forma eficiente independentemente 
das características específicas do hardware.

3. **Nenhum processo que esteja executando fora de sua região crítica pode bloquear outros processos:** 
Isso garante que um processo que não está executando em sua região crítica não pode impedir outros processos 
de entrar em suas regiões críticas. Isso evita a possibilidade de bloqueios desnecessários e aumenta a 
eficiência do sistema.

4. **Nenhum processo deve esperar sem ter uma previsão para entrar em sua região crítica:** Isso significa 
que os processos não devem ficar esperando indefinidamente para entrar em suas regiões críticas. Em outras 
palavras, se um processo deseja entrar em sua região crítica e essa região está livre, ele deve ser capaz 
de entrar imediatamente, sem esperar indefinidamente.

## Exclusão mútua: com espera ociosa

Existem alguns métodos que impedem que um processo invada outro quando estão em suas regiões críticas.

### Desabilitando interrupções

Nessa solução, as interrupções são desabilitadas por cada processo assim que entra em sua região crítica 
e reativadas assim que sai delas. Dessa forma, a CPU não será disponibilizada para outro processo.

Essa solução se torna falha, pois ao dar autonomia para os processos, a multiprogramação pode ficar 
comprometida caso um processo esqueça de reativar as interrupções ao sair da região crítica.

Em sistemas de multiprocessadores, a interrupção ocorre em apenas um processador e os outros acessariam 
normalmente a memória compartilhada, comprometendo a solução.
