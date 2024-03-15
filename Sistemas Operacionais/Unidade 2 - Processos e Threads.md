# Introdução

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
