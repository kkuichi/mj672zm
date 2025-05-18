**README.md**
## BAKALÁRSKA PRÁCA

# ANALÝZA VYBRANEJ DÁTOVEJ VZORKY NA PREDIKCIU VÝŠKY PRÍJMU

### Michal Jiříček
    # ŠKOLITEĽ: Ing. Anna Biceková, PhD.
    # ROK: 2024/2025
    # UNIVERZITA: Technická univerzita v Košiciach
    # FAKULTA: Fakulta Elektrotechniky a Informatiky
    # ŠTÚDJINÝ ODBOR: Informatika
    # ŠTUDIJNÝ PROGRAM: Hospodárska informatika

`Bakalárska práca sa zaoberá klasifikáciou dát do dvoch binárnych príjmových kategórií s využitím modelov strojového učenia. Zdrojové dáta jednotlivých občanov USA boli extrahované z databázy Census v roku 1994. Teoretická časť práce sa zaoberá príjmovou situáciou v Spojených štátoch a analýzou súčasného stavu. Praktická časť nadväzuje na nadobudnuté poznatky a postupuje pomocou metodológie CRISP-DM. Využitých je 5 modelov strojového učenia: kNN, Náhodný les, Rozhodovací strom, Logistická regresia a Naivný Bayes. Výsledky jednotlivých modelov sú vizuálne zobrazené pomocou ROC kriviek a matíc zámen.`

### ODKAZ NA DOSTUPNÉ DÁTA:
https://archive.ics.uci.edu/dataset/20/census+income

### PÔVODNÝ OBSAH (obsah po stiahnutí z UCI Irvine Machine Learning Repository):

- **adult.data** --> dáta určené na trénovanie
- **adult.names** --> popis datasetu
- **adult.test** --> dáta určené na testovanie 
- **Index** --> zoznam súborov a ich veľkosti
- **old.adult.names** --> starší popis datasetu

### AKTUÁLNY OBSAH:

- **adult.data** --> pôvodné dáta určené na trénovanie
- **adult.names** --> pôvodný popis datasetu
- **adult.test** --> pôvodné dáta určené na testovanie 
- **Index** --> pôvodný zoznam súborov a ich veľkosti
- **old.adult.names** --> pôvodný starší popis datasetu
- **BAKALARSKA_PRACA.ipynb** --> zdrojový kód práce
- **dataset.csv** --> očistené celkové dáta numerického typu
- **numericky_dataset.csv** --> očistené numerické atribúty numerického typu
- **trenovacie_data.csv** --> očistené celkové dáta numerického typu určené na trénovanie
- **numericke_trenovacie_data.csv** --> očistené numerické atribúty numerického typu určené na trénovanie
- **testovacie_data.csv** --> očistené celkové dáta numerického typu určené na testovanie
- **numericke_testovacie_data.csv** --> očistené numerické atribúty numerického typu určené na testovanie
- **README.md** --> aktuálny súbor s informáciami o zdrojovom kóde práce

### POŽIADAVKY:

1. Verzia Pythonu: **3.11.9** (testovaná verzia) alebo iná kompatibilná, stiahnuteľná z: https://www.python.org/downloads/.
2. JupyterLab alebo VS Code s rozšíreniami.
* Odporúčané rozšírenia pre Visual Studio Code: 
    - Jupyter
    - Jupyter Cell Tags
    - Jupyter Keymap
    - Jupyter Notebook Renderers
    - Jupyter Slide Show
    - Rainbow CSV
3. Nainštalované knižnice.
* Odporúčané verzie knižníc, ktoré boli využité pri praci. 
    - **seaborn**       -> 0.13.2
    - **pandas**        -> 2.2.3
    - **numpy**         -> 2.2.2
    - **matplotlib**    -> 3.10.0
    - **scikit-learn**  -> 1.6.1
     - **ipykernel**  -> 6.29.4
                    
### ODKAZY NA VYUŽITÉ KNIŽNICE:

- https://seaborn.pydata.org/index.html
- https://pandas.pydata.org/docs/index.html
- https://numpy.org/doc/2.1/index.html
- https://matplotlib.org/3.5.3/index.html
- https://scikit-learn.org/stable/

### INŠTALÁCIA KNIŽNÍC:
* Kniznice môžeme priamo inštalovať v prostredí Jupyter Notebook pomocou príkazu:

``` %pip install seaborn pandas numpy matplotlib scikit-learn ipykernel ```

### POPIS ATRIBÚTOV:

- **age** -> numerický atribút typu integer, vek jednotlivca
- **workclass** -> kategorický atribút, pracovná trieda jednotlivca 
- **fnlwgt** -> numerický atribút typu integer, vážené záznamy špecifikovaných ekonomických charakteristík
- **education** -> kategorický atribút, dosiahnuté vzdelanie jednotlivca 
- **education-num** -> numerický atribút typu integer, počet rokov vzdelávania jednotlivca
- **marital-status** -> kategorický atribút, rodinný stav jednotlivcov 
- **occupation** -> kategorický atribút, povolanie jednotlivcov 
- **relationship** -> kategorický atribút, aktuálny vzťah jednotlivca 
- **race** -> kategorický atribút, rasa jednotlivca 
- **sex** -> kategorický binárny atribút, pohlavie jednotlivca 
- **capital-gain** -> numerický atribút typu integer, kapitálový príjem jednotlivca
- **capital-loss** -> numerický atribút typu integer, kapitálová strata jednotlivca
- **hours-per-week** -> numerický atribút typu integer, počet odpracovaných hodín jednotlivca za týždeň
- **native-country** -> kategorický atribút, krajina pôvodu jednotlivca 
- **income** -> cieľový kategorický binárny atribút, určovanie ročného príjmu nad a pod 50 tisíc USD 
---------
- **net_capital** -> vzniká v priebehu práce, predstavuje kapitálový zisk alebo stratu (stĺpec capital-gain - capital-loss)




