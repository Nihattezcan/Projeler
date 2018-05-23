# kripto-me-ajla-ma
asd

sayi = [1,3,5,7,9,11,13,15,17,2,4,6,8,10,12,14,16,19,21,23,18,20,22,24,26,27,28] # Random olarak oluşturulabilir. 
alfabe = "abcdefghij klmnoprstuvyzxwq"
alinan_cumle = input("bir cümle giriniz> ")
def matris(girilen_cumle):
    yeni_matris = []
    for i in girilen_cumle:
        for k in range(len(alfabe)):
            if (i == alfabe[k]):
                b = sayi[k]
                yeni_matris.append(b)
    while True:
        h = sayi[10]
        kalan = len(yeni_matris) % 3
        if (kalan == 0):
            break
        elif (kalan == 1):
            yeni_matris.append(h)
            yeni_matris.append(h)
        else:
            yeni_matris.append(h)

    return yeni_matris
print(len(matris(alinan_cumle)))
print(matris(alinan_cumle))



def giden_mesaj(sifre_matrisi,yeni_matris):
    giden_mesaj = []
    birinci = []
    ikinci =[]
    ucuncu = []
    birinci.append(sifre_matrisi[0])
    birinci.append(sifre_matrisi[1])
    birinci.append(sifre_matrisi[2])
    ikinci.append(sifre_matrisi[3])
    ikinci.append(sifre_matrisi[4])
    ikinci.append(sifre_matrisi[5])
    ucuncu.append(sifre_matrisi[6])
    ucuncu.append(sifre_matrisi[7])
    ucuncu.append(sifre_matrisi[8])
    while True:
        n = int(len(yeni_matris))

        if (n == 0):
            break

        giden_mesaj.append(int(birinci[0]*yeni_matris[0])+int(birinci[1]*yeni_matris[1])+int(birinci[2]*yeni_matris[2]))
        giden_mesaj.append(int(ikinci[0]*yeni_matris[0])+int(ikinci[1]*yeni_matris[1])+int(ikinci[2]*yeni_matris[2]))
        giden_mesaj.append(int(ucuncu[0]*yeni_matris[0])+int(ucuncu[1]*yeni_matris[1])+int(ucuncu[2]*yeni_matris[2]))
        del yeni_matris[0]
        del yeni_matris[0]
        del yeni_matris[0]
    return giden_mesaj


a = matris(alinan_cumle)
sifre_matrisi = []
alinan_sifre = input("lütfen bir şifre belirleyiniz>") 

for h in alinan_sifre:
    sifre_matrisi.append(int(h))
sonuc = giden_mesaj(sifre_matrisi,a)
print(sifre_matrisi)
print(sonuc)





