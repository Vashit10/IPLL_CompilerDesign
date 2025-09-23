# Makefile for compiling the Yacc and Lex files for micro C

CC=gcc
CFLAGS=-Wall

all: parser

parser: lex.yy.c y.tab.c y.tab.h
	$(CC) $(CFLAGS) -o parser y.tab.c lex.yy.c -lfl

y.tab.c y.tab.h: a7_220101107.y
	yacc -d a7_220101107.y

lex.yy.c: a7_220101107.l
	lex a7_220101107.l

clean:
	rm -f parser lex.yy.c y.tab.c y.tab.h