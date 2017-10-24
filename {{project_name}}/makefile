all: {{project_name}}

clean:
	rm *.o *.lst *~

{{project_name}}: {{project_name}}.o
	ld -o {{project_name}} {{project_name}}.o

{{project_name}}.o:
	nasm -f elf64 -g -F dwarf {{project_name}}.asm -l {{project_name}}.lst
