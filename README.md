# 4IZ562 Řízení kvality dat
(Aktualizováno pro LS 2025/26)


* Přednášky: pátek 7:30 - 9:00 CET, cvičení: pátek 18:00 - 19:30 CET
* Konzultační hodiny individuálně na základě dohody s vyučujícím


## Struktura kurzu

### Úvod do řízení dat

1. **2025-02-20**: Úvod, organizační pokyny, motivace k řešení problematiky datové kvality. Požadavky na úspěšné absolvování kurzu. Co je to kvalita dat a informací. Řízení kvality dat a informací, Data Quality 1-2-3. Konfigurace labu, představení umělých dat, výstupů, MySQL toolbox.
2. **2025-02-27**: Vlastnosti dat. Příčiny a důsledky nekvalitních dat, Six Sigma, Kaizen, rekonciliace dat, root-cause analýza. Případové studie, měření vlastností dat, měření nákladů nekvalitních dat.
3. **2022-03-06**: Data Governance, související právní normy, Entity Recognition, kvalita metadat, datové katalogy, Data Lineage a Data Provenance. Právní normy relevantní pro naši praktickou úlohu, návrh principů, standardů, politik v praxi. Entity Recognition v praxi, anonymizace, masking, pseudonymizace dat.

### Analýza současného stavu

4. **2025-03-13**: Data Profiling a alternativní přístupy (analýza procesů, testování kontrol), Data Drift. Výstupy profilingu, příklady implementace v různých nástrojích, process mining.
5. **2025-03-20**: Validace dat, definice pravidel, datové kontroly, DQ Firewall, validační služby, vazba na metriky výkonnosti řízení dat. Validace v praxi, validace proti vybraným API.
6. **2025-03-27**: Audit kvality dat. Vypracování zprávy auditora. Parsing, standardizace, unifikace. Standardizace a unifikace v praxi. Prevence vzniku chyb, oprava stávajících chyb: standardizace, korekce, implementace kontrol. Proces řízení kvality dat (metodiky, modely, projekt implementace).

### Implementace nápravných opatření
7. **2025-04-03**: *Good Friday (výuka odpadá)* 
8. **2025-04-10**: *Inovační týden (výuka odpadá)* **Termín odevzdání zprávy auditora**
9. **2025-04-17**: Imputace chybějících pozorování, obohacování dat o externí datové zdroje, geocoding.
10. **2025-04-24**: Porovnávání a slučování záznamů, Master Data Management, Householding.
11. **2025-05-01**: *Státní svátek (výuka odpadá)*
12. **2025-05-08**: *Státní svátek (výuka odpadá)* 

### Monitorování datové kvality

13. **2025-05-15**: Implementace monitoringu, kontinuální zvyšování kvality dat, Augmented Data Quality, specifické formy datové kvality (nestrukturovaná data, Linked Data, ...). Rozdíl mezi Data Qualitz Monitoring a Data Observability. Extrakce metadat z nestrukturovaných dat, deduplikace nestrukturovaných dat. Aktuální trendy a výzvy. Příprava na test. 

### Zkouškové období

* 18.5. - 26.6. **zkouškový test**, **odevzdání nápravných opatření** (alespoň týden před koncem)

## Požadavky na úspěšné absolvování kurzu

### Zkouškový test

* 10 otázek z teorie po 4 bodech, celkem 40% celkového hodnocení

### Praktická úloha

* 60% celkového hodnocení

#### Audit kvality dat
* Identifikujte relevantní právní normy a regulace
* Identifikujte klíčové datové elementy
* Technický profiling: s pomocí vybraného nástroje vytvořte profilaci dat (základní popisné statistiky, četnosti syntaktických vzorů, ...)
* Validace vybraných atributů pomocí regulárních výrazů, kontrolních součtů, lookup a business pravidel
* Spočtěte úroveň kvantitativních vlastností dat (správnost, úplnost, konzistentnost, ...)
* Identifikujte nesoulad s požadavky právních norem a regulací
* Identifikujte nedostatky ve stávajícím datovém modelu (chybějící atributy, zbytečné atributy, chybné datové typy, nekonzistentní názvy, nekonzistentní collations)
* Root-cause analýza zjištěných defektů
* Na příkladu modelové firmy odhadněte roční výši nákladů na nekvalitní data (v kontextu užití dat)
* Porovnejte možné přínosy nápravných opatření se souvisejícími náklady
* Proveďte prioritizaci nápravných opatření
* Navrhněte externí datové zroje pro obohacení dat
* Navrhněte strategii pro doplnění chybějících hodnot
* Odevzdání vypracované zprávy auditora + naměřené charakteristiky / náklady (Word / HTML / PDF / Jupyter Notebook dle šablony pro zprávu auditora)

