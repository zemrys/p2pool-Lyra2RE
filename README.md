P2Pool Server Node software for Lyra2RE coins. Currently supported:
* Vertcoin [VTC]

Requirements:
-------------------------
Generic:
* Coindaemon >=0.10.0
* Python >=2.6
* Twisted >=10.0.0
* python-argparse (for Python =2.6)

Linux:
* sudo apt-get install python-zope.interface python-twisted python-twisted-web
* sudo apt-get install python-argparse # if on Python 2.6

Windows:
* Install Python 2.7: http://www.python.org/getit/
* Install Twisted: http://twistedmatrix.com/trac/wiki/Downloads
* Install Zope.Interface: http://pypi.python.org/pypi/zope.interface/3.8.0
* Install python win32 api: http://sourceforge.net/projects/pywin32/files/pywin32/Build%20218/
* Install python win32 api wmi wrapper: https://pypi.python.org/pypi/WMI/#downloads
* Unzip the files into C:\Python27\Lib\site-packages


Running P2Pool:
-------------------------
To use P2Pool, you must be running your own local bitcoind. For standard
configurations, using P2Pool should be as simple as:

    python run_p2pool.py

Then run your miner program, connecting to 127.0.0.1 on P2Pool-port with any
username and password.

If you are behind a NAT, you should enable TCP port forwarding on your
router. Forward port 9333 to the host running P2Pool.

Run for additional options.

    python run_p2pool.py --help


Official P2Pool wiki:
-------------------------
https://en.bitcoin.it/wiki/P2Pool


Alternate web front ends:
-------------------------
* https://github.com/hardcpp/P2PoolExtendedFrontEnd
* https://github.com/johndoe75/p2pool-node-status


Notes for Lyra2RE-Coins:
=========================

Requirements:
-------------------------
In order to run P2Pool with the Lyra2RE-Coins, you would need to build and install the
lyra2re_hash module that includes the Lyra2RE proof of work code that Lyra2RE-Coins uses for hashes.

Linux:

    git clone https://github.com/metalicjames/lyra2re-hash-python.git
    cd ~/lyra2re-hash-python
    sudo python setup.py install

Windows (mingw):
* Install MinGW: http://www.mingw.org/wiki/Getting_Started
* Install Python 2.7: http://www.python.org/getit/

In bash type this:

    git clone https://github.com/metalicjames/lyra2re-hash-python.git
    cd ~/lyra2re-hash-python
    /c/Python27/python.exe setup.py install

Running P2Pool:
-------------------------
Vertcoin: 
* Run P2Pool with the "--net vertcoin", "--net vertcoin2" (if you want to connect to 2nd network) or "--net vertcoin3" (for 3rd network) option.
* Run your miner program, connecting to 127.0.0.1 on port 9171, 9172 (for 2nd network) or 9174 (for 3rd network).

Sponsors:
-------------------------

Thanks to:
* The Bitcoin Foundation for its generous support of P2Pool.
* The Litecoin Project for its generous donations to P2Pool.
* The Vertcoin Community for its great contribution to P2Pool.

