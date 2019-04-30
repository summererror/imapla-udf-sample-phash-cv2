# Impala UDF for pHash (C++ Edition)


## License
- [x] ["Anti 996" License](https://github.com/996icu/996.ICU/blob/master/LICENSE)
- [ ] ["Anti 995" License]
- [ ] ["Follow 955" License]
- [ ] ["World Peace" License] Sri Lanka Bombing


- So, I'm waiting for the three licenses above to republic.


## Backgroud

Use [impala-udf-sample](https://github.com/cloudera/impala-udf-samples) to Create an Impala UDF function for image's phash compute based on cv::img_hash::pHash.
provided by [opencv-> pHash](https://docs.opencv.org/4.1.0/df/d4e/classcv_1_1img__hash_1_1PHash.html).



## Note:
Using median instead of avarage function.

Maybe some errors in the phash algorithm, please check it out when you actrually use it.

I'm unfamiliar with JAVA, by the way.


## Speed

0.5s/image, so, it's UNusable in produtive envirment abviously.
Luck!


## Maven

```shell
PATH_TO_MAVEN/mvn clean package
```

then add the .jar to your Hive envirnment, and create the function.

