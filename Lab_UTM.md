### UTM VM

* Pro M+ MacBooky není možné nahrát starší verzi Ubuntu kvůli architektuře ARM. Virtuální prostředí lze stále vytvořit prostřednictvím emulace v UTM
* Nainstalujte UTM z [https://mac.getutm.app](https://mac.getutm.app)
* Stáhněte si iso Ubuntu Focal Fosa 20.04 (desktop image varianta) [https://www.releases.ubuntu.com/20.04/](https://www.releases.ubuntu.com/20.04/)
* Při tvorbě VM vyberte možnost **emulace** – je v zásadě pomalejší, ale umožní spustit jiné architektury než ARM
* Novému VM přidělte alespoň 2 CPU, 8GB RAM a 20-30 GB VDI (doporučeno 4 CPU a 25 GB VDI)
* Zvolte variantu nainstalovat a minimalistickou instalaci (instalace i tak bude nějakou dobu trvat)
* Nainstalujte MySQL Server:
```
$ sudo apt update && sudo apt upgrade
$ sudo apt install mysql-server
```
* Zkontrolujte verzi MySQL Server:
```
$ mysql --version
```
* Pro verzi 8.0.32+ musíte najprve nastavit heslo uživatel root manuálně:
```
$ sudo mysql_secure_installation
$ sudo mysql
mysql> alter user 'root'@'localhost' identified with mysql_native_password by 'student';
mysql> quit;
$ sudo mysql_secure_installation
```
* Vytvořte uživatele student a přidělte mu oprávnění
```
$ sudo mysql -u root -p
mysql> create user 'student'@'%' identified by 'student';
mysql> grant all privileges on *.* to 'student'@'%'
```
* Vytvořte databázi 4iz562
* Naimportujte data, část po < upravte dle vaší cesty k souboru:
```
$ mysql -u student -p 4iz562 < 4iz562.sql
```
* Import databáze je v emulovaném prostředí pomalejší, v mezičase si tedy otevřete nový tab a spusťte následující příkazy
* Nainstalujte Python virtualenv a Jupyter Lab
```
$ sudo apt-get install python3-pip
$ sudo -H pip3 install --upgrade pip
$ sudo -H pip3 install virtualenv
$ mkdir Jupyter
$ cd Jupyter
$ virtualenv environment
$ source environment/bin/activate
$ pip install jupyter
$ pip install jupyterlab
$ pip install mysql-kernel
$ python -m mysql_kernel.install
```
* Přeinstalujte balíček sqlalchemy verzí 1.4.35 (s novější verzí nebude mysql-kernel fungovat)
```
$ pip install sqlalchemy==1.4.35
```
* Spusťte jupyter lab (otevře okno prohlížeče)
```
$ jupyter lab
```
* Otestujte připojení k MySQL:
```
mysql://student:student@localhost:3306
```
* Pokud se objeví následující hláška
```
cryptography' package is required for sha256_password or caching_sha2_password auth methods
```
... nainstalujte z jupyter notebooku cryptography python balíček:
```
!pip install cryptography
```
Pokud následující příkaz nezobrazí seznam databází na mysql serveru, je nejspíš něco špatně s kernelem nebo sqlalchemy balíčkem
```
show databases;
```
Pro diagnostiku problému zkuste nejprve zjistit verze balíčků jupyteru. Z notebooku spusťte následující příkaz:
```
!jupyter --version
```
Výstup by měl být:
```
Selected Jupyter core packages...
IPython          : 8.2.0
ipykernel        : 6.13.0
ipywidgets       : 7.7.0
jupyter_client   : 7.2.2
jupyter_core     : 4.10.0
jupyter_server   : 1.16.0
jupyterlab       : 3.3.4
nbclient         : 0.6.0
nbconvert        : 6.5.0
nbformat         : 5.3.0
notebook         : 6.4.11
qtconsole        : 5.3.0
traitlets        : 5.1.1
```
* Dále zkontrolujte verzi sqlalchemy:
```
!pip show sqlalchemy
```
* Pokud budete instalovat Talend Open Studio for Data Quality, stáhněte zip soubor ze Sourceforge.net a nainstalujte default JDK:
```
$ sudo apt install default-jdk
```
* Pokud se v průběhu práce na semestrální práci objeví následující hláška:
```
pandas.io.sql.execute requires a connection
```
Použijte tento fix:
```
!pip uninstall pandas -y
```
```
!pip install pandas==1.4.2
```
```
!pip show pandas
```
```
!pip show visions
```
### Bonus pro usnadnění práce s VM
* Práci si lze usnadnit povolením kopírování souborů z clipboardu v lokálním prostředí a nazpátek
* Zároveň lze nastavit sdílenou složku mezi VM a lokálním prostředí
* Zadejte následující příkaz:
 ```
sudo apt install spice-vdagent qemu-guest-agent spice-webdavd
``` 
* V nastavení v záložce Sharing povolte sdílení clipboardu a pokud tak není nastaveno, vyberte Directory Share Mode jako **SPICE WebDAV**
* Dále je potřeba vybrat cestu ke složce, kterou chci sdílet (např. Downloads)
* V prohlížeči VM otevřu následující adresu, kde nyní uvidím sdílený obsah složky: [http://127.0.0.1:9843/](http://127.0.0.1:9843/)
