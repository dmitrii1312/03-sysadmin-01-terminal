# 03-sysadmin-01-terminal
## 5. Ресурсы, выделенные по-умолчанию 
1 CPU
1 Gb
## 6. Добавить оперативной памяти или ресурсов процессора виртуальной машине
	Vagrant.configure("2") do |config|
		config.vm.box = "bento/ubuntu-20.04"
		config.vm.provider "virtualbox" do |v|
			v.memory = 1024
			v.cpus = 2
		end
	end
### 8.1 Задать длину журнала history
HISTSIZE с.862
### 8.2 Директива ignoreboth в bash
Параметр выставляется в HISTCONTROL и указывает что должны игнорироваться пробелы в начале команды и не должны сохраняться дубликаты (команды, которые запускаются несколько раз подряд)
## 9. Сценарии использования скобки {}
с.257 используется как список
## 10. Создать однократным вызовом touch 100000 файлов
	touch file{1..100000}. 
	
	300000 файлов не создать, слишком длинный список аргументов получается:
	-bash: /usr/bin/touch: Argument list too long
## 11. Конструкция [[ -d /tmp ]]
Проверяет, что файл /tmp - существует и это директория
## 12. Вывод type -a bash
	mkdir /tmp/new_path_directory
	export PATH="/tmp/new_path_directory:/usr/local/sbin:/usr/local/bin:/bin:/usr/sbin:/sbin:/usr/games:/usr/local/games:/snap/bin"
	cp /bin/bash /tmp/new_path_directory
	cp /bin/bash /usr/local/bin
## 13. Планирование команд с помощью batch и at
batch - Запускает задачу когда система не нагружена, at - запускает задачу в определенное время

