# MTPEdocs-MQM

## Introduction

To encourage studies on machine translation quality estimation (MTQE) for Japanese-to-English translation direction, we manually annotated erroneous spans in the MT outputs of [MTPEdocs](https://github.com/tntc-project/MTPEdocs).

* [MT-MQM](MT-MQM): Span-based issue annotations based on MQM-like manual quality assessment of MT
    * Outputs of two MT systems in MTPEdocs have so far been covered.
        * JaEn_01_TexTra
        * JaEn_02_Google
    * Another set of workers from PE were asked to annotate problematic spans within MT output and label each span with issue type and severity.
        * [The issue typology](fujita-issue-typology-en.pdf) is configured slightly from Table 2 in Freitag et al. (2021) with a prioritization of Terminology issues as in Fujita et al. (2017).
        * All the identified issues were annotated (cf. five most severe issues were selected in Freitag et al. (2021)).
        * Neither PE (in [MTPEdocs](https://github.com/tntc-project/MTPEdocs)) nor human translation (in [Translation Resources of Nagoya City](https://github.com/tr4lg/nagoya-dataset/)) was referred to.
    * Segment-level MQM scores were computed based on the annotated issues as Table 4 in Freitag et al. (2021).
        * "Critical" issues were weighted equivalently to "Major" issues.
        * Due to the unlimited number of issues being involved, the score is sometimes very large.

## References

* Markus Freitag, George Foster, David Grangier, Viresh Ratnakar, Qijun Tan, and Wolfgang Macherey. [Experts, Errors, and Context: A Large-Scale Study of Human Evaluation for Machine Translation](https://aclanthology.org/2021.tacl-1.87/). Transactions of the Association for Computational Linguistics (TACL), 9:1460–1474, 2021.
* Atsushi Fujita, Kikuko Tanabe, Chiho Toyoshima, Mayuka Yamamoto, Kyo Kageura, and Anthony Hartley. [Consistent Classification of Translation Revisions: A Case Study of English-Japanese Student Translations](https://aclanthology.org/W17-0807/). In Proceedings of the 11th Linguistic Annotation Workshop (LAW), pages 57–66, 2017.

## Developer

The dataset in this directory is credited to National Institute of Information and Communications Technology (henceforth, NICT).  NICT has made the dataset publicly available under the conditions of license specified below.

## License

![Creative Commons License](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)

* Use and/or redistribution of this dataset, except for the source documents, is permitted under the conditions of [Creative Commons Attribution-NonCommercial-ShareAlike License 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

## Precautions

* NICT bears no responsibility for the contents of the dataset and assumes no liability for any direct or indirect damage or loss whatsoever that may be incurred as a result of using the dataset.
* If any copyright infringement or other problems are found in the dataset, please contact us at atsushi.fujita[at]nict[dot]go[dot]jp. We will review the issue and undertake appropriate measures as necessary.

## Acknowledgments

We are grateful to Rei Miyata for his helpful advice on the MQM-like annotation instruction and the issue typology.
This dataset has been developed partly supported by JSPS KAKENHI Grant-in-Aid for Scientific Research (B) [23K28378, Developing Shared Translation Resources for Local Governments to Facilitate Multilingual Information Dissemination](https://kaken.nii.ac.jp/en/grant/KAKENHI-PROJECT-23K28378/), as a part of work at [Advanced Translation Technology Laboratory](https://att-astrec.nict.go.jp/), [Advanced Speech Translation Research and Development Promotion Center](https://astrec.nict.go.jp/), [National Institute of Information and Communications Technology](https://www.nict.go.jp/en/).
