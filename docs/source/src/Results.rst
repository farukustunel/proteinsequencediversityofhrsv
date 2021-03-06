=======
Results
=======

----
Data
----

NCBI Virus ve VIPR veritabanlarından indirilen insan solunum sinsityal virüsü protein dizilerine ait birleştirilen ve tekilleştirilen veri seti, virüsün 11 proteini için toplam 13770 kayıttan oluşmaktadır. Bu sayı, veri setinin protein dizilerine göre sınıflandırılması ve tekrar tekilleştirilmesi işleminden sonra 5766'ya düşmüştür. Virüsün her iki alt tipinin de benzer uzunlukluktaki protein dizilerine sahip olduğu görülmektedir (Şekil 1). Ayrıca, proteinlerin kendi içindeki dizi çeşitliliği de en düşük benzerlik oranına bakılarak incelenebilir. Virüsün en fazla çeşitliliğe sahip proteini en düşük benzerlik oranı %35.39 olan G proteini iken en fazla korunmuş bölge içeren proteini ise %75.54 ile L proteini olarak bulunmuştur.


.. figure:: ../figures/data_table.svg
      :alt: İnsan solunum sinsityal virüsünün analiz edilen verileri ile ilgili bilgiler
      
      İnsan solunum sinsityal virüsünün analiz edilen verileri ile ilgili bilgiler


NCBI Virus veritabanından indirilen veri seti incelendiğinde protein dizilerinin dağılımının 1956 ve 2019 yılları arasında olduğu görülmektedir. En fazla protein dizisi eklenen yıl ise 2013'tür ve eklenen protein dizisi kaydı 7328'dir (Şekil 1).


.. figure:: ../figures/ncbi_virus_years.png
      :alt: NCBI Virus veritabanından indirilen veri setindeki protein dizilerinin yıllara göre dağılımı 
      
      NCBI Virus veritabanından indirilen veri setindeki protein dizilerinin yıllara göre dağılımı

NCBI Virus veritabanından indirilen veri setindeki protein dizileri Asya, Afrika, Avrupa, Kuzey Amerika, Güney Amerika ve Okyanusya olmak üzere 6 farklı kıtada ve 71 farklı ülkede coğrafi dağılım göstermektedir (Şekil 1). Veri setindeki en büyük yüzdeye sahip olan ülke %23 ile Amerika'dır.


.. figure:: ../figures/geo_ncbi_virus.png
      :alt: NCBI Virus veritabanından indirilen veri setindeki protein dizilerinin coğrafi dağılımı
      
      NCBI Virus veritabanından indirilen veri setindeki protein dizilerinin coğrafi dağılımı


VIPR veritabanından indirilen veri seti incelendiğinde protein dizilerinin dağılımının 1956 ve 2019 yılları arasında olduğu görülmektedir. En fazla protein dizisi eklenen yıl ise 2013'tür ve eklenen protein dizisi kaydı 7102'dir (Şekil 1). Bu sayının, NCBI Virus veritabanından indirilen veri setinde farklı olması veritabanlarında bulunan protein dizileri arasında farklılık olduğuna işaret etmektedir. Çalışmanın geniş kapsamlı olması açısından farklı veritabanlarının kullanılmasının önemini de ortaya koymaktadır.

.. figure:: ../figures/vipr_years.png
      :alt: VIPR veritabanından indirilen veri setindeki protein dizilerinin yıllara göre dağılımı
      
      VIPR veritabanından indirilen veri setindeki protein dizilerinin yıllara göre dağılımı


VIPR veritabanından indirilen veri setindeki protein dizileri NCBI Virus veritabanı ile aynı olarak Asya, Afrika, Avrupa, Kuzey Amerika, Güney Amerika ve Okyanusya olmak üzere 6 farklı kıtada ve 71 farklı ülkede coğrafi dağılım göstermektedir (Şekil 1). Veri setindeki en büyük yüzdeye sahip olan ülke %26 ile Amerika'dır. Diğer ülkelerde NCBI Virus veritabanındaki protein dizileri ile benzer yüzdelere sahiptir.

.. figure:: ../figures/geo_vipr.png
      :alt: VIPR veritabanından indirilen veri setindeki protein dizilerinin coğrafi dağılımı
      
      VIPR veritabanından indirlen veri setindeki protein dizilerinin coğrafi dağılımı

---------------------------
Proteome Sequence Diversity
---------------------------

