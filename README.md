# MurmurHash .NET
C# implementation of Murmur Hash 2

Usage:

```
MurmurHash2.Hash("mystring");
MurmurHash2.Hash(byteArray);
```

I wrote a small benchmark to test the number of collisions on a 466k words (list of all English words taken from here: https://github.com/dwyl/english-words) and **the number of collisions is 22** which I consider a pretty good result.

Standard `string.GetHashCode()` gives **48 collisions** on the 466k word list.

Elapsed time (on the 466k word list):

| Hash | Elapsed time | # of collisions |
| --- | --- | --- |
| MurmurHash2 | 188 ms | 22 |
| GetHashCode | 122 ms | 48 |
