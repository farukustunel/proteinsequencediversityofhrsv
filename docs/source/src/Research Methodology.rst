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

İnsan solunum sinsityal virüsü (hRSV) A ve B alt tiplerinin tüm protein dizileri NCBI Virus [ref] (https://www.ncbi.nlm.nih.gov/labs/virus/vssi) ve VIPR [ref] (https://www.viprbrc.org) veritabanlarından 31.03.2021 tarihinde indirilmiştir. İndirilen protein dizileri virüsün 11 proteini (F,G,L,M,M2-1,M2-2,N,NS1,NS2,P,SH) dikkate alınarak sınıflandırılmıştır. Bu araştırmanın virüsün insanda neden olduğu hastalıklara karşı profilaktif aşı çalışmalarına katkı sağlaması hedeflendiği için konak olarak insan seçilmiştir. Her iki veritabanında da protein dizilerinin farklı uzunluklardaki kayıtları bulunmaktadır. Bu durum, dizi hizalamalarında hatalara yol açabileceğinden dolayı her iki alt tipin proteinleri için NCBI veritabanından referans protein dizileri seçilmiştir. Dizi uzunlukları referans değerinde olan ve bu değerden en fazla %10 uzaklıkta olan diziler analiz için seçilmiştir. 

---------------
Data Processing
---------------

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Data Merging, Cleansing and Deduplication
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

NCBI Virus ve VIPR veritabanlarından indirilen veriler tek dosya haline getirilerek birleştirilmiştir. Analizlerde sorun oluşturabilecek protein dizileri kontrol edilmiş ve veri setinden çıkartılmıştır. Her iki veritabınında da bulunan ortak diziler cd-hit[ref] programı kullanılarak tekilleştirilmiştir. Bu işlemde, dizi benzerliği eşik değerini ifade eden ``-c`` parametresi 1 olarak seçilmiştir. Benzerlik değerini hesaplamada kullanılacak olan ve dizi uzunluğunu belirleyen ``-n`` değeri ise varsayılan değer olan 5 olarak seçilmiştir. Bu değer, aynı zamanda programın 0.7-1 eşik değeri aralığı için önerdiği değerdir. Analiz sonuçlarının güvenilir olması ve verilerin sınıflandırılmasının doğruluğundan emin olmak için hata içeren protein dizilerinin üst verileri, NCBI ve Uniprot[ref] veritabanları kullanılarak kontrol edilmiş ve hatalar düzeltilmiştir. Yapılan bu işlemler, veri setinde oluşabilecek yanlılığın da önüne geçilmesini sağlayarak verileri analize hazır hale getirmiştir.

^^^^^^^^^^^^^^^^^^^^^^^^^^^
Multiple Sequence Alignment
^^^^^^^^^^^^^^^^^^^^^^^^^^^



^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Multiple Sequence Alignment Check
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

-----------------------------------
Mapping Proteome Sequence Diversity
-----------------------------------

-------------------------------------------------------
Quantification and Characterization of Diversity Motifs
-------------------------------------------------------

------------------------------------------------
Distribution of conserved and variable sequences
------------------------------------------------

-------------------------------------------  
Identification of Candidate Vaccine Targets
-------------------------------------------