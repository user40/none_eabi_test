CC            = arm-none-eabi-gcc
AS			  = arm-none-eabi-as
# -Osはプログラムサイズを小さくする最適化
CFLAGS		  = -march=armv5te -mthumb -Os
# 非ARM系のマシンでリンクするために必要
LDFLAGS		  = --specs=nosys.specs
PROGRAM       = hello

all:
	$(CC) $(CFLAGS) $(LDFLAGS) $(PROGRAM).c -o $(PROGRAM)

bin: obj
	arm-none-eabi-objcopy -O binary $(PROGRAM).o

obj: asm
	$(AS) -c $(PROGRAM).s -o $(PROGRAM).o

asm:
	$(CC) -S $(CFLAGS) $(PROGRAM).c

clean:
	rm -f *.o *.s *~ $(PROGRAM)