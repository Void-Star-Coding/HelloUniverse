What is Chocolatey?
  Chocolatey is a package manager allowing you to swiftly download and install files and tools, somewhat analogous to Linux apt

Installation:
  Open Elevated Powershell
  > Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
  
  How to use Chocolatey
    Installing
      Check out the packages at https://community.chocolatey.org/packages
      Choose a package you want, then in elevated console
      > choco install <packagename>
      You can install multiple packages at once separated by spaces