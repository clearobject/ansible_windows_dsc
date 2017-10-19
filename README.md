## win_dsc ansible

WinAnsible Intro:
* http://docs.ansible.com/ansible/latest/intro_windows.html#windows-system-prep

Documentation for win_dsc module:
* http://docs.ansible.com/ansible/latest/win_dsc_module.html

Windows side visibility:
* See what winRM is up to:
  * Applications and Services/Microsoft/Windows/Windows Remote Management/Operational
  * Get-WinEvent -LogName Microsoft-Windows-WinRM/Operational

* See what DSC is up to:
  * Applications and Services/Microsoft/Windows/Desired State Configuration
  * Get-WinEvent -LogName "Microsoft-Windows-Dsc/Operational"
  * https://docs.microsoft.com/en-us/powershell/dsc/troubleshooting#where-are-dsc-event-logs

DSC working directory:
* C:\Windows\System32\Configuration

DSC Resource documentation: 
* Nice documentation for builtins: https://docs.microsoft.com/en-us/powershell/dsc/builtinresource
* Source for builtins: https://github.com/PowerShell/DscResources/tree/master/DscResources
* Source for add-on resources: https://github.com/PowerShell/DscResources/tree/master/xDscResources
  * There are a lot of intesting options in this list.
* http://www.powershellgallery.com/packages?q=Tags%3A%22DSCResourceKit%22

The included domain playbook makes use of https://github.com/PowerShell/xActiveDirectory by placing it in C:\Windows\System32\WindowsPowerShell\v1.0\modules, which is included on $env:PSModulePath. Details for this: https://blogs.msdn.microsoft.com/powershell/2013/12/05/how-to-deploy-and-discover-windows-powershell-desired-state-configuration-resources/

