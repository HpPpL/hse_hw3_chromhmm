# hse_hw3_chromhmm

## Google Colab
[Ссылка](https://colab.research.google.com/drive/182ygIZzfH4UguZL7h_oeDTN-VZyt2rZS?usp=sharing)

## Гистоновые Метки
File | Name 
--- | ---
wgEncodeBroadHistoneK562H2azStdAlnRep1.bam | H2az.bam
wgEncodeBroadHistoneK562H3k27acStdAlnRep1.bam | H3k27ac.bam
wgEncodeBroadHistoneK562H3k27me3StdAlnRep1.bam | H3k27me3.bam
wgEncodeBroadHistoneK562H3k36me3StdAlnRep1.bam | H3k36me3.bam
wgEncodeBroadHistoneK562H3k4me1StdAlnRep1.bam | H3k4me1.bam
wgEncodeBroadHistoneK562H3k4me2StdAlnRep1.bam | H3k4me2.bam
wgEncodeBroadHistoneK562H3k4me3StdAlnRep1.bam | H3k4me3.bam
wgEncodeBroadHistoneK562H3k79me2StdAlnRep1.bam | H3k79me2.bam
wgEncodeBroadHistoneK562H3k9acStdAlnRep1.bam | H3k9ac.bam
wgEncodeBroadHistoneK562H3k9me1StdAlnRep1.bam | H3k9me1.bam


## cellmarkfiletable.txt

Клеточная линия | Гистоновая метка | Файл с гистоновой меткой | Файл с контролем
--- | --- | --- | ---
K562 | H3k4me1 | H3k4me1.bam | Control.bam
K562 | H3k9me1 | H3k9me1.bam | Control.bam
K562 | H3k27ac | H3k27ac.bam | Control.bam
K562 | H3k36me3 | H3k36me3.bam | Control.bam
K562 | H3k4me3 | H3k4me3.bam | Control.bam
K562 | H3k79me2 | H3k79me2.bam | Control.bam
K562 | H3k4me2 | H3k4me2.bam | Control.bam
K562 | H2az | H2az.bam | Control.bam
K562 | H3k27me3 | H3k27me3.bam | Control.bam
K562 | H3k9ac | H3k9ac.bam | Control.bam


## ChromHMM

Emission | Overlap | Transition 
 --- | --- | ---
![Image](/data/emissions_10.png) | ![Image](/data/K562_10_overlap.png) | ![Image](/data/transitions_10.png)

RefSeqTSS | RefSeqTES 
 --- | --- 
![Image](/data/K562_10_RefSeqTSS_neighborhood.png) | ![Image](/data/K562_10_RefSeqTES_neighborhood.png)

## Эпигенетические типы
Поскольку табличка у меня получилась просто огромная, то на фото было трудно все поместить, поэтому под нож пошли UCSC гены и CPG островки.. Экзоны и интроны видно на части фото..
№ | Название | Описание | Картинка
 --- | --- | ---| ---
1 | Polycomb-repressed | <ul><li> Выражен в H2az, H3k4me1, H3k27me3. Менее явно выражен в H3k4me2, H3k4me3, H3k9ac. </li> <li>Чаще всего находятся на ядерной ламине. </li> <li> Попадает на экзон. </li> | ![Image](/data/1_Repressed.png)
2 | Heterochromatin | <ul><li> Выражен в H3k9me1, H3k27me3. Менее явно выражен в H2az. </li><li> Не попадает на ген </li> <li>Чаще всего находятся на ядерной ламине. </li> | ![Image](/data/2_Heterochrom-lo.png)
3 | Weak transcribed | <ul><li> Выражен в H3k4me1, H3k79me2. Менее явно выражен в H3k9me1. </li> <li> Проявляется на RefSeqTES </li> | ![Image](/data/3_Weak_Txn.png)
4 | Transcriptional transition | <ul><li> Выражен в H3k4me1 </li> | ![Image](/data/4_Txn_Transition.png)
5 | Insulator | <ul><li> Выражен в H2az, H3k4me1 </li> <li> Не попадает на ген. </li> <li> Слабо проявляется на RefSeqTES </li>  | ![Image](/data/5_Insulator.png) 
6 | Weak/poised enhancer | <ul><li> Выражен в H2az, H3k4me1. Менее явно выражен в H3k4me2, H3k9ac. </li> <li> Слабо проявляется на RefSeqTES </li>  <li> Попадает на экзон или интрон. </li> | ![Image](/data/6_Weak_Enhancer.png)
7 | Strong enhancer | <ul><li> Выражен в H2az, H3k4me1, H3k4me2, H3k4me3, H3k9ac, H3k9me1, H3k27ac </li>   <li> Попадает на экзон. </li> | ![Image](/data/7_Strong_Enhancer.png)
8 | Inactive/poised Promoter | <ul><li> Выражен в H2az, H3k4me1, H3k4me2, H3k4me3. Менее явно выражен в H3k9ac, H3k27me3 </li> <li> Чаще всего находятся на ядерной ламине. </li> <li> Проявляется на CPG островках. </li> | ![Image](/data/8_Poised_Promoter.png)
9 | Weak Promoter | <ul><li> Выражен в H2az, H3k4me1, H3k4me2, H3k4me3, H3k9ac.  </li> <li> Попадает на экзон. </li> <li> Проявляется на RefSeqTES </li> <li> Проявляется на RefSeqTSS </li>   | ![Image](/data/9_Weak_Promoter.png) 
10 | Active Promoter | <ul><li> Выражен в H2az, H3k4me1, H3k4me2, H3k4me3, H3k9ac, H3k27ac,  H3k79me2.  </li> <li> Проявляется на RefSeqTES </li> <li> Слабо проявляется на RefSeqTSS </li>  <li> Проявляется на CPG островках. </li> | ![Image](/data/10_Active_Promoter.png)

 ## Бонус
[Ссылка на архив](https://drive.google.com/file/d/1l-vFv_RZUnJj7H9aT5EK6HqfjxD8WZnt/view?usp=sharing) - архив, так как в несжатом виде файл большой
