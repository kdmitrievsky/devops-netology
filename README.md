# devops-netology

По умолчанию виртуальной машине выделено 2 процессора и 1024Мб оперативной памяти.

Добавить ресурсов виртуальной машине можно в блоке конфигурации vm.provider соответствующими параметрами: memory и cpus
    
    Например: 
    имя_узла.vm.provider "virtualbox" do |v|
        
    v.memory = 1024

    v.cpus = 2

    end

Длину журнала history можно задать переменной HISTSIZE (595 строчка мануала)

Директива ignoreboth позволяет не записывать в историю и дубликаты команд и команды начинающиеся с пробела

{} (фигурные скобки) используются для выполнения набора команд как единого целого в контексте текущего shell (строка 197 в man bash) или для вывода значения параметра в конструкции ${} 

Создать 100000 файлов одной командой можно так: touch file{1..100000}. 300000 файлов создать не удается по причине слишком большого числа аргументов (Argument list is too long)

Конструкция [[ -d /tmp ]] выдает true если в корне существует директория tmp

Для появления нужного пути в первой строке вывода type -a bash нужно переопределить переменную PATH следующим образом: export PATH="/tmp/new_path_directory:$PATH"

Разница м/у batch И at в следующем: at - разовое задание, выполняемое в определенную дату/время, batch (это alias at -b) - разовое задание, выполняемое когда загрузка системы ниже определенного уровня.

