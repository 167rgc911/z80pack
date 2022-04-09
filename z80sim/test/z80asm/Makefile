AS = z80asm # with z80pack
AS = z80asm_d # http://deb.debian.org/debian/pool/main/z/z80asm/z80asm_1.8.orig.tar.gz
DAS = z80dasm_d #http://deb.debian.org/debian/pool/main/z/z80dasm/z80dasm_1.1.6.orig.tar.gz

ASFLAGS =

all: float.hex z80main.hex

float.hex: float.asm
	$(AS) $(ASFLAGS) float.asm -o float.bin
	bin2hex float.bin float.hex

z80main.hex: z80main.asm z80dis.asm z80ops.asm
	$(AS) $(ASFLAGS) z80main.asm -o z80ops.bin
	bin2hex z80main.bin z80main.hex

clean:
	rm -f *.bin *.hex *.lis
