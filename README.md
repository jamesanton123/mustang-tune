
	
egr and thermactor are disabled by default in a9l2

Done:
	ALOSL, AHISL	Injector Slopes	Input your injector's manufacturer's recommended values if available or scaled percentage, see Note** below for no data 
	FN 389			Injector Breakpoint
	FN 367			Injector Offset	
	FN 348			Crank PW  (when x >=180, I set y to 1.14. This was done by calculating 3.55 * (19/60) ).
	FN 036			Use specs from for lightning 90mm maf http://www.efidynotuning.com/maf.htm
	Tune maf at different mafV values
	Take car for test run
	
	Load scaled
	0			0
	1300		44
	2600		64
	3900		72
	5200		67
	6500		
	
	
		
TODO:
	FN 904A			Sealevel Spark Table
	FN 035			Load Scaling (do this with supercharger belt removed in second gear, and every 1300 rpm, not the maximum load you can achieve)
	Need to dial in fuel by either injector slopes or maf transfer (@decipha https://eectuning.org/forums/viewtopic.php?t=19709)
	adjust the maf curve or injector values to get the wideband to spit out the afr the ecu is telling it to (LAMBSE) the LAMBSE is the Lambda (AFR) the ecu is DEMANDING, if your lambse is 1.160 at WOT and your wideband reads 0.990 lambda at WOT then you are RICH and you need to pull some fuel out just for clarification

	
Unscaled injector data
	FRPP 60 lb/hr @ 39.15psi
	LU60
	Siemens Deka 60 lb/hr
	Low Slope	63.187
	High Slope	60.267
	Breakpoint	0.00003363 on efidynotune data, but I used 3.363 as per https://eectuning.org/forums/viewtopic.php?p=95717	
	voltage offset(ms)
	16.00	0.312
	15.00	0.312
	14.00	0.409
	13.00	0.518
	12.00	0.636
	11.00	0.758
	10.00	0.921
	8.00	1.441
	6.00	2.59
	0.00	2.59
	0.00	2.59
	0.00	2.59 
	


Cranking PW's I'll multiply the factory A9L settings by .317 (got this by doing 19/60)
	