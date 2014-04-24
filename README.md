organizedtextextracts
=====================

Extracting organized text from PDF's with python

I got PDFMiner to extract text and create an html which I then use HTMLParser and urllib to remove all HTML tags so I can get the bare text from the pdf (this part works great, absolutely no data is lost during the process.

The problem I have is that the string (extracted from the PDF converted to HTML) is not organized usefully. I'm working on this problem right now and I'm trying to come up with creative ways around it. Here is where you can find the pdf that I'm converting to html and then to a string stripped of all tags. (http://apps.oakgov.com/egov0003/controller?cmd=jailfile&filename=inmates.pdf)

Here is the result of the module I made.

print text[:1000]

Page 1
Current Oakland County Jail Inmates
(Highlighted inmates have active holds)
Name
Inmate Id Book Date Date of Birth Sex Jail Location
Court
ABBEY, BRENDA LEE
393575
4/23/2014
10/9/1962
ABBOTTSARDIN, JOSEPH 
390477
7/10/2013
8/31/1989
ABERLICH, CHRISTOPHER GEORGE
ABNER, RANDOLF 
392913
152694
11/7/2013
2/27/2014
8/3/1982
3/2/1960
ABRAMS, CLINTON ALFRED
ABRAMS, KYLE ELLIOT
298103
331231
10/28/2013 8/31/1970
8/13/1984
4/4/2014
F
M
M
M
M
M
OCJL-ANNEX
52/3 DC/ROCHESTER HI
BLK-FO CELL-1
46TH DC/SOUTHFIELD
BLK-ZT CELL-1
TEMP MALES
6TH CIRCUIT COURT
6TH CIRCUIT COURT
OCJL-ANNEX
OAKLAND CO JAIL
6TH CIRCUIT COURT
52/1 DC/NOVI
52/2 DC/CLARKSTON
Charge Description
Operating Under the
Influence of Alcohol /
Liquor OWI
DWLS / DWLR
Vehicle Theft UDAA
Weapons Offense (Other)
Dangerous Drugs (Other)
DWLS / DWLR
Sex Offense (other)
Carrying Concealed
AGGR. FEL.
ASSAULT-FAMILY-OTHE
R WEAPON
ACKLIN, ERIC DAVID
369392
8/26/2013
12/10/1961
M
OCJL-ANNEX
48TH DC/BLOOMFIELD H Retail Fraud Theft 2nd
D

As you can see, the order is nearly lost. I need a way around this. Check out my module called convertpdf2text. When you use the module, you have to import it like so.

import convertpdf2text
from convertpdf2text import *
