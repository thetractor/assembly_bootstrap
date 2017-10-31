all: lib.o {{cookiecutter.project_slug}}

clean:
	rm *.o *.lst *~

{{cookiecutter.project_slug}}: {{cookiecutter.project_slug}}.o
	mv ../../lib/lib.o .
	ld -o {{cookiecutter.project_slug}} {{cookiecutter.project_slug}}.o lib.o

{{cookiecutter.project_slug}}.o:
	nasm -f elf64 -g -F dwarf {{cookiecutter.project_slug}}.asm -l {{cookiecutter.project_slug}}.lst

lib.o: /home/lars/dev/bfh/gdi/lib/lib.asm
	nasm -f elf64 -g -F dwarf ../../lib/lib.asm -l lib.lst
