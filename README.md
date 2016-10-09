# RAUPJC JMBAG 0036487047
# 1.
U sadržaju Bin/Debug foldera pojavili su se ClassLibrary1.dll i ClassLibrary1.pdb.  
Nakon što maknem ClassLibrary1.dll i pokrenem .exe , aplikacija se ruši s pojavom Unhandled Exception 
" System.IO.FileNotFoundException: Could not load file or assembly 'ClassLibrary1 .."
Do pogreške dolazi jer datoteka KonzolnaAplikacija koristi funkcionalnosti iz asemblija ClassLibrary1.dll i zahtijeva njenu prisutnost.
Na Vaš zahtjev poslat cu vam .exe i .dll datoteke.
# 2.
Nakon izmjene stringa metode PrintHelloWorld() , konzolna aplikacija nije prikazala novi string jer nismo preveli ClassLibrary projekt 
,a CLR  prije pokretanja main metode učitava sve asemblije , kako ClassLibrary asemblij nije preveden prikazana je stara verzija stringa.
# 3.
Nakon pokretanja aplikacije ispisalo se: Pero: Hello World  .
# 4. 
Nakon što sam dodao PeroClassLibrary kao referencu u bin/Debug folderu vidim PeroClassLibrary.dll , asemblij koji sam koristio 
u programu KonzolnaAplikacija, konkretno metodu PrintHelloWorld() .
# 5. 
Nakon što obrišem originalni .dll na disku , aplikacija se uredno pokreče jer sada se referencira na PeroClassLibrary.dll iz bin/debug 
foldera.
