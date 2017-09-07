GCC = @g++
LEX = @flex
YACC = @bison

demo: demo.cpp yacc.o
			$(GCC) demo.cpp yacc.o -o demo

yacc.o: yacc.c
			$(GCC) -c yacc.c

yacc.c: demo.y lex.c
			$(YACC) -o yacc.c -d demo.y

lex.c: demo.lex
			$(LEX) -o lex.c demo.lex

clean:
				@-rm -f *.o *~ lex.c yacc.c yacc.h demo
.PHONY: clean
