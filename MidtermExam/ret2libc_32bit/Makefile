all:
	echo 0 | sudo tee /proc/sys/kernel/randomize_va_space
	gcc -m64 -fno-stack-protector -z execstack -o stack stack.c
	sudo chown root stack
	sudo chgrp root stack
	sudo chmod +s stack
clean:
	rm -f stack
