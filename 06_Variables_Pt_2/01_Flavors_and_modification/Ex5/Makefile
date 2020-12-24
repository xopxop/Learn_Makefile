foo := a.o b.o c.o
# bar becomes a.c b.c c.c
bar := $(foo:.o=.c)

all:
	echo $(bar)