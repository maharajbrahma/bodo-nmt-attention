# Word-Level English-Bodo Neural Machine Translation

*Work-done by: Sanjib Narzary, Maharaj Brahma, Bobita Singha, Rangjali Brahma, Bonali Dibragede, Sunita Barman*

- [Introduction] (#introduction)

# Introduction
English-Bodo Neural Machine Translation despite having potential no prior research has been done. According to [2011 Census of India](http://www.censusindia.gov.in/2011Census/Language-2011/Statement-1.pdf), Bodo has 14,57,547 native speakers and a total of 14,82,929 total speakers. During the initial stage of this work we searched for English-Bodo parallel corpus, to our surprise we found only one resource - [Indian Language Technology Proliferation and Deployment Centre](https://tdil-dc.in/index.php?lang=en). 


# Dataset
*Tourism corpus*: English-Bodo parallel corpus of Tourism domain (20901 sentences) provided by the [TDIL-DC](https://tdil-dc.in)
*The detailed steps of cleaning and preprocessing is present in paper*

# Training
* The hyper-parameters could be changed in the **start.sh** file.

``` shell
bash start.sh
```
or 
```shell
./start.sh
```

The trained models are saved in the models/ directory.
