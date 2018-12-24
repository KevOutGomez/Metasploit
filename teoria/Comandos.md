# Comandos en Metasploit
A continuación se enlistan algunos de los comandos mas utilizados dentro de Metasploit:

* Comando para inicializar Metasploit:
	```bash
	msfconsole
	```
	Este comando puede ir acompañado de algunas banderas como lo es:
	* **-h**: Help
	* **-v**: Mostrar la versión de Metasploit
	* **-q**: Modo tranquilo, sin mostrar imagen de inicio.

* Para actualizar Metasploit (Solo Metasploit):
	```bash
	msfupdate
	```

Dentro de Metasploit:

* Para mostrar todos los comandos disponibles de Metasploit:
	```bash
	help
	```

	o tambien podemos utilizar:

	```bash
	?
	```
* Lista más opciones (opciones avanzadas) para cada uno de los modulos de Metasploit:
	```bash
	advance
	```

* Elegir otro modulo:
	```bash
	back
	```

* Para listar todos los exploits de Metasploit utilizamos:
	```bash
	show exploits
	```

* Para listar los auxiliares:
	```bash
	show auxiliary
	```

* Para listar los nops:
	```bash
	show nops
	```

* Para ver a detalle la información de un modulo:
	```bash
	info [nombre del modulo]
	```

	Ejemplo:

	```bash
	info windows/wins/ms04_045_wins
	```

* Para realizar una busqueda especifica de algun modulo utilizamos:
	```bash
	search [palabra_clave]
	```

	Ejemplo:

	```bash
	search adobe
	```

	Para hacer mas especifica la búsqueda podemos utilizar opciones especificas como:

	* **path:** Permite filtrar los modulos que tengan en su path coincidencias con la palabra clave.

		```bash
		search path:wins
		```

		Salida:

		```bash
		Matching Modules
		================

   		Name                                                    Disclosure Date  Rank       Check  Description
   		----                                                    ---------------  ----       -----  -----------
   		auxiliary/admin/http/typo3_winstaller_default_enc_keys                   normal     No     TYPO3 Winstaller Default Encryption Keys
   		exploit/windows/local/bypassuac_injection_winsxs        2017-04-06       excellent  No     Windows Escalate UAC Protection Bypass (In Memory Injection) abusing WinSXS
   		exploit/windows/wins/ms04_045_wins                      2004-12-14       great      Yes    MS04-045 Microsoft WINS Service Memory Overwrite
   		post/windows/gather/credentials/winscp                                   normal     No     Windows GatherWinSCP Saved Password Extraction
		```

	* **platform:** Permite filtrar los modulos especificando la plataforma a la que estan dirigidos.

		```bash
		search platform:osx
		```

		Salida:

		```bash
		Matching Modules
		================

		Name                                                                  Disclosure Date  Rank       Check  Description
		----                                                                  ---------------  ----       -----  -----------
		auxiliary/gather/safari_file_url_navigation                           2014-01-16       normal     No     Mac OS X Safari file:// Redirection Sandbox Escape
		exploit/apple_ios/browser/safari_libtiff                              2006-08-01       good       No     Apple iOS MobileSafari LibTIFF Buffer Overflow
   		exploit/apple_ios/email/mobilemail_libtiff                            2006-08-01       good       No     Apple iOS MobileMail LibTIFF Buffer Overflow
   		exploit/multi/browser/firefox_escape_retval                           2009-07-13       normal     No     Firefox 3.5 escape() Return Value Memory Corruption
   		exploit/multi/browser/firefox_proto_crmfrequest                       2013-08-06       excellent  No     Firefox 5.0 - 15.0.1 __exposedProps__ XCS Code Execution
		....
		```

	* **type:** Permite especificar el tipo de modulo

		```bash
		search type:post
		```

		Salida

		```bash
		Matching Modules
		================

		Name                                                    Disclosure Date  Rank       Check  Description
		----                                                    ---------------  ----       -----  -----------
   		post/aix/hashdump                                                        normal     No     AIX Gather Dump Password Hashes
   		post/android/capture/screen                                              normal     No     Android Screen Capture
   		post/android/gather/sub_info                                             normal     No     extracts subscriber info from target device
		```
	
	* **cve:** Para una búsqueda a partir de la fecha en la que fue descubierta la vulnerabilidad, es importante señalar que el acrónimo **cve** corresponde a Vulnerabilidades y Exposiciones Comunes

		```bash
		search cve:2017
		```
	**NOTA**: Es importante señalar que las opciones anteriores pueden ser combinadas para realizar una búsqueda más específica del algun módulo.

