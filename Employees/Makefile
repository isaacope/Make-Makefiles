#
# Author: Isaac Copeland
# File: Makefile
# Date: 09/15/22
# Compilation instructions for Employee Program
#

# the compiler
CC = g++
# compile with all warnings and errors
CFLAGS = -g -Wall -Wextra -c
# the executable to be created
TARGET = employee
# compile and link all .o files and create binary
FINAL = -g -Wall -Wextra -o $(TARGET)

default: all

all: $(TARGET)

# compilation instructions for the components of the target
$(TARGET): Employee.o Supervisor.o Officer.o main.o
	$(CC) $(FINAL) Employee.o Supervisor.o Officer.o main.o

# compilation instructions for the components of the object files 
Employee.o: Employee.cpp Employee.h
	$(CC) $(CFLAGS) Employee.cpp

Supervisor.o: Supervisor.cpp Supervisor.h
	$(CC) $(CFLAGS) Supervisor.cpp

Officer.o: Officer.cpp Officer.h
	$(CC) $(CFLAGS) Officer.cpp

main.o: main.cpp Employee.h
	$(CC) $(CFLAGS) main.cpp

# compilation instructions for make clean
clean:
	$(RM) $(TARGET) *.o *~
