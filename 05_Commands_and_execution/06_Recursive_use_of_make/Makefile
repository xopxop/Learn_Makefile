new_contents = "hello:\n\ttouch inside_file"
all:
	mkdir -p subdir
	echo $(new_contents) | sed -e 's/^ //' > subdir/makefile
	cd subdir && $(MAKE)

clean:
	rm -rf subdir