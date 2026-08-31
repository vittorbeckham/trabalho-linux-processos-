  # DIAGNÓSTICO DE PROCESSOS EM LINUX

![Linux](https://img.shields.io/badge/Faculdade%20Serra%20Dourada-red)
![Sistemas Operacionais](https://img.shields.io/badge/Sistemas%20Operacional%20Linux-green)
![Trabalho 1](https://img.shields.io/badge/Trabalho%201-blue)
> Curso: Analise e Desenvolvimento de Sistemas

>Trabalho academico - Processos em  Linux

---

  ### Alunos

- **Jose Vitor Santos da Silva**
- **Eduardo Gonçalves Oliveira**

---
  ## Descrição


>**Aplicação Escolhida: Minecraft Java Edition**
>>    *O minecraft e um jogo mundialmente conhecido entre a comunidade gamer e foi desenvolvido em java. Durante sua execução, a aplicação utiliza diversos recursos do sistema operacional, como processador (CPU), memória RAM, armazenamento e processos relacionados à execução do jogo e da máquina virtual Java.*
>
>**Justificativa da escolha**
>> *Escolhi o Minecraft porque ele foi uma das minhas primeiras experiências com o Linux. Meu primeiro computador utilizava esse sistema, e uma das primeiras coisas que eu queria fazer nele era instalar e jogar Minecraft. Além de ter uma relação pessoal com a escolha, acredito que o jogo também é uma boa aplicação para realizar este trabalho, pois durante sua execução utiliza recursos do computador, como processador e memória, permitindo acompanhar e analisar seus processos por meio das ferramentas do Linux.*

---
  ## Ambiente Utilizado

- **Distribuição Linux:** Ubuntu 
- **Versão:** 25.04 (Plucky Puffin) (64-bit)
- **Ambiente:** Máquina Virtual (VirtualBox)

---

  ## Como Executar a Aplicação Analisada

> ### Para realizar o experimento, foi utilizada uma máquina virtual configurada no VirtualBox com o sistema operacional Linux (ubunto).
>
> **O procedimento de execução foi realizado na seguinte ordem:**
>
>> 1. Iniciar o VirtualBox.
>> 2. Iniciar a máquina virtual com o Linux.
>> 3. Abrir o Minecraft Launcher.
>> 4. Aguardar o carregamento do launcher.
>> 5. Iniciar o Minecraft.
>> 6. Com o jogo em execução, realizar a análise dos processos e
   recursos utilizados pelo sistema.

  ## Comandos Ultilizados
> Aqui vamos ver os comandos que foram ultilizados nessa atividade/trabalho de forma organzidade de acordo com o que foi pedido no trabalho e oque cada um desse comados faz.

   ---
  ## Evidências 

![Minecraft em execução](evidencias/01-minecraft.png)

   ---

  ## Interpretação Técnica dos Resultados

>Durante a execução do Minecraft, foi possível observar o
comportamento do processo por meio das ferramentas de monitoramento
disponíveis no Linux.
>
>O processo apresentou consumo de aproximadamente **72% de CPU**,
indicando uma utilização significativa do processador durante a
execução do jogo.
>>
>Em relação à memória, o processo utilizou aproximadamente **3,8 GB
de RAM**, demonstrando que a aplicação demanda uma quantidade
considerável de memória para manter seus recursos e dados carregados.
>
>O Linux também atribuiu ao processo o **PID 4521**, utilizado para
identificar e acompanhar especificamente a execução do Minecraft.
>
>Com base nesses resultados, foi possível observar como uma aplicação
real utiliza os recursos disponibilizados pelo sistema operacional.

---

## Conclusão do diagnóstico

>Durante o experimento, foi possível acompanhar o comportamento do processo desde sua execução até seu encerramento. Inicialmente, o processo encontrava-se em estado de espera e apresentava consumo de CPU e memória compatível com a aplicação executada.
>
>A análise do PID e PPID permitiu identificar o processo analisado e sua relação com o processo pai, demonstrando a hierarquia de processos do sistema Linux. A análise do estado também mostrou que o processo sofreu alterações conforme os sinais enviados. Com o SIGSTOP, sua execução foi interrompida temporariamente, enquanto o SIGCONT permitiu sua retomada. Por fim, o SIGTERM provocou o encerramento controlado do processo.
>
>A alteração do valor de nice permitiu observar a relação entre prioridade e escalonamento, mostrando como o sistema operacional pode influenciar a preferência de execução de um processo. A análise das threads e das informações disponíveis em /proc complementou o diagnóstico, fornecendo dados internos sobre o processo.
>
>Assim, as evidências coletadas demonstram, na prática, como o Linux controla processos, estados, prioridades, recursos, threads e sinais. O comportamento observado esteve de acordo com o funcionamento esperado do sistema operacional durante o experimento.
