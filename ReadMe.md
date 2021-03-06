# Wintellect PowerShell Module #

After posting many random PowerShell scripts in my [blog ](http://www.wintellect.com/devcenter/author/jrobbins), I packaged them up into a common module to make sharing and incorporating easier. Please fork and let me know if there's any bugs you find. I hope you find it useful.

WintellectPowerShell is in the [PowerShell Gallery](https://www.powershellgallery.com/packages/WintellectPowerShell/). To install, execute the following command:

	Install-Module -Name WintellectPowerShell -Scope CurrentUser

If you had a previous version of WintellectPowerShell installed and you get an error about the 'Authenticode issuer' that is because I had to renew my code signature file. Add the -SkipPublisherCheck to the above command. All required files are properly digitally signed.

Here's the about text showing all cmdlets. Of course, all cmdlets have detailed help for more information.

	TOPIC
	    about_WintellectPowerShell
    
	SHORT DESCRIPTION
	    Provides cmdlets for setting up symbol servers and other 
	    functionality related to debugging and performance tuning.
	           
	LONG DESCRIPTION
        This module makes setting up symbol servers and source server debugging 
        functionality easier to control for Visual Studio 2013 through 2017 
        and WinDBG. Setting up a development machine for symbol server 
        access is more difficult than it needs to be but no more.
		
        You can have any combination of Visual Studio 2013 through 2017, and
        WinDBG on the computer for these cmdlets to work.
		
        These cmdlets had been originally developed as PowerShell scripts by John 
        Robbins and released on his blog. This module combines all the separate 
        scripts to make everything easier to manage.
		
        If you have any questions, suggestions, or bug reports, please contact John 
        at john@wintellect.com.
					
        The following cmdlets are included.

	
	    Cmdlet                         Description
	    ------------------             ----------------------------------------------
        Set-SymbolAndSourceServer      Sets up a computer to use a symbol and source
	                                   server. (Combines Set-SymbolServer and 
                                       Set-Source Server)

	    Set-SymbolServer               Sets up a computer to use a symbol server.
	        
	    Get-SymbolServer               Returns a hashtable of the current symbol 
	                                   server settings.
	
	    Set-SourceServer               Sets the source server directory.
	
	    Get-SourceServer               Returns a hashtable of the current source 
	                                   server settings
	        
	    Get-SourceServerFiles          Prepopulate your symbol cache with all your
	                                   Source Server extracted source code.
	                
	    Get-SysinternalsSuite          Gets all the wonderful Sysinternals tools
	        
	    Get-Uptime                     Returns how long a computer has been running.
	        
	    Test-PathReg                   Utility function to test is a registry key 
	                                   property exists in a key.
	
	    Remove-IntelliTraceFiles       Removes no longer needed IntelliTrace files.
	
	    Compare-Directories            Compares two directories.
	
	    Merge-HashTables               Utility function to merge two hash tables 
	                                   together.
	
	    Set-ProjectProperties          Makes setting Visual Studio project options 
	                                   super easy.
	
	    Add-NgenPdbs                   Easily create PDB files from NGEN'd images on 
	                                   a machine.
	
	    Set-Environment                Alias to "set" to bring the DOS set command 
	                                   to PowerShell.
	
	    Invoke-CmdScript               Executes a CMD script and imports the 
	                                   environment variables set in the script to 
	                                   the current PowerShell instance.
	
	    Import-VisualStudioEnvironment Executes the specified Visual Studio 
	                                   VCVARSALL.BAT file importing the environment
	                                   variables into PowerShell for command line
	                                   usage.

        Set-Signatures                 Makes digitally signing files a lot easier by
                                   	   looking for the first non-Azure code signing 
                                       file and picking the timestamp server.

        Get-DumpAnalysis               Automates analyzing a bunch of minidump  
                                       files using CDB and debug scripts.

	
	SEE ALSO
	    Online help and updates: 
	            http://www.wintellect.com/devcenter/author/jrobbins
	    GitHub repository      : 
	            https://github.com/Wintellect/WintellectPowerShell