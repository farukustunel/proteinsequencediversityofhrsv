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

İnsan solunum sinsityal virüsü (hRSV) A ve B alt tiplerinin tüm protein dizileri NCBI Virus [1] (https://www.ncbi.nlm.nih.gov/labs/virus/vssi) ve VIPR [1] (https://www.viprbrc.org) veritabanlarından 31.03.2021 tarihinde indirilmiştir. İndirilen protein dizileri virüsün 11 proteini (F,G,L,M,M2-1,M2-2,N,NS1,NS2,P,SH) dikkate alınarak sınıflandırılmıştır. Bu araştırmanın virüsün insanda neden olduğu hastalıklara karşı profilaktif aşı çalışmalarına katkı sağlaması hedeflendiği için konak olarak insan seçilmiştir.

---------------
Data Processing
---------------

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Data Merging, Cleansing and Deduplication
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

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