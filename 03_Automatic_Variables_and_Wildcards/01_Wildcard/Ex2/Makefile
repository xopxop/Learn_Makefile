wrong = *.o #wrong
objects := $(wildcard *.c) #right

some_binary:
	touch f1.c
	touch f2.c
	echo $(wrong)
	echo $(objects)

clean:
	rm -f *.c