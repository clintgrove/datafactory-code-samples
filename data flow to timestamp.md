toTimestamp('2021-10-13 15.52.05.488000', 'yyyy-MM-dd HH.mm.ss.SSSSSS')
if you have this string, you cannot use it like this ADF

You have to use it like this

toTimestamp('2021-10-13 15:52:05:488', 'yyyy-MM-dd HH:mm:ss:SSS')

lets say your string for datetime was this 2021-10-13 15.52.05.488000

then do this


`iif(length(toString($$))==26,toTimestamp(dropRight(replace(toString($$),'.',':'),3), 'yyyy-MM-dd HH:mm:ss:SSS'))`


![image](https://github.com/clintgrove/datafactory-code-samples/assets/30802291/ecc133aa-385c-4c80-97be-cbb943cbb4cc)
