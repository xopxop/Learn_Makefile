one = export blah="I was set!"; echo $$blah

define two
export blah=set
echo $$blah
endef

#One and two are different.

all:
	@echo "This print 'I was set'"
	@$(one)
	@echo "This does not print 'I was set' because each command runs in a separate shell"
	@$(two)