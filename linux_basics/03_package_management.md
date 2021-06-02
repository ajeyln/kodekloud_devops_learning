<h1 align="center"> Package Management </h1>

### Functions of Package managers

* Package Integrity and Authenticity
* Simplified Package Management
* Grouping Packages
* Manage Dependencies

### Types

* DPKG - Debian based distribution
* APT 
* APT-GET
* RPM - Readbased distribution
* YUM
* DNF

### RPM(RedHat Package manager) - Low level package manager

**Operation**

+ Installation - **rpm -ivh packagename.rpm**
+ Uninstallation - **rpm -e packagename.rpm**
+ Upgradation - **rpm -Uvh packagename.rpm**
+ Query - **rpm -q packagename.rpm**
+ Verify - **rpm -Vf <path to file>**

### YUM(Yellowdog Update Modified) - Due to dependency issues

**Operation**

+ RPM based distribution
+ Software Repositories (Collection of packages -/etc/yum.repos.d/package)
+ High level package manager
+ Automatic Dependency Resolution

* yum install package
* yum reporlist - repolists
* yum provide package - to check dependency of package
* yum remove package
* yum update package

### DPKG( Debian package manager) - Low level package manager

**Operation**

+ Installation/Upgrade - **dpkg -i packagename.deb**
+ Uninstallation - **dpkg -r packagename.deb**
+ List - **dpkg -l packagename.deb**
+ Status - **dpkg -s packagename.deb**
+ Verify - **dpkg -p <path to file>**

### APT /APT-GET(Advance package manager) - Due to dependency issues

**Operation**

* apt install package / apt-get install package
* apt update - refresh repos (After installation of OS)
* apt upgrade - upgrade packages
* apt remove package
* apt search package
* apt list | grep package

### LABS

* YUM and RPM - Installed packages using YUM and RPM , eg: YUM Install, rpm -ivh etc.
* DPKG and apt - Installed packages using DPKG and APT , eg: apt remove, dpkg -l etc.


