all: {{cookiecutter.project_slug}}

clean:
	rm *.o *.lst *~

{{cookiecutter.project_slug}}: {{cookiecutter.project_slug}}.o
	ld -o {{cookiecutter.project_slug}} {{cookiecutter.project_slug}}.o

{{cookiecutter.project_slug}}.o:
	nasm -f elf64 -g -F dwarf {{cookiecutter.project_slug}}.asm -l {{cookiecutter.project_slug}}.lst