hRSV proteome dizi çeşitliliği Shannon entropisi kullanılarak ölçülmüştür. Proteome düzeyinde entropi değeri ortalama 0.79 olarak bulunmuştur ve entropi değeri dağılımı 0 ile 4.19 arasında değişim göstermiştir. Buna bağlı olarak, proteome düzeyinde korunmuşluk yüzdesi yüksek olarak ifade edilebilir. Proteome düzeyindeki total varyantların ortalama değeri ise %22.66'dır ve varyantların değer dağılımı %0 ile %79.33 arasında bulunmuştur. 4 proteinin (L,M,N,P) ortalama entropi değeri olan 0.79'dan düşük değere sahip olduğu gözlemlenmiştir (Tablo 1). 

.. figure:: ../figures/entropy_stats_table-cropped.svg
      :alt: hRSV proteomunun entropy değerleri ve total varyantlarının istatistiksel analizini içeren tablo
      
      hRSV proteomunun entropy değerleri ve total varyantlarının istatistiksel analizini içeren tablo


Entropi değeri 1'e eşit ve küçük olan tam 2480 pozisyon hRSV proteomunda bulunmuştur. 1612 pozisyonun entropi değeri 2'ye eşit ve küçük olmakla birlikte 1'den de büyük olarak gözlemlenmiştir. Bunun yanı sıra, entropi değeri 3'e eşit ve küçük olan 2'den de büyük olan 269 pozisyon vardır. 82 pozisyonun entropi değeri 3'den büyük, 4'e eşit ve küçüktür. Sadece 6 pozisyonun entropi değeri 4'den büyük, 5'e eşit ve küçük olarak bulunmuştur. Toplamda analiz edilen 4449 pozisyonun %55.7'sinin (entropi değeri 1'e eşit ve küçük olan pozisyonlar) yüksek korunmuşluğa sahip olduğu saptanmıştır. Proteome düzeyinde maksimum entropi değeri olan 4.19 ise M2-2 proteininde bulunmaktadır ve 43-51 pozisyonları arasındaki nonamer dizisine aittir. Total varyantların maksimum değeri olan %79.33 ise G proteininde 312-320 pozisyonları arasındaki nonamerde bulunmuştur. Bu zamana kadar yapılan çalışmalarda en yüksek entropi değerine sahip (en fazla çeşitlilik gösteren) nonamer HIV-1 B kolunda Env proteinine aittir ve değeri 9.2'dir. Aynı şekilde, en yüksek total varyantlar da HIV-1 virüsün Env proteinine ait olup değeri %98'dir. Özellikle entropi değerinde yaklaşık 2 kattan fazla bir boşluk olduğu hRSV ve HIV-1 arasında görülmektedir (Şekil 1). Bu durum, hRSV proteomunun genel olarak korunmuş bölgelerden oluştuğunu göstermektedir ve uygun aşı adayı epitoplar keşfetmenin hRSV için mümkün olduğunu ortaya koymaktadır.


.. figure:: ../figures/entropyvstotalstemplot.png
      :alt: hRSV proteinlerinin her pozisyonu için entropy değerlerini ve total varyantlarını gösteren grafik  
      
      hRSV proteinlerinin her pozisyonu için entropy değerlerini ve total varyantlarını gösteren grafik



hRSV proteomunda entropi ve total varyantlar arasında ilişki incelendiğinde iki değer arasında güçlü pozitif korelasyon olduğu görülmektedir (Pearson korelasyon katsayı r = 0.89). Tüm nonamer pozisyonları ele alındığında total varyantlar için entropi değeri 1, toplam nonamerlerin yaklaşık %55'inde görülmüştür. Entropi değeri 2,3,4 ve 4.19 (maksimum entropi değeri) sırasıyla tüm nonamerlerin yaklaşık %36, %6, %1.8 ve ‰1'inde saptanmıştır. Grafik dikkatli incelendiğinde entropi değeri 1-3 aralığı ile total varyantların %20-%40 değer aralığında boşluklar gözlemlenmektedir (Şekil 1). Bu durum, diğer virüsler ile kıyaslama yapıldığında olağan dışı olarak karşımıza çıkmaktadır ve ilgili bölgenin daha detaylı araştırılmasının gerekliliğini ortaya koymaktadır.


.. figure:: ../figures/entropyvsincidence_all.png
      :alt: hRSV proteomunun entropy değerleri ve total varyantları arasındaki ilişkiyi gösteren grafik
      
      hRSV proteomunun entropy değerleri ve total varyantları arasındaki ilişkiyi gösteren grafik



---------------------------
Dynamics of Diversity Motif
---------------------------

hRSV proteomunun motif çeşitliliği dinamiklerini daha iyi anlamak için 4449 üst üste gelen nonamer dizisinin nicel analizi yapılmıştır (Appendix 1). M2-2 proteininin örnek olarak seçilmiş nonamerleri için motif çeşitliliği dinamikleri Tablo 1'de incelenebilir. Tablo 1'deki veri setinin M2-2 proteini için başlangıç pozisyonu çoklu dizi hizalaması dikkate alındığında 1-13 arasında olan toplam 13 farklı nonamerden oluştuğu gözlemlenebilir. 13 farklı nonamerin temsil ettiği toplam nonamer sayısı ise 2319'dur. Bu nonamerler arasında korunmuşluk derecesi tamamen korunmuş olan bir tek nonamer bulunmuştur. 7-15 pozisyonları arasında olan nonamerin entropi değeri 0 ve index değeri %100 olarak görülmektedir. Diğer nonamerler ise çok yüksek korunmuşluğa sahip ve karışık değişkenleri içeren korunmuşluk seviyelerine sahiptir. Çok yüksek korunmuşluğa sahip olan nonamerler arasında en yüksek index değeri %99.6'dır ve nonamer pozisyonları 8-16 ve 9-17'dir. Entropi değerleri de sırasıyla 0.04 ve 0.03'tür. Karışık değişkenleri içeren korunmuşluk seviyesine sahip olan nonamerler arasında en yüksek index değeri ise %81.4'tür. Bu nonamerlerin pozisyonları 1-9 ve 2-10'dur. Entropi değerleri sırasıyla 1.08 ve 1.07'dir. Her iki pozisyonun da toplam 105 nonamer dizisi içerdiği tespit edilmiştir. Total varyantların değeri bu pozisyonlar için %18.6, major varyantlar için %10.85, minor varyantlar ve özgün varyantlar için ise %3.88'dir. Nonatip olarak adlandırılan ve ilgili bölgedeki farklı nonamer sayısının o bölgedeki tüm nonamer sayısına bölümü sonucu hesaplanan değer ise %6.2'dir. Tablo genelinde gösterilen nonamer pozisyonlarının hiçbirinde düşük destek (ilgili pozisyon için nonamer sayısının 30'dan az olması durumu) görülmemiştir.  

