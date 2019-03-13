# PMF Strojno učenje 2019 - Vježbe

Materijali za vježbe kolegija [Strojno učenje](https://web.math.pmf.unizg.hr/nastava/su/) Prirodoslovno-matematičkog fakulteta (PMF - Matematički odsjek) Sveučilišta u Zagrebu za akademsku godinu 2018./2019. 

## Sadržaj vježbi

* [Vježba 1 - Uvod u osnovne alate i priprema podataka](https://github.com/pmf-strojnoucenje/Vjezbe/blob/master/Notebooks/PMF_SU_2018_Vjezbe1_00_Osnove.ipynb)
* [Vježba 2 - Nadzirano učenje](https://github.com/pmf-strojnoucenje/Vjezbe/blob/master/Notebooks/PMF_SU_2018_Vjezbe2_00_Nadzirani_modeli.ipynb)
* [Vježba 3 - Odabir značajki](https://github.com/pmf-strojnoucenje/Vjezbe/blob/master/Notebooks/PMF_SU_2018_Vjezbe3_00_Odabir_znacajki.ipynb)
* [Vježba 4 - Smanjivanje dimenzionalnosti](https://github.com/pmf-strojnoucenje/Vjezbe/blob/master/Notebooks/PMF_SU_2018_Vjezbe4_00_Smanjivanje_dimenzionalnosti.ipynb)
* [Vježba 5 - Učenje bez nadzora](https://github.com/pmf-strojnoucenje/Vjezbe/blob/master/Notebooks/PMF_SU_2018_Vjezbe5_00_Ucenje_bez_nadzora.ipynb)
* Vježba 6 - Duboko učenje

## Anaconda okruženje

Vježbe se nalaze u obliku Python/Jupyter bilježnica (Jupyter notebooks) i testirane su na Windows, Linux i Mac OS X unutar [Anaconda](https://www.anaconda.com) (Python 3.6) okruženja (verzija 4.4.0). Za prvih pet vježbi vam neće trebati dodatni programski paketi pored onih koji dolaze s Anacondom. Za šestu vježbu (Duboko učenje) trebat će vam [TensorFlow](https://www.tensorflow.org) (verzija 1.6). Preporučamo da instalirate TensorFlow samo s CPU podrškom ako ne koristite računalni sustav s NVIDIA grafičkom karticom i podrškom za CUDA 9.0.

Slijedite uputstva u nastavku za vaš OS (Windows, Linux, Mac OS X):
* Preuzmite i instalirajte programski sustav Anaconda 3 s [https://www.anaconda.com/download/](https://www.anaconda.com/download/)
* Stvorite Anaconda okruženje (conda environment) s Python 3.6 i pretpostavljenim Anaconda Python bibliotekama (pogledajte [conda-cheatsheet](https://conda.io/docs/_downloads/conda-cheatsheet.pdf)). U stvorenom i aktiviranom okruženju mogu se koristiti pripadne Python biblioteke i instalirati nove.
* Instalirajte TensorFlow 1.6 s CPU/GPU podrškom koristeći pip (uputstva na [https://www.tensorflow.org/install/](https://www.tensorflow.org/install/)).

### Windows
TensorFlow instalacija je testirana na 64-bitnim Windows 7 i Windows 10, pošto trenutno nema podrške za TensorFlow na 32-bitnim sustavima. Preporučamo da instalirate TensorFlow u Anaconda okruženje. Preuzmite i instalirajte program Anaconda (Python 3.6) za Windowse s [https://www.anaconda.com/download/](https://www.anaconda.com/download/).

Potom pokrenite Anaconda Command Prompt:
* Stvorite Anaconda okruženje (conda environment) naziva `vjezbe` (možete koristiti naziv po vlastitom izboru):
  ```
  conda create --name vjezbe python=3.6 anaconda
  ```
* Aktivirajte stvoreno okruženje `vjezbe` s:
  ```
  activate vjezbe
  ```
* Instalirajte Tensorflow unutar aktiviranog okruženja `vjezbe`:
  ```
  pip install --ignore-installed --upgrade tensorflow
  ```

Za više informacija o tome kako instalirati programsku biblioteku TensorFlow na Windows OS-u pogledajte [https://www.tensorflow.org/install/install_windows](https://www.tensorflow.org/install/install_windows). Ako već imate stariju verziju programa Anaconda i dalje možete provesti navedenu proceduru, čime ćete instalirati Python 3.6 i učiniti ga dostupnim unutar okruženja `vjezbe`, no možda će biti potrebno naknadno nadograditi neki od Python paketa, primjerice `numpy`. To možete napraviti unutar okruženja `vježbe` na sljedeći način:
  ```
  conda install -c anaconda numpy
  ```
Za više informacija oko rukovanja s Anaconda okruženjima pogledajte [Managing environments](https://conda.io/docs/user-guide/tasks/manage-environments.html) u Anaconda dokumentaciji.

### Linux/Mac OS X
Slično kao i za Windows, najjednostavniji način za instalaciju programskog paketa TensorFlow na Linuxu ili Mac OS X je instalirati ga samo s CPU podrškom unutar Anaconda okruženja prema proceduri opisanoj ranije. Za detaljnija uputstva pogledajte:

* za Linux [https://www.tensorflow.org/install/install_linux#installing_with_anaconda](https://www.tensorflow.org/install/install_linux#installing_with_anaconda)

* za Mac OS X [https://www.tensorflow.org/install/install_mac#installing_with_anaconda](https://www.tensorflow.org/install/install_mac#installing_with_anaconda)

## Github repozitorij

Git je sustav za upravljanje izvornim kodom, klijentski program za korištenje sustava Git možete preuzeti s [https://git-scm.com/downloads](https://git-scm.com/downloads). Iz komandne linije ([Anaconda] Command Prompt na Windowsima ili Terminal na Linux/Mac OS X) pozicionirajte se u željeni direktorij i klonirajte git repozitorij naredbom:
  ```
  git clone https://github.com/PMF-StrojnoUcenje2018/Vjezbe.git
  ```
Kako bi preuzeli ažurirane materijale za vježbe u prije klonirani repozitorij, pozicionirajte se u drirektorij kloniranog repozitorija i preuzmite nove promjene repozitorija koristeći git naredbu:
  ```
  git pull origin master
  ```

Kao alternativnu za gore navedeni postupak možete preuzmiti zip arhivu trenutnog stanja repozitorija s [https://github.com/pmf-strojnoucenje/Vjezbe/archive/master.zip](https://github.com/pmf-strojnoucenje/Vjezbe/archive/master.zip).

## Jupyter
Sve vježbe su spremljene kao Python bilježnice sustava Jupyter [http://jupyter.org/] kojeg možete pokrenuti na sljedeći način iz komadne linije:

* aktivirajte okruženje `vjezbe` (za više detalja pogledajte [conda-cheatsheet](https://conda.io/docs/_downloads/conda-cheatsheet.pdf)):

  - Windows: `activate vjezbe`

  - Linux/Mac OS X: `source activate vjezbe`

* unutar `vjezbe` pokrenite Jupyter notebooks poslužitelj (za detalje pogledajte [uputstva](https://jupyter.readthedocs.io/en/latest/running.html#running)):
  ```
  jupyter notebook --notebook-dir=PATH-TO-REPOSITORY --port=NUMBER-OF-UNUSED-PORT
  ```
  Usmjerite vaš web preglednik na `http://localhost:[NUMBER-OF-UNUSED-PORT]` nakon čega ćete moći navigirati strukturu direktorija i koristiti pripremeljene Python/Jupyter bilježnice za vježbe.
