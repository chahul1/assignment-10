# assignment-10
Q1:
1# Design of tension member
2 Tu float(input("Enter the value of ultimate tensile strength:")
3 fy float(input("Enter the value of yield strength of steel:"))
4 fu= float(input("Enter the value of ultimate strength of steel:")
5 fub float(input("Enter the value of ultimate strength of bolt:")
6 Gamma mo= float(input("Enter the value of partial factor of safety Garmma mo:")
7 Gamma_m1= float(input("Enter the value of partial factor of safety Garmma_m1:")
8 Gamma_mb= float(input("Enter the value of partial factor of safety Gamma_mb:")
9 print ("Gross Area Required")
10 Agreq= 1.1* Tu* 1000/fy
11 print ("The value of gross area required is:", 1.2*Agreq)
12 # Selection of section
13 # Selecting ISA 100x65x8
14 Ag= float(input("Enter the value of gross area of steel is:")
15 Lcl= float(input("Enter the length of connected leg:")
16 Lol = float(input("Enter the length of outstand leg:")
17 t= float(input("Entert the value of least thickness: ")
18 Ag = 1257
19 # Design of connections
20 d = float(input("Enter the value of diameter of bolt:"))
21 do=d + 2
22 print ("The diameter of bolt hole is:", do)
23 # As per IS code minimum pitch distance is
24 pin = 2.5 d
25 print ("The minimum pitch is:", pain)
26 # Edge distance as per IS 800 is
27 e= 1.5 do
28 print ("Enter the value of edge distance:", e)
29 nn= float (input("Number of shear planes with threaded intercepting the shear plane:")
30 ns float (input("Number of shear plane without threads:")

43

31 Anb 0.78 0.7854*d*d
32 print ("threaded area of bolt is:", Anb)
33 Asb =0.7854*d*d
34 print ("plane shank area of bolt is:", Asb)
35 Vdsb= (fub/(1.732* Gamma_mb)" (nn* Anb+ ns Asb) 10*-3)
36 print ("The value of Vdsb:", "Vdsb)
37 kbl = e/(3*do)
38 print ("Kbl:", kb1)
39 kb2 = (pmin/(3*do)) - 0.25
40 print ("Kb2:", kb2)
41 kb3= fub/fu
42 print ("Kb3:", kb3)
43 kb4 = 1
44 print ("Kb4:", kb4)
45 kb min(kb1, kb2, kb3, kb4)
46 print ("Kb:", kb)
47 Vdpb (2.5 kb*d*t*fu*10**-3)/Gamma mb
48 print ("Vdpb:", Vdpb)
49 Vd= min(Vdsb, Vdpb)
50 print ("Vd:", Vd)
51 N =Tu/Vd
52 print ("Number of bolts requird:", N)
53 N= float(input("Enter the value of number of bolts:"))
54 # Check for strength
55 # Criteria 1 Yeilding of Gross Section
56 Tdg (Ag*fy 11-3)/Gamma_mo

Adhav

57 print ("The value of tensile strength due to yielding of gross section is:", Tdg)
58 # Criteria 2 Rupture
59 Anc = (Lc1-(t/2)-do) *t
60 print ("Net Area of Connecting leg is: (Anc):", Anc)
61 Ago (Lol-(t/2) "t

62 print ("Gross Area of outstand leg is: (Anc):", Ago)
63 Lc = (N-1)*pmin
64 print ("Le:", Lc)
65 bs = 0.6 Lcl+ Lol t
66 print ("bs:", bs)
67 =(fy/fu) (bs/Lc) ( Lol/) Beta 1.4 (0.076 (fy/tu) (bs/Lc)* (Lol/t)
68 print ("Beta:", Beta)
69 print ("Check 1")
70 if Beta>1.4:
71print ("Not Safe")
72 else:
73 print ("'Safe")
74 print ("Check 2")
75 if Beta<0.7:
76print ("Not Safe")
77 else:
78 print ("'Safe")
79 Tdn (0.9 fu*Anc)/Gamma_ml) + (Beta Ago*fy/Gamma_mo)
80 print ("'Tdn:", Tcn)
81 # Criteria 3 Block Shear
82 Avg (pmin* (N-1)+e) t
83 print ("'Avg:", Avg)
84 Avn = ((pmi* (N-1) +e)-(N-1)*do+(8.5* do)) t
85 print ("Avn:", Aun)
86 Atg 0.6* Lc1 *t
87 print ("Atg:", Atg)
88 Atn= Atg 0.5* do
89 print ("Atn:", Atn)

d Adhav

90 Tb1 = (((Avg*fy)/(1.732 *Gamma_mo)) +(0.9* fu*Atn)/Gamma_m1)10*-3
91 print ("Tb1:", Tb1)

<5

92 Tb2 = (0.9*Avn*fu)/(1.732* Gamma_m1) +(Atg*fy)/Gamma_mo)) 10*-3
93 print ("Tb2:", Tb2)
94 Tb = min (Tb1, Tb2)
95 print ("Tb", Tb)
96 Td = min(Tdg, Tah, Tb)
97 print ("Td", Td)
98 if Td>Tu:
99 print ("SAFE")
100 else:
101 print ("Revise the Section")