.. figure:: ../figures/m2_2_sample_table-cropped.svg
      :alt: hRSV M2-2 proteininin nicel çeşitlilik analizine ait örnek tablo
      
      hRSV M2-2 proteininin nicel çeşitlilik analizine ait örnek tablo


Her bir çeşitlilik motifinin total varyantlar ile olan ilişkisi Şekil 1'de proteom düzeyinde incelenmiştir. Total varyantların artış gösterdiği durumlarda tüm motif çeşitlerinin özgün bir desene sahip olduğu görülmektedir (Şekil 1 A.). Total varyantların artış gösterdiği durumda major varyantların değerinin piramit deseni oluşturduğu gözlemlenmiştir. Major varyantların değerleri 0 ile %49.21 arasında değişim göstermektedir. Grafik içerisinde görülen ve index değerinin genelinden farklı konumlarda bulunan noktalar ise farklı proteinlerin aynı pozisyonu içinde görülen birden fazla index nonamerini temsil etmektedir. SH proteininde 35-43 ve 50-58 pozisyonları arasındaki nonamerler ile NS2 proteininde 39-47 ve 40-48 pozisyonları arasındaki nonamerler için birden fazla index bulunmuştur. Minor ve özgün varyantlar ise proteom boyunca hemen hemen her pozisyonda görülebilmektedir. Minor varyantların maksimum değeri yaklaşık olarak %58'dir ve bu değere karşılık gelen total varyantların değerinin ise %60'a yakın olduğu görülebilir. Özgün varyantların ise daha dengeli bir dağılım gösterdiği tespit edilmiştir ve maksimum değeri yaklaşık %21 olarak bulunmuştur. Nonatipler de özgün varyantlar gibi proteom düzeyinde dengeli bir dağılım göstermiştir ve görülen maksimum değer yaklaşık %31 olarak tespit edilmiştir. Ayrıca korunmuşluk içeren nonamer dizi değerlerindeki azalmanın %18'e kadar düştüğü ve buna karşılık total varyantların değerinin %80'e kadar çıktığı görülmektedir. Bu iki değer arasında teorik olarak beklenildiği gibi ters orantı gözlemlenmiştir. Tüm çeşitlilik motiflerinin frekans dağılımları keman grafiği kullanılarak analiz edilmiştir (Şekil 1 B.). İndex nonamerler, major varyantlar, minor varyantlar, özgün varyantlar ve nonatiplerin proteome boyunca görülen ortalama değerleri sırasıyla %77.3, %17.6, %3.7, %1.2 ve %2 olarak ölçülmüştür. İndex nonamerlerin değerleri %50-60 ve %90-%100 arasında yoğunluk göstermektedir. Major varyantların yoğunluğu ise yaklaşık olarak %20-%30 ve %50-%60 değerleri arasında fazlalık göstermektedir. Diğer çeşitlilik motifleri için yoğunluklar yaklaşık olarak %20-%25 arasında değişiklik göstermektedir.


