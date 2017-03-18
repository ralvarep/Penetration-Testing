# Penetration Testing

This repository provides a virtual scenario of Penetration Testing to explore vulnerabilities.

Demo scenario has been created using [Virtual Networks over linuX (VNX)](http://www.dit.upm.es/~vnx/).

Index:
- [Requirements](https://github.com/ralvarep/Penetration-Testing#requirements)
- [Scenario](https://github.com/ralvarep/Penetration-Testing#scenario)
- [Usage](https://github.com/ralvarep/Penetration-Testing#usage)
- [Author](https://github.com/ralvarep/Penetration-Testing#author)
- [References](https://github.com/ralvarep/Penetration-Testing#references)


## Requirements

 - VNX installed [(VNX Installation Guide)](http://web.dit.upm.es/vnxwiki/index.php/Vnx-install)
 - Operating System: Ubuntu 16.04
 - Hard Drive: 40 GB avaible space (Filesystem size)
 - Memory: 8 GB RAM or more


## Scenario

![Scenario](https://raw.githubusercontent.com/ralvarep/Penetration-Testing/master/img/scenario.jpg)


## Usage

**STEP 1: Clone this repository**
~~~
$ git clone https://github.com/ralvarep/Penetration-Testing.git
~~~

**STEP 2: Build filesystems**
~~~
$ filesystems/create-rootfs_all
~~~
This step may take several minutes, depending on your Internet connection. It will download all the necessary filesystems of the virtual machines.

**STEP 3: Create virtual scenario**
~~~
$ sudo vnx -f Penetration-Testing.xml -t
~~~
When the scenario is created, you can login to consoles with root:xxxx.

**STEP 4 (Optional): Network Configuration in Windows 7**

If you want to use Windows 7 in the scenario, you have to configure the following network settings:

* For IPv4:

![Configuration-IPv4](https://raw.githubusercontent.com/ralvarep/Penetration-Testing/master/img/windows7/configuration-ipv4.png)

* For IPv6:

![Configuration-IPv6](https://raw.githubusercontent.com/ralvarep/Penetration-Testing/master/img/windows7/configuration-ipv6.png)

**OTHER OPTIONS:**

* Launch terminal of some virtual machine
~~~
$ sudo vnx -f ONOS-vRouter.xml --console -M VM-NAME
~~~
* Shutdown scenario
~~~
$ sudo vnx -f ONOS-vRouter.xml --shutdown
~~~
* Start scenario that has previously been shutdown
~~~
$ sudo vnx -f ONOS-vRouter.xml --start
~~~
* Destroy scenario
~~~
$ sudo vnx -f ONOS-vRouter.xml -P
~~~


## Author
This project has been developed by [Raúl Álvarez Pinilla](https://es.linkedin.com/in/raulalvarezpinilla) as a result of the [Specialit's Degree in Information and Computer Security](http://www.esii-2.posgrado.uclm.es) at University of Castilla-La Mancha.


## References

 *  [Kali Linux](https://www.kali.org/)
 *  [Metasploit Lab Environment](https://www.offensive-security.com/metasploit-unleashed/requirements/)
 *  [Test Microsoft Edge and versions of IE8 through IE11 using free virtual machines](https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/)
