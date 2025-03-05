# Ulesanne 1
tana=date.today()
print(f"Tere! Täna on {tana}")

# 27/12/2022
tana1 = tana.strftime("%d/%m/%Y")
print(tana1)
# December 27, 2022
tana2 = tana.strftime("%B %d, %Y")
print(tana2)
# 12/27/22
tana3 = tana.strftime("%m/%d/%y")
print(tana3)
# Dec-27-2022
tana4 = tana.strftime("%b-%d-%Y")
print(tana4)

päev=tana.day
kuu=tana.month
aasta=tana.year

print(f"Päev on {päev},\nKuu on {kuu},\nAasta on {aasta}")
paevad=monthrange(2025,2)[1]
onjaanud=paevad-päev
print(f"Kuu lõpuni on jäänud {onjaanud} päevad")
try:
    sünnipäev=input("Sünnipäev: ") #YYYY-MM-DD
    sp=datetime.strptime(sünnipäev,"%Y-%m-%d")
    print(sp)
    vanus_aastades=tana.year-sp.year
    vanus_kuudes=vanus_aastades*12
    print(f"Vastus: Vanus {vanus_aastades} aastad")
except:
    print("Sa pead YYYY-MM-DD format kasutada sisestamisel.")
# Ulesanne 2
#Sulgude kasutamine
print("a=3 + 8/ (4 - 2) * 4")
a=3 + 8 / (4 - 2) * 4
print(a)
print("a=(3 + 8)/ (4 - 2) * 4")
a=3 + (8 / 4) - 2 * 4
print(a)
# Ulesanne 3
 R=float(input("Sisesta R,kus R on ringi raadius:"))
    # ==, !=, <, >, <=, >=
    if R<=0:
        print("Nulliga ja neg. arvudega ei ole mõtte töötada!")
    else:
        Ringi_S=round(pi*R**2,2)
        Ringi_P=round(2*pi*R,2)
        Ruudu_S=2*R*2*R
        Ruudu_P=4*2*R
        print(f"Ringi_S= {Ringi_S}\nRingi_P= {Ringi_P}\nRuudu_S= {Ruudu_S}\nRuudu_P= {Ruudu_P}")
except:
    print("Sisesta ainult arvud!!!")
# Ulesanne 4
maa_raadius_km= 6378         # Maa raadius ekvaatorikohal (km)
myndi_läbimõõt_mm= 25.75     # 2-eurose mündi läbimõõt (mm)
pi= 3,14....    # Pi väärtus täpsemaks arvutuseks
# Arvutused
maa_ümbermõõt_km=2*pi*maa_raadius_km    # Maa ümbermõõt ekvaatoril (km)
maa_ümbermõõt_km=maa_ümbermõõt_km* 1_000_000   # Teisendame millimeetriteks
# Leiame müntid arvu
myntide_arv= maa_ümbermõõt_km / maa_läbimõõt_km
# Tulemuse kuvamine
print(f"Maa ümbermõõdu katmiseks ekvaatori kohal on vaja imbes {int(myntide_arv):,} 2-eurost münti.")
# Ulesanne 5 
a="kill-koll ".capitalize()
b="killadi-koll ".capitalize()
print(2*a,b,2*a,b,4*a) 
# Ulesanne 6
t="""
Rong see sõitis tsuhh tsuhh tsuhh,
piilupart oli rongijuht.
Rattad tegid rat tat taa,
rat tat taa ja tat tat taa.
Aga seal rongi peal,
kas sa tead, kes olid seal?

Rong see sõitis tuut tuut tuut,
piilupart oli rongijuht.
Rattad tegid kill koll koll,
kill koll koll ja kill koll kill.
"""
print(t.upper())
# Ulesanne 7
# Kasutajalt andmete
küsimine laius = float(input("Sisesta ristküliku laius: ")) 
kõrgus = float(input("Sisesta ristküliku kõrgus: ")) 
# Arvutused 
umbermoot = 2 * (laius + kõrgus)  # Ristküliku ümbermõõt
pindala = laius * kõrgus  # Ristküliku pindala
# Tulemuse väljastamine
print(f"Ristküliku ümbermõõt: {umbermoot}")
print(f"Ristküliku pindala: {pindala}")
# Ulesanne 8
# Kasutajalt andmete küsimine
kütus_liitrid = float(input("Sisesta tangitud kütuse hulk (liitrites): ")) 
kilomeetrid = float(input("Sisesta läbitud kilomeetrid: ")) 
# Kontrollime, et kilomeetreid poleks 0, et vältida jagamisviga 
if kilomeetrid > 0: kütusekulu_100km = (kütus_liitrid / kilomeetrid) * 100 # Arvutame kütusekulu 100 km kohta 
print(f"Kütusekulu 100 km kohta on {kütusekulu_100km:.2f} liitrit.") 
else:
print("Viga: läbitud kilomeetrite arv peab olema suurem kui 0.")
# Ulesanne 9
# Algandmed
kiirus_kmh = 29.9  # Rulluisutaja kiirus km/h
# Kasutajalt sisendi küsimine
minutid = float(input("Sisesta minutite arv: "))
# Arvutused
tunnid = minutid / 60  # Teisendame minutid tundideks
kaugus_km = kiirus_kmh * tunnid  # Arvutame läbitud vahemaa
# Tulemuse väljastamine
print(f"Rulluisutaja jõuab {minutid} minutiga umbes {kaugus_km:.2f} km kaugusele.")
# Ulesanne 10
minutid_kasutajalt=int(input("Aeg minutides:"))
tunnid=minutid_kasutajalt//60 # täisosa
minutid=minutid_kasutajalt%60 # jääk
print("vastus".center(20,"*")) # vorminda ise vastus nii: "hh:mm"