.. figure:: ../figures/proteomemotif.png
      :alt: hRSV dizi çeşitliliği motiflerinin proteom düzeyinde dinamiklerini gösteren grafik
      
      hRSV dizi çeşitliliği motiflerinin proteom düzeyinde dinamiklerini gösteren grafik


hRSV dizi çeşitliliği motiflerinin protein düzeyindeki dinamikleri, proteom düzeyindeki dinamikleri ile benzerlik göstermektedir (Şekil 1). G ve M2-1 proteinleri hariç diğer proteinlerin tüm motifleri %20-%40 değer aralığında veri noktalarına sahip değildir. Total varyantlar ise tüm proteinlerde %80 değerinin altında bulunmaktadır.


.. figure:: ../figures/motifvstotal4all.png
      :alt: hRSV dizi çeşitliliği motiflerinin protein düzeyinde dinamiklerini gösteren grafik
      
      hRSV dizi çeşitliliği motiflerinin protein düzeyinde dinamiklerini gösteren grafik

hRSV dizi çeşitliliği motiflerinin protein düzeyindeki sıklık dağılımları şekil 1'de keman grafikleri kullanılarak analiz edilmiştir. İndex motifleri incelendiğinde hiçbir protein için %20'inin altında değere rastlanmamıştır. G, M2-2 ve SH proteinleri dışındaki proteinlerin index değerleri %40-%60 ve %80-%100 aralıklarında yoğunluk göstermektedir. Major varyantlar ise tüm proteinlerde %50 değerinin altında veri noktalarına sahiptir. Bu durum minor varyantlar incelendiğinde yaklaşık %59 olarak tespit edilmiştir. Özgün varyantlar ve nonatipler için ise sırasıyla yaklaşık olarak %22 ve %32 değerlerinin üstünde veri noktaları görülmemiştir. 

.. figure:: ../figures/freqdistviolin.png
      :alt: hRSV dizi çeşitliliği motiflerinin dağılımını inceleyen violin grafiği 
      
      hRSV dizi çeşitliliği motiflerinin dağılımını inceleyen violin (keman) grafiği 

------------------------------------------------
Distribution of Conserved and Variable Sequences
------------------------------------------------

hRSV proteomunda hemen hemen tüm nonamer dizi pozisyonları karışık değişkenleri içeren ve yüksek derecede korunmuşluğa sahip olarak sınıflandırılmıştır (Şekil 1). Protome düzeyinde inceleme yapıldığında karışık değişkenleri içeren nonamer dizileri yaklaşık %49 (2180 nonamer dizisi), yüksek derecede korunmuşluk içeren nonamer dizileri yaklaşık %47 (2092 nonamer dizisi), tamamen korunmuş nonamer dizileri ise yaklaşık %4 (177 nonamer dizisi) olarak bulunmuştur. Sadece L, N, M, M2-1 ve M2-2 proteinleri tamamen korunmuş (index değeri %100'e eşit) olan nonamer dizilerini içermektedir. Çok yüksek derecede çeşitliliğe sahip (index değeri %10'dan küçük) ve yüksek derecede çeşitliliğe sahip (index değeri %20'den küçük, %10'dan büyük ve eşit) nonamer dizilerine ise hiçbir proteinde rastlanmamıştır.

.. figure:: ../figures/rating1.png
      :alt: Protein ve proteome düzeyinde hRSV nonamerlerinin korunmuşluk derecelerini gösteren grafik 
      
      Protein ve proteome düzeyinde hRSV nonamerlerinin korunmuşluk derecelerini gösteren grafik  



----------------------------------------------------
Highly Conserved, Immunogenic Sequences as Potential Vaccine Targets
----------------------------------------------------