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

[Baixar Documento PDF](./Evidencias.pdf)

   ---

## Interpretação Técnica dos Resultados

>Durante a execução do Minecraft, foi possível observar o comportamento dos processos por meio dos comandos de monitoramento disponíveis no Linux.
>
>Nos resultados obtidos, o processo **5009**, relacionado ao launcher, apresentou aproximadamente **2,6% de uso de CPU** e **4,7% de memória**. Já o processo **5378**, responsável pela execução do jogo, apresentou >um consumo maior, com aproximadamente **46,5% de CPU** e **31,4% de memória**.
>
>Essa diferença mostra que o processo responsável pelo jogo utiliza mais recursos do sistema do que o launcher, principalmente por estar executando o jogo e suas funções.
>
>Também utilizamos os **PID e PPID** para identificar e acompanhar os processos e entender a relação entre o processo pai e o processo filho. Com essas informações, foi possível observar na prática como o Linux >organiza e gerencia os processos durante a execução de uma aplicação.
>
>Com base nos resultados, conseguimos perceber como uma aplicação real utiliza os recursos do sistema operacional e como ferramentas do Linux podem ser utilizadas para acompanhar e analisar esse comportamento.


---

## Conclusão do diagnóstico

>Durante o experimento, foi possível acompanhar os processos do Minecraft desde sua identificação até o encerramento. Primeiro, utilizamos os comandos `pgrep` e `pstree` para encontrar os PIDs e entender a relação >entre o processo pai e o processo filho. Com isso, conseguimos identificar o processo **5009**, relacionado ao launcher, e o processo **5378**, responsável pela execução do jogo.
>
>Também analisamos o estado, a prioridade, o valor de nice, o uso de CPU e memória dos processos. Foi possível perceber uma diferença no consumo de recursos entre eles: enquanto o processo 5009 utilizava cerca de >**2,6% de CPU e 4,7% de memória**, o processo 5378 apresentava um consumo maior, com aproximadamente **46,5% de CPU e 31,4% de memória**.
>
>Durante os testes com os sinais, observamos na prática o efeito do **SIGSTOP**, que interrompeu os processos e fez com que a interface, os sons e as animações do jogo ficassem parados. Também foi possível observar >a mudança do estado dos processos de **S para T**. Depois, utilizando o **SIGCONT**, os processos voltaram a funcionar normalmente.
>
>Também realizamos a alteração da prioridade utilizando o comando `renice` e verificamos novamente os processos com o `top`. Essa etapa permitiu observar como podemos alterar e acompanhar a prioridade de um >processo durante sua execução.
>
>Por fim, fizemos o teste encerrando o processo pai com o **SIGTERM**. Nesse caso, o processo **5009** foi encerrado, mas o processo **5378**, responsável pelo jogo, continuou funcionando normalmente. Com isso, >conseguimos observar na prática um processo filho ficando órfão após o encerramento do seu processo pai. Depois, encerramos também o processo 5378, finalizando o diagnóstico.
>
>Dessa forma, o experimento permitiu relacionar os conceitos estudados com situações reais de gerenciamento de processos no Linux. Conseguimos observar a hierarquia entre processos, o uso de recursos, as threads, >os estados, as prioridades e o funcionamento dos sinais de controle, entendendo melhor como o sistema operacional acompanha e gerencia os processos durante sua execução.