#### Implementace doporučených opatření
* Optimalizace datového modelu
* Parsing adresy, standardizace, vytvoření porovnávacích kódů a zřetězení na adresní registr
* Nastavení příznaku doručitelnosti na adresu na základě pravidel
* Doplnění chybějících pozorování
* Unifikace dat klientů, adres, kontaktů
* Deduplikace klientů
* Identifikace domácnosti
* Návrh kontrol bránících dalšímu vzniku chyb v datech
* Odevzdání CSV souboru s vyčištěnými daty (viz instrukce ze cvičení) + PDF dokumentace provedených opatření

### Celková klasifikace

#### Celková známka

* 90 a více bodů = 1
* 75 - 89 bodů = 2
* 60 - 74 bodů = 3
* 50 - 59 bodů = 4+ (možnost dozkoušení)
* 0 - 49 bodů = nevyhověl

#### Jak lzé získat body

* 60% bodů lze získat z praktické úlohy
* 40% bodů lze získat z testu
* bonusové body z quizů na přednáškách
* bonusové body za inovativní přístup (což není napsání promptu pro Claude apod., ale skill pro AI agenta už to být může)

## Zdroje ke studiu

### Povinná literatura

* Prezentace k přednáškám
* Články výslovně zmíněné přednášejícím

### Doporučená literatura

* McGILVRAY, D. Executing Data Quality Projects: Ten Steps to Quality Data and Trusted Information. Morgan Kaufmann, 2008. xviii, 325 s. ISBN 978-0-12-374369-5.
* MAYDANCHIK, Arkady. Data quality assessment. Bradley Beach: Technics Publications, LLC, [2007], ©2007. xiv, 321 stran. Data quality for practitioners series. ISBN 978-0-9771400-2-2.
* CHAPMAN, P., KHABAZA, T., SHEARER, C.: CRISP-DM 1.0 Step by step data mining guide. IBM, 2012. ftp://ftp.software.ibm.com/software/analytics/spss/support/Modeler/Documentation/14/UserManual/CRISP-DM.pdf
* Materiály dostupné na www.dataquality.cz
* PEJČOCH, D. Metody řešení problematiky neúplných dat [online]. 2011-01-13 Přednáška č. 4 v rámci Data Quality Tutorial. Dostupné pod odkazem: https://github.com/dpejcoch/4IZ562/tree/master/papers/Data_Imputation.pdf.
* PEJČOCH, D. Benchmark přístupů k Fuzzy Match / Merge. Sborník prací účastníků vědeckého semináře doktorského studia. Fakulta informatiky a statistiky VŠE. Praha 2009. ISBN 978-80-245-1524-3.
* LOSHIN, D. The Practitioner’s Guide to Data Quality Improvement. Burlington: Morgan Kaufmann as inprint of Elsevier, 2011. ISBN 978-0-12-373717-5.
* ENGLISH,  Larry P. Improving Data Warehouse and Business Information Quality: Methods for Reducing Costs and Increasing Profits. Wiley & Sons, 1999. xxvi, 518 s. ISBN-10 0-471-25383-9.
* LEE, Yang W., PIPINO, Leo L., FUNK, James D., WANG, Richard Y. Journey to Data Quality. The MIT Press, 2006. 240 s. ISBN-10 02-621-2287-1.
* BATINI, Carlo, SCANNAPIECO, Monica. Data Quality: Concepts, Methodologies and Techniques. Berlin: Springer-Verlag, 2006. xix, 262 s. ISBN-10 3-540-33172-7.
* BERSON, Alex, DUBOV, Larry. Master Data Management and Customer Data Integration for a Global Enterprise. McGraw-Hill Companies, 2007. xxi, 393 s. ISBN-10 0-07-226349-0.
* DYCHÉ,  Jill, LEVY, Evan. Customer data integration: Reaching a Single Version of the Truth. SAS Institute Inc., Wiley & Sons, 2006, xxiv, 294 s. ISBN-10 0-471-91697-8.
* REDMAN, T. Data Quality: The Field Guide. Boston: Butterworth-Heinemann MA, 2001. xviii, 241. ISBN-10 1-55558-251-6.
* DAMA International: The DAMA Guide to the Data Management Body of Knowledge (DAMA-DMBOK). Technics Publication, LLC, 2009. ISBN 978-1-9355040-2-3.
* Chaudhuri S., Ganjam K., Ganti V., Motwani R.: Robust and Efficient Fuzzy Match for Online Data Cleaning, SIGMOD 2003, June 9-12, 2003 San Diego, CA.
* D'Ambrosio A. Boosted Incremental Tree-based Imputation of Missing Data, PhD. thesis, Universitá degli Studi di Napoli Federico II. 2007.
* PEJČOCH, D. Audit datové kvality podle IT Assurance Guide: Using COBIT - 1. díl. In: Data Quality CZ [online]. 2012-03-07 07:14:52. Dostupné z: [URL].
* PEJČOCH, D. Audit datové kvality podle IT Assurance Guide: Using COBIT - 2. díl. In: Data Quality CZ [online]. 2012-03-07 07:14:52. Dostupné z: [URL].
* PEJČOCH, D. Audit datové kvality podle IT Assurance Guide: Using COBIT - 3. díl. In: Data Quality CZ [online]. 2012-03-07 07:14:52. Dostupné z: [URL].

