# Comandos usados para o trabalho
---
### Comando para obter o PID e PPID
*pgrep + nome do processo*
>comando usado na atividade
>> _pgrep minecraft_

### Comando para obter a arvore
*pstree + o primeiro pid obitido*
>comando usado na atividade
>> _pstree 5007_

### Comando para obter o estado inicial
*ps -o stat,pri,ni,%cpu,%mem,cmd -p + 
>comando usado na atividade
>> _ps -o stat,pri,ni,%cpu,%mem,cmd -p 5009_
>> 
>> _ps -o stat,pri,ni,%cpu,%mem,cmd -p 5378_

### Comando para verificar as threads
*ps -L -p + PID*
>comando usado na atividade
