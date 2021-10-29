====================
Research Methodology
====================

----------------
General Overview
----------------

Bu projede kullanılan biyoinformatik analizler Şekil 1'de gösterilmiştir. Bu analizler içerisinde, veri toplama ve sınıflandırma ilk aşamada yer almaktadır. Bunu takip eden veri işleme sürecinde ise, verileri analiz için uygun hale getirme ve deduplikasyon işleminin gerçekleştirilmesi, verileri birleştirme, birleştirilen verilerin dizi hizalamala analizlerinin yapılması ve sonuçlarının kontrol edilmesi, hizalanan dizilerin proteom düzeyinde dizi çeşitliliğinin belirlenmesi, dizi çeşitliliği motiflerinin karakterizasyonu ve nicel olarak ölçümü, korunmuşluk içeren ve çeşitlilik gösteren dizi bölgelerinin dağılımının saptanması, potansiyel aşı adayı epitopların belirlenmesi bulunmaktadır.

 .. figure:: ../figures/methodology3.gv.svg
      :alt: Araştırma yöntemi şeması
      :class: with-shadow
      :width: 400px
      :height: 400px

      Şekil 1. Araştırma yöntemine genel bakış

-----------------------------------
Data Collections and Classification
-----------------------------------

İnsan solunum sinsityal virüsü (hRSV) A ve B alt tiplerinin tüm protein dizileri NCBI Virus (https://www.ncbi.nlm.nih.gov/labs/virus/vssi) [ref] ve VIPR (https://www.viprbrc.org) [ref] veritabanlarından 31.03.2021 tarihinde indirilmiştir. İndirilen protein dizileri virüsün 11 proteini (F,G,L,M,M2-1,M2-2,N,NS1,NS2,P,SH) dikkate alınarak sınıflandırılmıştır. Bu araştırmanın virüsün insanda neden olduğu hastalıklara karşı profilaktif aşı çalışmalarına katkı sağlaması hedeflendiği için konak olarak insan seçilmiştir. Her iki veritabanında da protein dizilerinin farklı uzunluklardaki kayıtları bulunmaktadır. Bu durum, dizi hizalamalarında hatalara yol açabileceğinden dolayı her iki alt tipin proteinleri için NCBI veritabanından referans protein dizileri seçilmiştir. Dizi uzunlukları referans değerinde olan ve bu değerden en fazla %10 uzaklıkta olan diziler analiz için seçilmiştir. 

---------------
Data Processing
---------------

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Data Merging, Cleansing and Deduplication
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

NCBI Virus ve VIPR veritabanlarından indirilen veriler tek dosya haline getirilerek birleştirilmiştir. Analizlerde sorun oluşturabilecek protein dizileri kontrol edilmiş ve veri setinden çıkartılmıştır. Her iki veritabınında da bulunan ortak diziler cd-hit[ref] programı kullanılarak tekilleştirilmiştir. Bu işlemde, dizi benzerliği eşik değerini ifade eden ``-c`` parametresi 1 olarak seçilmiştir. Benzerlik değerini hesaplamada kullanılacak olan ve dizi uzunluğunu belirleyen ``-n`` değeri ise varsayılan değer olan 5 olarak seçilmiştir. Bu değer, aynı zamanda programın 0.7-1 eşik değeri aralığı için önerdiği değerdir. Analiz sonuçlarının güvenilir olması ve verilerin sınıflandırılmasının doğruluğundan emin olmak için hata içeren protein dizilerinin üst verileri, NCBI [ref] ve Uniprot[ref] veritabanları kullanılarak kontrol edilmiş ve hatalar düzeltilmiştir. Yapılan bu işlemler, veri setinde oluşabilecek yanlılığın da önüne geçilmesini sağlayarak verileri analize hazır hale getirmiştir.

^^^^^^^^^^^^^^^^^^^^^^^^^^^
Multiple Sequence Alignment
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Çoklu dizi hizalaması herhangi bir biyoinformatik analiz için hayati öneme sahip bir dizi karşılaştırma analizidir. Hâlihazırda birçok dizi hizalaması analizi yapan programlar bulunmakla birlikte, bu programlar hem açık kaynak kodlu olarak hem de ticari versiyon olarak kullanıcılara sunulmaktadır. Analize hazır protein veri seti, açık kaynak kodlu MUSCLE[ref] programı kullanılarak analiz edilmiştir. 


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Multiple Sequence Alignment Check
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Çoklu dizi hizalaması sonuçları, her bir protein veri seti için AliView (Alignment Viewer) programı kullanılarak kontrol edilmiştir. Analiz edilen 11 protein veri seti arasından sadece G proteininde 240'ıncı pozisyondan sonra yer yer boşluklar gözlemlenmiştir. Diğer proteinler için herhangi bir sorunla karşılaşılmamıştır. 

-----------------------------------
Mapping Proteome Sequence Diversity
-----------------------------------

Shannon entropisi [ref], İnsan solunum sinsityal virüsü (hRSV) proteomunun dizi çeşitliliğini belirlemek için kullanılmıştır. Sliding k-mer window yaklaşımı ise hücresel bağışıklık tepkisi oluşturabilecek peptidlerin belirlenmesi için çoklu dizi hizalaması sonuçlarına uygulanmıştır. Bu yaklaşımda ``k`` değeri olarak 9 seçilmiştir. Çünkü, insan lökosit antijenleri (HLAs) ve T hücresi reseptör (TCR) bağlanma bölgeleri çoğunlukla bu uzunluktaki peptidleri (nonamer) tanımaktadır [ref]. Nonamer çeşitliliği, her üst üste gelen pozisyonlar için (1-9,2-10,3-11 vb.) entropi değeri belirlenerek hesaplanmıştır. Entropi değeri olan H(x), dizi hizalaması sonuçlarındaki ilgili pozisyonlar için şu formül kullanılarak hesaplanmıştır.

.. math::

   H(x) = -\sum\limits_{i=1}^{n(x)} p(i,x)\,log_2\,p(i,x)

Bu formülde p(i,x), i nonamer dizisinin x pozisyonunda bulunma olasılığını ifade eder. Entropi değeri H(x), n(x) değeri olan toplam nonamer dizisi arttıkça artış gösterir. Entropi değeri, x pozisyonunda bulunan dizi çeşitliliğini belirtir ve aynı zamanda x pozisyonunda bulunan nonamerlerin birbirleri ile göreceli olasılığına da bağlıdır. İlgili nonamer dizisinin x pozisyonunda dominant olması o pozisyon için entropi değerini azaltıcı etki gösterir. Bu durum, x pozisyonunun nonamer dizileri açısından korunmuşluk gösterdiğini kanıtlar. Entropi değerini etkileyen bir başka faktör ise dizi hizalamasında bulunan proteinlerin sayısıdır. Paninski kuralına göre dizi hizalamasındaki proteinlerin sayısı N olarak ifade edilirse hizalamada oluşabilecek istatistiksel yanlılık N ile ters orantılı olarak değişim göstermektedir [ref]. Her x pozisyonu için entropi değerinde N sayısını ele alarak istatistiksel olarak düzenleme yapılması analiz sonuçlarının doğruluğu açısından büyük önem arz etmektedir. Anlatılan tüm bu aşamaların analizi, DiMA (Diversity Motif Analyzer) [ref] programı kullanılarak gerçekleştirilmiştir.


-------------------------------------------------------
Quantification and Characterization of Diversity Motifs
-------------------------------------------------------

Entropi değeri protein dizi çeşitliliği hakkında genel olarak bilgi sahibi olmamızı sağlar. Bu çeşitliliğin nicel ölçümü ve karakterizasyonu için dizi çeşitliliği motiflerini incelemek gereklidir. Motiflerin karakterizasyonu çoklu dizi hizalamasındaki her bir nonamer pozisyonu için o pozisyonda bulunan farklı nonamer dizilerinin nicel ölçümü yapılarak gerçekleştirilmiştir [ref]. En çok tekrar eden nonamer dizisi "index" olarak adlandırılmıştır. Bunun dışında kalan nonamerler ise "varyantlar" olarak isimlendirilmiştir ve index nonamer dizisinden en az 1 amino asiti farklıdır. Varyantların içinde en sık bulununan nonamer dizisi "major", major motifinden daha az sıklıkta olan ve birden fazla bulunan nonamer dizisi ise "minor" olarak tanımlanmıştır. Tek olarak bulunan çeşitlilik motifine ise "özgün" denilmiştir. Bu motiflere ek olarak "nonatipler" tüm motiflerin (index,major,minor,özgün) nonamerleri toplamının dizi hizalamasındaki tüm dizilerin toplamına bölünmesi sonucu hesaplanmış ve proteom düzeyinde dizi dinamiklerini açığa çıkarmıştır.   

.. figure:: 
      :alt: Dizi çeşitliliği motifleri
      :class: with-shadow
      :width: 400px
      :height: 400px

      Şekil 1. Dizi çeşitliliği motifleri

------------------------------------------------------------------------------------------------
Distribution of conserved and variable sequences and Identification of Candidate Vaccine Targets
------------------------------------------------------------------------------------------------

Korunmuşluk içeren ve çeşitlilik gösteren peptidleri incelemek için index motifi kendi arasında 5 kategoriye ayrılmıştır:

1. Çok yüksek derecede çeşitliliğe sahip (index değeri %10'dan küçük)
2. Yüksek derecede çeşitliliğe sahip (index değeri %20'den küçük, %10'dan büyük ve eşit)
3. Karışık değişkenleri içeren (index değeri %90'dan küçük, %20'den büyük ve eşit)
4. Yüksek derecede korunmuşluğa sahip (index değeri %100'den küçük, %90'dan büyük ve eşit)
5. Tamamen korunmuş (index değeri %100'e eşit)

Yüksek derecede korunmuşluğa sahip ve tamamen korunmuş olan nonamer dizileri çok düşük entropi değerlerine sahip olmakla birlikte evrimsel açıdan da dirençlilik gösterirler. Bu yüzden aşı adayı olabilecek epitoplar bu kategorilere ait dizilerden seçilmiştir ve amino asit dizileri üst üste gelen nonamerler birbirleri ile birleştirilmiştir. Birleştirilen nonamerlerin immünojenitesi IEDB (Immune Epitope Database) [ref] veritabanı kullanılarak araştırılmıştır. Virüse ait deneysel olarak ispatlanan ve rapor edilen epitoplar da IEDB veritabanı kullanılarak belirlenmiştir.

------------------
Epitope Prediction
------------------

CD8+ T hücresi (CTL) epitopları, MHC-I bağlanma kapasitelerini hesaplayan IEDB'nin web tabanlı tahmin programı ile (http://tools.iedb.org/mhci/) ortaya çıkarılmıştır. Yüksek derecede korunmuşluğa sahip ve tamamen korunmuş olan nonamer dizileri program için giriş verisi olarak kullanılmış ve tahmin metodu olarak veritabanının önerdiği NetMHCPan 4.1 EL [ref] algoritması kullanılmıştır. Epitopların, HLA (İnsan Lökosit Antijeni) bağlanma kapasitelerini ölçmek için 12 süpertipten (A1,A2,A3,A24,A26,B7,B8,B27,B39,B44,B58,B62) toplam 95 alel seçilmiştir. Eşik değeri olarak %1'den küçük skora sahip [ref] (iyi bağlanma kapasitesi gösteren) olan epitoplar ve onlara karşılık gelen HLA alelleri ileri analizler için seçilmiştir. Aynı zamanda, CD4+ T hücresi (HTL) epitopları da, MHC-II bağlanma kapasitelerini hesaplayan IEDB'nin web tabanlı tahmin programı ile (http://tools.iedb.org/mhcii/) analiz edilmiştir. MHC-I'den farklı olarak MHC-II giriş verileri için 15 amino asit uzunluğundaki dizilerin kullanılması gerekmektedir. Bu uzunluktaki diziler birleştirilen nonamer dizilerinden üretilmiştir. Tahmin metodu olarak veritabanının önerdiği IEDB recommended seçeneği kullanılmıştır. Bu metodun içeriğinde farklı aleller için olmak üzere Consensus, NN-align, SMM-align, CombLib ve Sturniolo olarak adlandırılan 5 farklı algoritma bulunmaktadır. Eğer bağlanma kapasitesi ölçülmek istenen HLA aleli bu algoritmalardan biri ile tahmin edilemiyorsa NetMHCIIpan algoritması ile veriler analiz edilmektedir. Analiz sonuçları algoritmaların ortak skorları kullanılarak üretilmiştir. MHC-II sınıfındaki epitopların tahmini için 3 süpertipe (DP,DQ,DR) ait toplam 45 alel seçilmiştir. Eşik değeri ise %10 olarak belirlenmiştir [ref]. Tahmin edilen epitoplar ve onlara karşılık gelen aleller ileri analizler için seçilmiştir.
