# Word-Level English-Bodo Neural Machine Translation

*Work done by: Sanjib Narzary, Maharaj Brahma, Bobita Singha, Rangjali Brahma, Bonali Dibragede, Sunita Barman*

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Training](#training)
- [Testing](#testing)
- [Translating](#translating)

## Introduction
English-Bodo (Eng-Brx) Neural Machine Translation despite having potential no prior research has been done. According to [2011 Census of India](http://www.censusindia.gov.in/2011Census/Language-2011/Statement-1.pdf), Bodo has 14,57,547 native speakers and a total of 14,82,929 total speakers. During the initial stage of this work we searched for English-Bodo parallel corpus, to our surprise we found only one resource - [Indian Language Technology Proliferation and Deployment Centre](https://tdil-dc.in/index.php?lang=en). 


## Dataset
*Tourism corpus*: English-Bodo parallel corpus of Tourism domain (20901 sentences) provided by the [TDIL-DC](https://tdil-dc.in)

*The detailed steps of cleaning and preprocessing is present in paper*.

*All experiment are performed using Tensorflow NMT Framework by Thang Luong, Eugene Brevdo, Rui Zhao*.

## Training
The training process is similar to that of [Tensorflow NMT](https://github.com/tensorflow/nmt) however for better handling of hyper-parameters and execution we made a shell script **start.sh**. The hyper-parameters could be changed in the **start.sh** file.

``` shell
bash start.sh
```
or 
```shell
chmod +x start.sh
./start.sh
```
The trained models are saved in the **models/** directory.

## Testing
For testing the trained model on test set execute **out.sh**.
- Translating 2090 English sentences to Bodo sentences
```shell
bash out.sh
```
or
```shell
chmod +x out.sh
./out.sh
```
- View the translated sentence
```shell
gedit output.brx
```
*Terminal editor like nano does not render Bodo characters properly so it's better to view it in gedit or leafpad*

- Calculate BLEU score
```shell
perl multi-bleu.perl nmt_data/tst2013.brx < output.brx
```

## Translating
- Enter English sentence which you want to translate in **test.en** file
- Change the models path in **translate.sh**
- Generate translation [Eng->Brx]
```shell
bash translate.sh
```
or 
```shell
chmod +x translate.sh
./translate.sh
```
- See translated Bodo sentence
```shell
gedit out.brx
```