### Odborné portály

* Dataversity: https://www.dataversity.net/
* DAMA: https://www.dama.org/cpages/home

### Osobnosti z oblasti řízení kvality dat a informací

* **Larry English** - guru informační kvality
* **Jil Dyché** - první dáma Data Governance
* **Evan Levy** - spoluzakladatel Baseline Consulting, autor řady publikací
* **David Loshin** - autor řady publikací pojednávajících o dopadu nekvalitních dat do byznysu
* **prof. Richard Wang** - vůdčí postava MIT Total Data Quality Management program
* **prof. Carlo Batini** - Università degli Studi di Milano-Bicocca
* **Thomas C. Redman, Ph.D.** - prezident Navesink Consulting Group
* **Arkadyi Maydanchik** – audit datové kvality
* **Dannette McGilvray** – metodika 10 steps
* **Sunil Soares** – Big Data Quality
* **John Ladley** – Data Governance
* **Henrik Gabs Liliendahl** - https://liliendahl.com/ (MDM, Data Quality)
* **Alex Berson a Larry Dubov** – Master Data Management

## Lab

Pro vypracování semestrální práce potřebujete data modelové firmy dostupné jako SQL dump z MySQL / MariaDB databáze. SQL soubor je dostupný z Teams.

Na cvičeních budeme používat vlastní virtuální prostředí (VM/Docker) + Jupyter Notebook s MySQL kernelem (alternativně můžete používat VS Code s příslušnými pluginy)

### Rozhodovací matice pro prostředí
* Windows + nechci si ušpinit ruce: předpřipravaný OVA pro VirtualBox
* Windows + chci si ušpinit ruce: vytvořit vlastní VM pro VirtualBox
* Mac M1+ (nejsnazší cesta): Docker Desktop + předpřipravené YAML pro docker compose
* Linux: VirtualBox nebo Docker + virtualenv nebo Jupyter container

### Další nástroje
* Validace dat (technické testy): Great Expectations (GX) (https://greatexpectations.io), DBT Tests (Pokud budete nahrávat csv soubory do DB modelu)
* Data Profiling: Ydata Profiling (Python library)
* Další free nástroje: OpenRafine,  SODA Core (https://www.soda.io), MobyDQ, Deequ, Quadient DataCleaner, Apache Griffin, DataKitchen (https://datakitchen.io)
* Ataccama DQ Analyzer (stažitelný na www.ataccama.com) + Atacama ONE Profiler (online)
* DataCleaner Community Edition dostupný na https://datacleaner.github.io (data profiling, data wrangling, etc.)
* Open Source Data Quality and Profiling dostupný na https://sourceforge.net/projects/dataquality (profiling, metadata discovery, anomaly detection, deduplication, standardization, address correction, data masking)
* Vlastní nástroj napsaný v SQL + jakýkoliv jazyk (R, Java, Python, ...)
* Claude Pro + skills + MySQL MCP Server
* Python + HTML/JavaScript generovaný Claude

