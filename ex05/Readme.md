# Упражнение 5

## I. Променливи в BASH

**променлива=[стойност]** - присвояване на стойност на променлива
**$променлива | ${променлива}** - използване на стойността

- Типа на променливите е символен низ и за това не е задължително променливите да се декларират предварително
- Имената на променливите може да съдържат букви, цифри и _, като започват с буква или _

    currentDate=\`date\` - резултат от дадена команда
    
    echo $currentDate


#### Аритметични изрази (само за цели числа)
- `expr val {+, -, \\*, /} val [{+, -, \*, /} val][...]`
- `$[val + val]`

Примери:
* z = \`expr $x + 7\` - Важни са space-овете
    Пример: echo $z → 10
* z = \`$[x + 6]\` - Може и без space
    Пример: echo $z → 13
* 
    * br=0
    * br=\`expr $br + 1\`

### Системни променливи
- `HOME` - home директорията на потребителя 
- `PS1` - първичен prompt 
- `PATH` - Глобална променлива, която указва в кои директории да се търсят изпълними файлове
- `USER` - името на текущия потребителя
- `PWD` - текущата директория
- `?` - exit status на последния завършил процес  
- `!` - PID на последния стартиран процес във асинхронен режим

## II. Командни процедури

<span>script1.sh</span>

    #!/bin/bash
    
    echo "Hello world!"

Стартиране:

    chmod 777 script1.sh
    ./script1.sh