all: foo.o bar.o

# The automatic variable $@ matches the target, and $< matches the prerequisite
foo.o: foo.c
	echo "Call gcc to generate $@ from $<"

bar.o: bar.c
	echo "Call gcc to generate bar.o from bar.c"

# Matches all .c files and creates them if they don't exist
%.c:
	touch $@

clean:
	rm -f foo.c bar.c