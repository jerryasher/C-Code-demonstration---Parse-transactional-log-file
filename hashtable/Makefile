CC=gcc
CFLAGS=-c -Wall
DEBUG=-ggdb
LDFLAGS=
SOURCES=report.c txnstats.c
OBJECTS=$(SOURCES:.c=.o)
EXECUTABLE=report

DEPS = txnstats.h

all: $(SOURCES) $(EXECUTABLE)
	
$(EXECUTABLE): $(OBJECTS) 
	$(CC) $(DEBUG) $(LDFLAGS) $(OBJECTS) -o $@

%.o: %.c $(DEPS)
	$(CC) -c $(DEBUG) -o $@ $< $(CFLAGS)

.PHONY: clean

clean:
	rm -rf *o *~ report
