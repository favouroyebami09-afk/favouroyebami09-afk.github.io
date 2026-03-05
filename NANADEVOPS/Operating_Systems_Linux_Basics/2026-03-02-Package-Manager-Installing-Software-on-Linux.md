<h1> Installing a software on Linux </h1>

```console 
Software Package:  compressed archive that contains all the files that are required by a 
specific software to run. 
    -software applications usually have depenedencies 
    -package manager is already included in every Linux distribution, ex: Ubuntu 
    -Ubuntu have a package manager called APT (Advanced Package Tool)

apt search [package_name] > search for a given package
    ex: apt search openjdk

apt install [package_name1] [package_name2] > installs multilple package with one command 
apt remove [package_name] > remove install app

Overall a 'Package Manager' is a central place to install, upgrade, configure, remove software.
-Package manager fetches package from a repository 
-Always update the package index before upgrading or installing new packages
    -sudo apt update 
```

<h3> Common Ways of Installing Software on Linux </h3>

```console 
1. Apt- Package Manager 

2. Snap- Package Manager 

3. Add Repository

4. Ubuntu Software Center 
```


