# Introdução

Nesta seção, serão apresentados os conceitos, características, hierarquia e os estados dos processos e 
threads, bem como a criação e o término de processos.

Os processos são tarefas ou programas em execução, e o Sistema Operacional é responsável por 
administrá-los por meio do gerenciador de processos.

Existem os processos iniciados pelo usuário e também os processos iniciados por outros processos.

## Processos: Conceito e Criação 

Nos computadores, os processos funcionam como uma linha de produção, executando vários programas ao mesmo
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

