# Detección del Sistema Operativo
ifeq ($(OS),Windows_NT)
    # Configuración para Windows
    RM = del /Q
    TARGET = programa.exe
    RUN_CMD = ./$(TARGET)
else
    # Configuración para Linux / Mac
    RM = rm -f
    TARGET = programa
    RUN_CMD = ./$(TARGET)
endif

CC = gcc
CFLAGS = -g -Wall -std=c23
FILE = hello.c

.PHONY: all run clean

all: $(TARGET) run

$(TARGET): $(FILE)
	$(CC) $(CFLAGS) $(FILE) -o $(TARGET)

run: $(TARGET)
	$(RUN_CMD)

clean:
	$(RM) $(TARGET)