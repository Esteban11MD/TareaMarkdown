# Comandos de Consola 
### Introduccion 
los comandos de consola nos ayudan a realizar diversas tareas a travez de una terminal, lo que hariamos son acciones que se realizarian a nivel grafico pero que se realizan a nivel de consola.

### Comandos en consolas windows y linux
|COMANDOS ARCHIVOS	|MSDOS	|LINUX|
|-------------------|-------|-----|
|**Ver contenido**	|`type archivo.txt`|cat archivo.txt|
|**Archivo vacío**	|copy nul archivo.txt	|touch archivo.txt|
|**Archivo con texto**	|echo hola como estas > archivo.txt    O    copy con archivo.txt	|cat > archivo.txt |
|**Borrar archivo**	|del archivo.txt	|rm archivo.txt|
|**Renombrar archivo**	|ren archivo.txt archivo2.txt	|mv archivo.txt archivo2.txt|
|**Mover archivo**|	move carpeta2\archive2.txt carpeta1	|mv archivo.txt carpeta2|
|**Copiar archivo**|	copy archivo.txt carpeta1	|cp archivo.txt carpeta2|
|**Crear carpeta**|	mkdir carpeta1	|mkdir carpeta1
|**Borrar carpeta**|	rmdir carpeta1   O   rd /s carpeta1	|rmdir carpeta1    O   rm -r carpeta1|
|**Renombrar carpeta**|	ren carpeta1 carpeta2	|mv carpeta1 nuevacarpeta|
|**Mover carpeta**	|move carpeta1 carpeta2	|mv carpeta1 carpeta2|
|**Copiar carpeta vacía**|	Xcopy carpeta1 carpeta2 /T /E	|   |
|**Copiar carpeta y su contenido**|	Copy carpeta1 carpeta2	|cp -r carpeta1 carpeta2|
|**Ver contenido en carpeta**|	dir o tree /f 	|ls   O   ls -R   O   ls -al|
|**Ver contenido filtrado**|	find “texto” D:usuario……\carpeta	|Find . -name archivo.txt|
|**¿Dónde estoy?**	|cd	|pwd|
|**Desplazarse arriba y abajo**| cd carpeta1 Y cd .. | cd carpeta1 Y cd .. |

