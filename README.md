import random #, rastgelelik sağlamak için kullanılacak fonksiyonları içerir.

kullanım_alanları = [
    "İşveren Sorumlulukları",
    "İşe Alım Süreçleri",
    "İnsan Hakları İhlalleri",
    "Çalışanların Etik Hakları",
    "Çalışan Performansı ve Verimliliği İzleme",
    "Yapay Zeka Eğitimleri ve Farkındalık Programları"
]

potansiyel_etik_sorunlar = [
    "Verinin korunması ve gizliliği ile ilgili konular",
    "Önyargılı kararlar, ayrımcılık",
    "Algoritmaların önyargıları yansıtma potansiyeli",
    "Çalışanın düşünce özgürlüğü, gizlilik hakları ve adil muamele haklarının ihlali",
    "Çalışanın gizlilik hakkının ihlali",
    "Yapay zekanın etik kullanımı konusunda eksik bilgi veya yanılgılar"
]

önerilen_çözümler = [
    "Kanun ve yönetmeliklere uygun hareket etme, bilinçli ve hassas bir tutum sergileme",
    "Yazılımların objektif olmasını sağlama, adil kararlar verilebilmesi için düzenlemeler yapılması",
    "Etik bir çerçeve oluşturma ve bu çerçevenin nasıl tasarlandığının ve nasıl geliştirildiğinin belirlenmesi",
    "Çalışanların haklarını koruma, zarar verebilecek uygulamalardan kaçınma",
    "Gizlilik haklarına saygı gösterme ve kişisel verilerin korunmasına dikkat etme",
    "Eğitim ve farkındalık programlarının düzenlenmesi, yapay zekanın düzgün ve etik kullanılmasının teşvik edilmesi"
]

while True:
    # Yapay Zeka için seçim yap
    seçilen_kullanım_alanı = random.choice(kullanım_alanları) # fonksiyonu kullanılarak rastgele bir kullanım_alanı seçilir.
    soru_index = kullanım_alanları.index(seçilen_kullanım_alanı) #Ardından, seçilen kullanım alanının indeksi alınır ve bu indeks kullanılarak potansiyel etik sorun ve önerilen çözüm bulunur.
    seçilen_etik_sorun = potansiyel_etik_sorunlar[soru_index]
    seçilen_çözüm = önerilen_çözümler[soru_index]

    # Sonuçları yazdır
    print("Yapay Zeka Kullanım Alanı: ", seçilen_kullanım_alanı)
    print("Potansiyel Etik Sorunlar: ", seçilen_etik_sorun)
    print("Önerilen Çözümler: ", seçilen_çözüm)

    # İnsan kontrolü için seçimi yap
    insan_kontrolü_seçimi = input("Yapay zeka seçimi ile aynı mı? (Evet/Hayır): ")

    if insan_kontrolü_seçimi.lower() == "evet":
        print("İnsan kontrolü seçimi: Yapay zeka ile aynı.")
    else:
        insan_kullanım_alanı = input("Hangi kullanım alanını seçtiniz? (1-6): ")
        insan_index = int(insan_kullanım_alanı) - 1
        print("Yapay Zeka Seçimi: ", seçilen_kullanım_alanı)
        print("İnsan Kontrolü Seçimi: ", kullanım_alanları[insan_index])
        print("Yapay Zeka Sorunlar: ", seçilen_etik_sorun)
        print("İnsan Kontrolü Sorunlar: ", potansiyel_etik_sorunlar[insan_index])
        print("Yapay Zeka Çözüm: ", seçilen_çözüm)
        print("İnsan Kontrolü Çözüm: ", önerilen_çözümler[insan_index])

    devam = input("Devam etmek istiyor musunuz? (Evet/Hayır): ")
    if devam.lower() != "evet":
        break
