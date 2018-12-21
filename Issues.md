### 2018-12-21 bcolz OSError: data directory does not exist 【seems solved】
https://github.com/Nov05/fastai/blob/master/colab/lesson1_bcolz_error.ipynb
It was probably caused by corrupted training/testing datasets. Fetch datasets from remote rather than uploading from local.
`!wget http://files.fast.ai/data/dogscats.zip && unzip -qq dogscats.zip -d drive/'My Drive'/colab/data/`
```
--2018-12-21 00:29:26--  http://files.fast.ai/data/dogscats.zip
Resolving files.fast.ai (files.fast.ai)... 67.205.15.147
Connecting to files.fast.ai (files.fast.ai)|67.205.15.147|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 857214334 (818M) [application/zip]
Saving to: ‘dogscats.zip’
```

### 2018-12-21 TypeError: No loop matching the specified signature and casting was found for ufunc add 【open】
https://github.com/Nov05/fastai/blob/master/lesson1_no-loop-matching-error.ipynb
Also the batch size shouldn't be too large, Colab seems to have problems with that. 20 should be fine.

