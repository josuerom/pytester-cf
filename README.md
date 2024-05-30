# PyTester
Testeador, parseador y generador de plantillas para programas escritos en los lenguajes de programación C++, Java y Python. Esta herramienta está especialmente diseñada para abordar problemas directos de la plataforma [codeforces](https://codeforces.com/problemset) de manera ágil.

Para que estas automatizaciones funcionen correctamente, debe instalar los cuatro paquetes de terceros.
```bash
pip install requests beautifulsoup4 termcolor pyinstaller
```
> En Unix necesarimente debes crear antes un entorno virtual, para que ese comando funcione correctamente.

## LO QUE DEBE HACER
Modifique las líneas `29`, `55`, `59`, `168` y `156` según sus necesidades. Además, si es que no tiene una carpeta en donde almacena las plantillas, entonces deberá crearla.

Luego de haber modificado el programa y esté le funcione adecuadamente, entonces ⤵️

## CONVIERTA EL MODULO EN UN EJECUTABLE
### En Windows
Ejecuta la instrucción con el nombre del modulo de python3 correspondiente, en la misma ubicación que se encuentre el archivo, por ejemplo:
```python
pyinstaller --onefile wi_tester.py
```

Ahora, debes agregar la ruta en donde se encuentre el ejecutable `.\dist\wi_tester.exe` al PATH (Variables de entorno), por ejemplo: `%HOMEPATH%\pytester\dist`, para que cuando escribas el nombre del ejecutable (sin el .exe) desde cualquier parte de la terminal, el sistema lo pueda reconocer como un comando, y así mantener una mayor velocidad de invocación.

### En Linux & MacOS
Ejecuta todas estas instrucciones dentro de la carpeta que contiene el modulo de python3.

Crea un entorno virtual
```bash
python3 -m venv pytester
source pytester/bin/activate
```
Ahora realiza la conversión de modulo a ejecutable para Unix
```bash
pyinstaller --onefile un_tester.py
```
Desactiva el entorno virtual
```bash
deactivate
```
Luego de esos, debe aparecer algo como esto `./dist/un_tester`; debes mover el archivo ejecutable al directorio de binarios del sistema y concederle los permisos de ejecución. Por lo que debe ejecutar
```bash
sudo chmod +x dist/un_tester
sudo mv dist/un_tester /usr/bin/
```
Una vez haya hecho esto y haya salido bien, entonces puede invocar al ejecutable desde cualquier parte de la terminal con el nombre que le haya dejado al binario añadido a la ruta `/usr/bin/` como `un_tester`.

Si necesita renombrar, ejecute `sudo mv /usr/bin/un_tester /usr/bin/tester`.
