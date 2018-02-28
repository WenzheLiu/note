# install pip without root
First download get-pip.py from web by:
```
$ curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
% Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 1558k  100 1558k    0     0   111k      0  0:00:14  0:00:14 --:--:--  206k
```
Then install pip:
```
python get-pip.py --user
```
Then pip will be installed in user local directory. For Windows 7, the package will be in:
```
$ ls ~/AppData/Roaming/Python/Python27/site-packages/ -a
easy-install.pth  etcd3-0.7.0-py2.7.egg/  pip/  pip-9.0.1.dist-info/  wheel/  wheel-0.30.0.dist-info/
```
Add the path to PYTHONPATH env, so that python can find it higher order if the same with system.
```
Windows: export PYTHONPATH=~/AppData/Roaming/Python/Python27/site-packages
Linux:   export PYTHONPATH=/home/weliu/.local/lib/python2.7/site-packages
```
And the bin will be in:
```
$ ls ~/AppData/Roaming/Python/Scripts/
pip.exe     pip2.7.exe  pip2.exe    wheel.exe
```
Add the bin path to PATH environment, so you can call pip in any directory.

# install lib by pip without root
```
pip install <lib> --user
```
The package will be installed in user local directory.
