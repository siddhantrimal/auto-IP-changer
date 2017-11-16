# Auto IP Changer
Simple script to invoke elevated automatic configuration of pre-defined IP settings, in command shell
* Based on [Elevate - Version 4][1]
* Built for cmd.exe (_not_ Powershell)

More about older versions of this [here][2]

## Why was this necessary?
Because (1) I'm a lazy fellow and (2) you should use automation whenever possible. Personally, I've bound this script to a hotkey `Ctrl+Shift+I` and enjoy a quick network configuration switch everytime I go from Lab-to-Home and vice-versa, so on and so forth.  

## Usage
1. Download `autoIPsetter.bat`
1. Edit and configure it to your liking. (_Editing is available in right-click context menu, as a text file_)
	* There following are the defaults

			REM ----------PRESET SETTINGS-------
			set varIP=10.0.80.50
			REM WRITE YOUR COMPUTER IP ABOVE
			set varDefaultGateway=10.0.80.1
			set varSubnetMask=255.255.255.192
			REM --------------------------------
1. Run it. _Thats about it_.

## Known Issues:
1. `The filename,directory name, or volume label syntax is incorrect. System cannot find the file specified.`
	* Don't worry, its just a case of self-referencing error on first-run. Please close the batch file and run again, it should not show the error again. Its a self-healing code and creates correct references on the second run.
2. __The batch file was working fine but it stopped running suddenly!__
	* Yes, this is also a known issue. Its not actually the Batch-file failing to run, its the side-effect of the said Deadpool-like healing-factor from point#1. The batch file hard-codes the path where it is executed into its own code when it is executed the first time. If you notice the code, there is a certain reference command !batchPath! . This is overwritten on the first pass(i.e. first execution of the batch file). Since the batch file writes itself, it is unavoidable. It is advisable to keep a copy of the original before using (_or, you can just visit the repo page again, if you lose the original; link is in the file footer attribution_)
> Any more issues? Well, I don't know. [Why don't you tell me?][99]

## License
Standard MIT License. See the [LICENSE file][100]

[1]: http://stackoverflow.com/a/12264592/5040900
[2]: http://cod3r.blogspot.com/2017/03/elevatedbatchprocessingoftogglecode.html

[99]: https://github.com/siddhantrimal/auto-IP-changer/issues
[100]: https://github.com/siddhantrimal/auto-IP-changer/blob/master/LICENSE