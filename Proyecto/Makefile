a.out: main.o lex.yy.o Bison.tab.o
		gcc main.o lex.yy.o Bison.tab.o -ll

main.o: main.c Bison.tab.c
		gcc -c main.c

lex.yy.o: lex.yy.c
		gcc -c lex.yy.c

Bison.tab.o: Bison.tab.c
		gcc -c Bison.tab.c 

lex.yy.c: Flex.l Bison.tab.c
		flex Flex.l

Bison.tab.c: Bison.y
		bison -d Bison.y

clean:
		rm -f a.out main.o lex.yy.o Bison.tab.o lex.yy.c Bison.tab.c Bison.tab.h

run: a.out
		./a.out
