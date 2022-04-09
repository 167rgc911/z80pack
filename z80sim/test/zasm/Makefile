AS = z80asm # with z80pack
AS = z80asm_d # http://deb.debian.org/debian/pool/main/z/z80asm/z80asm_1.8.orig.tar.gz
AS = zasm # https://k1.spdns.de/Develop/Projects/zasm/Distributions/
DAS = z80dasm_d #http://deb.debian.org/debian/pool/main/z/z80dasm/z80dasm_1.1.6.orig.tar.gz

ASFLAGS =

all: float.hex z80main.hex

float.hex: float.asm
	$(AS) $(ASFLAGS) --hex float.asm -l float.lis -o float.hex
	#$(AS) $(ASFLAGS) float.asm -l float.lis -o float.bin
	#bin2hex float.bin float.hex

z80main.hex: z80main.asm z80dis.asm z80ops.asm
	$(AS) $(ASFLAGS) z80main.asm

clean:
	rm -f *.hex *.lis
