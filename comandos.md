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
>> _ps -L -p 5009_
>> 
>> _ps -L -P 5378_

### Comando para Explorar o diretório
*cat /proc/+PID/status*
>comando usando na atividade
>>cat  /proc/5009/status
>>
>>cat  /proc/5378/status

### Comando usados para aplica sinais 
*kill -STOP + PID*

*kill -CONT + PID*

*renice + valor + PID*

*kill -TERM + PID*
>comando usado na atividade
>>kill -STOP 5009
>>
>>kill -STOP 5378
>>
>>kill -CONT 5009
>>
>>kill -CONT 5378
>>
>>renice 1 -p 5009
>>
>>renice 1 -p 5378
>>
>>kill -TERM 5009
>>
>>kill -TERM 5378

### Outros comando usando ( para verificar o nice e %cpu + %mem)
*top -p + PID*
>comando usado na atividade
>>top -p 5009
>>
>>top -p 5009
