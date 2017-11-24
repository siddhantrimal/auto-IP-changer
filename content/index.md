---
date: 2016-03-08T21:07:13+01:00
title: auto IP changer
type: index
weight: 0
---

## Stupidly simple

1. Change the frontmatter in plaintext.

	```
	REM ----------PRESET SETTINGS-------
	set varIP=10.0.80.50
	REM WRITE YOUR COMPUTER IP ABOVE
	set varDefaultGateway=10.0.80.1
	set varSubnetMask=255.255.255.192
	set varPrimaryDNS=4.2.2.2
	set varSecondaryDNS=8.8.8.8
	REM --------------------------------
	```

2. Run it once to setup.

3. It's ready to work.

## Go one step further

* After setting up, right-click on the batch-file and create shortcut
* Right-click on the shortcut file and go to __Properties > Shortcut Key__
* Bind the shortcut to some hotkey (say) `Ctrl+Shift+'`

## Watch it work

![][1]

[1]: img/autoIPchanger-demo.gif