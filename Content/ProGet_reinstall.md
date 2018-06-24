Way To Be a Full Stack C# Programmer
====================================

Package Management ([ProGet](https://inedo.com/proget))
-------------------------------------------------------
ProGet is a tool to help package your application and components which ensure your software is built only once, and then deployed consistently across environments. It supports Docker container and third-party packages: like NuGet, npm, PowerShell, and Chocolatey. 

ProGet is also easy to download and set up on a Window machine(this can also be your server) following the (instruction)[https://inedo.com/support/documentation/proget/installation/installation-guide]. But beware that the port number is set up via the installing wizard. Choose carefully at this stage, since the only way to switch the ProGet service port is by re-installing it again. 

Which brought me here to record down what difficult I have encountered when I re-install the ProGet for changing port purpose. The version I re-install is 5.1 which during the install wizard to re-state the sql server for the web service. The interesting part is, though I have installed sql server express 2016 (further I also tried using sql server express 2017). It keeps failing at the last stage of installation with error _could not stop the service of inedo_. Re-installing the sql server will not solve this problem, since ProGet create itself mdf and log file under Microsoft Service Folder. Remove or rename those files will let PreGet re-install pass. 

To do:
1. ProGet also have the Linux version, might worth to follow when using Linux as service machine.
2. ProGet has the cache folder to cache the package, but how it works is still unclear to me
3. Due to I am trying to maintain the packages in home, there is no build machine to auto build and publish the package yet. When running the install the latest script with Paket, I was running into this package version conflict issue. I am going to tackle this with another blog.

