# eos
Equation of State files for use in the RNS program.

The format required is as follows:
line 1) number of tabulated points in file
remaining lines) four columns:

column 1) energy density/c^2 	(g/cm^3)
column 2) pressure		(dynes/cm^2)
column 3) enthalpy 		(cm^2/s^2)
column 4) baryon number density (cm^{-3})

The program HnG.c can be used to convert an equation of state in the form
energy density vs pressure to Nick's format. Look at a listing of the 
c code to learn how to use  the program. 

EOS included in this library:

APR = Akmal, Pandharipande, & Ravenhall, (1998) Phys Rev C 58,1804
3-body potential formalism including special relativistic corrections
      
ABPR = Alford, Braby, Paris & Reddy (2005), ApJ 629, 969-978
		Mixed Phase Hybrid Quark Star - EOS given in ABPR 
		with gap energy = Delta=0, m_s = 180 MeV 
		in all 3 cases Colour Flavour Locked eos are matched to APR 
      eosABPR1	B^{1/4}=140.0 MeV, c=0.3
      eosABPR2	B^{1/4}=161.3 MeV, c=0
      eosABPR3	B^{1/4}=167.0 MeV, c=0
      
BBB = Baldo, Bombaci & Burgio, A&A 328, 274-282 (1997)
    Hadronic EOS (2 versions, see paper)

HLPS = Hebeler, Lattimer, Pethick & Schwenk (2013), ApJ 773
Representative EOS that span a realistic (from a nuclear viewpoint) range of stiffness.
HLPS1 = softest EOS; HLPS3 = stiffest EOS

Single Letters of the Alphabet: eosX, where X = {A,B,C,F,G,L} = EOS from the Arnett & Bowers Catalog
Arnett and Bowers (1977) APJS 33, 415
These are VERY out of date and are only included for historical reasons.
	Example:
	L = PANDHARIPANDE AND SMITH (MEAN FIELD): Arnett & Bowers EOS L
	Unrealistically stiff EOS, useful if you need a really big star.
