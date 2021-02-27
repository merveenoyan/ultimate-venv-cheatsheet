# Virtual Environment Cheatsheet
Bu repo twitch yayınlarım için hazırladığım, farklı virtual environment'ların komutlarını içeren bir kaynaktır.
## Conda
```
* conda info: kurulu olan conda hakkında bilgi verir.
* conda update anaconda: ortam (environment) içindeki bütün paketleri anaconda'daki son versiyonlarına yükseltir.
* conda create --name env_ismi python=3.6: belirlediğiniz isimle 3.6 python'la conda ortamı açar.
* conda activate env_ismi: eğer ortamın bulunduğu klasörün içindeyseniz environment'ın ismini vererek ortamı aktive edebilirsiniz, yoksa path vermeniz gerekir.
* conda deactivate: aktif conda ortamını deaktive eder.
* conda list --name env_ismi: ortamdaki bütün paketleri ve versiyonları listeler
* conda remove --name env_ismi --all: environment'ı siler.
* conda create --clone env_ismi --name yeni_env: environment'ın kopyasını yeni bir isimle oluşturur.
* conda install "PKGNAME>2.5, <3.2": bir paketi yüklerken iki versiyon arasında bulunan bir versiyonunu yükler.
* conda install "PKGNAME[version='3.1.2|3.4.1']": paketin belirtilen versiyonlarından birini yükler.
* conda search PKGNAME --info: paketin versiyonları hakkında fikri verir.
```
## Pyenv
Pyenv hem bilgisayardaki python versiyonlarını kontrol edebileceğiniz hem de sanal ortam açabileceğiniz bir framework.
![](https://files.realpython.com/media/pyenv-pyramid.d2f35a19ded9.png)
```
* brew install pyenv: pyenv'i brew'la kurmanızı sağlar.
* pyenv commands: pyenv komutlarını gösterir.
* pyenv install 3.6.8: python 3.6.8'i indirip kurar.
* pyenv which pip: pyenv ortamının içindeki pip paket yöneticisini gösterir.
* pyenv versions: bilgisayardaki pyenv ortamlarını gösterir.
* pyenv global 3.6.8: globaldeki versiyonu ayarlar.
* pyenv local 2.7.15: bulunduğunuz klasör'de python versiyonunu ayarlar.
* pyenv virtualenv 3.6.5 env_ismi: verilen ortam ismiyle 3.6.5 python ortamı kurar.
* pyenv activate env_ismi: pyenv ortamını aktive eder.
* pyenv which python: pyenv ortamı içindeki python'ın path'ini gösterir.
Not: bash script dosyanıza eval "$(pyenv virtualenv-init -)" yazarsanız direkt olarak bulunduğunuz yerdeki pyenv ortamını direkt aktive eder.
* pyenv deactivate: aktif olan ortamı deaktive eder.
```
## Python3 VENV
```
python3 -m venv env_ismi: verilen ortam ismiyle yeni ortam açar. 
(windows) env_ismi\Scripts\activate.bat: ortamı aktive eder.
(linux/mac) source env_ismi/bin/activate: ortamı aktive eder. 
deactivate: ortamı deaktive eder
```
## pip 
```
pip python'da kullanılan bir paket yöneticisidir. 
pip install paket_ismi: verilen bir paketi yükler.
pip install paket_ismi==2.2.2: verilen bir paketi bir versiyonla yükler.
pip freeze: requirements dosyasındaki dependency'leri gösterir.
pip freeze > requirements.txt: requirements.txt dosyasına ortamın içinde bulunan dosyaları yazar.
pip install -r requirements.txt: requirements.txt dosyasındaki paketleri direkt olarak ortama kurar.
pip install path: belirttiğiniz yoldaki (path) paketi yükler.
```
Kaynaklar: https://docs.conda.io/projects/conda/en/latest/user-guide/cheatsheet.html
https://opensource.com/sites/default/files/gated-content/cheat_sheet_pip.pdf
https://realpython.com/intro-to-pyenv/
