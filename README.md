Simulacija računalniškega omrežja – Cisco Packet Tracer
--------------------------------------------------------------------
Opis projekta
---------------

Projekt simulira računalniško omrežje treh povezanih lokacij: Ljubljana, Maribor in Kranj. Omrežje je zgrajeno v programu Cisco Packet Tracer in vključuje usmerjanje, varnostne mehanizme, strežnike, VoIP telefonijo in IoT naprave.

Topologija omrežja
-----------------------

3 lokacije, vsaka s svojim usmerjevalnikom (Cisco 2811) in stikalom (Cisco 2960):
Ljubljana – 172.16.0.0/22
Kranj – 172.16.5.0/25
Maribor – 172.16.4.0/24
Usmerjevalniki so med seboj povezani v trikotno topologijo (Kranj – Ljubljana – Maribor – Kranj) prek omrežja 172.16.5.128/29, kar zagotavlja redundanco poti.
Usmerjanje med lokacijami temelji na dinamičnem usmerjevalnem protokolu OSPF.
Varnost
Vsak usmerjevalnik ima nastavljen SSH dostop (uporabniško ime: admin, geslo uporabnika in geslo za router sta ločeno definirana) za varno oddaljeno upravljanje.
Redundantne povezave med lokacijami omogočajo dodatno odpornost omrežja ob izpadu ene povezave.
Strežniki
Vsaka lokacija ima svoj strežnik (npr. strežnik v Kranju, strežnik "IOT mb" v Mariboru), ki opravlja vlogo lokalnega servisa/DNS/IoT nadzora.
VoIP telefonija
V Ljubljani in Kranju so nameščeni IP telefoni (Cisco 7960) z dodeljenimi internimi številkami (npr. 54001, 54002, 55001), kar omogoča simulacijo VoIP klicev znotraj omrežja.
IoT naprave (Maribor)

Lokacija Maribor vključuje dodaten IoT segment:
-------------------------------------------------

RFID bralnik in RFID kartice (pravilna/napačna kartica) za nadzor dostopa
Pametna vrata (Door)
Pametna luč (Light)
Vse naprave so povezane na IoT strežnik in nadzorovane prek lokalnega omrežja

Naslavljanje
----------------------------

Vsaka lokacija ima definiran:

IP naslov usmerjevalnika (gateway)
Masko podomrežja in njen inverz (wildcard mask)
DNS strežnik
Naslovni prostor za končne naprave (PC, laptopi, telefoni, IoT naprave)
Uporabljena orodja
Cisco Packet Tracer

Avtor

Jure Škrlep
