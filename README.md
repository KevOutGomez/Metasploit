# Metasploit
![Metasploit](https://dcq42kgjc5wgh.cloudfront.net/cdn/13/images/curso-online-metasploit-framework_l_primaria_1.jpg)

Metasploit es un proyecto de código abierto para la seguridad informática, que proporciona información acerca de vulnerabilidades de seguridad y ayuda en tests de penetración "Pentesting" y el desarrollo de firmas para sistemas de detección de intrusos.

Su subproyecto más conocido es el Metasploit Framework, una herramienta para desarrollar y ejecutar exploits contra una máquina remota. Otros subproyectos importantes son las bases de datos de opcodes (códigos de operación), un archivo de shellcodes, e investigación sobre seguridad. Inicialmente fue creado utilizando el lenguaje de programación de scripting Perl aunque actualmente el Metasploit Framework ha sido escrito de nuevo completamente en el lenguaje Ruby.

## Instalación
Para instalar **Metasploit** es necesario ejecutar los siguientes comandos:

```bash
sudo yum -y install ruby-irb rubygems rubygem-bigdecimal rubygem-rake rubygem-i18n ruby-devel libpcap-devel postgresql-server postgresql-devel
```

```bash
curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall && \
  chmod 755 msfinstall && \
  ./msfinstall
```


