# Introdução

Nesta seção, serão apresentados os conceitos, características, hierarquia e os estados dos processos e 
threads, bem como a criação e o término de processos.

Os processos são tarefas ou programas em execução, e o Sistema Operacional é responsável por 
administrá-los por meio do gerenciador de processos.

Existem os processos iniciados pelo usuário e também os processos iniciados por outros processos.

## Processos: Conceito e Criação 

Nos computadores, os processos funcionam como uma linha de produção, executando vários programas ao mesmo tempo de forma sequencial. A CPU é responsável por alternar os programas, executando-os por frações de segundo, para que cada um tenha acesso ao processamento, dando a ilusão ao usuário de paralelismo.

O paralelismo, ou pseudoparalelismo, é a falsa impressão de que os programas estão sendo executados ao mesmo tempo, mas o que realmente acontece é que o processo de um programa é suspenso temporariamente para dar lugar ao processamento de outro.

Um modelo foi desenvolvido para lidar com o paralelismo de forma mais fácil, organizando os programas executáveis em processos sequenciais. Um processo pode ser entendido como um programa em execução, incluindo não apenas o código em si, mas também informações importantes como o valor do contador de programa atual, registradores e variáveis.

A alternância entre processos, que ocorre constantemente na CPU, é conhecida como multiprogramação. Isso significa que, em um ambiente multiprogramado, a CPU não está dedicada a executar apenas um único processo de cada vez. Em vez disso, ela alternadamente executa diversos processos em rápida sucessão, o que dá a impressão de que múltiplos programas estão sendo executados simultaneamente.
