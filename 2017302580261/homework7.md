# p3

a (n-1)d

b (n-1)d

c 0



# p5

a

| 前缀匹配          | 接口 |
| :---------------- | ---- |
| 11100000 00       | 0    |
| 11100000 01000000 | 1    |
| 1110000           | 2    |
| 11100001 1        | 3    |
| 其他              | 3    |

b依次为 其他接口3 1110000接口2 111000011接口3

# p6

| 目的地址范围 | 链路接口 |
| ------------ | -------- |
| 00000000     |          |
| 到           | 0        |
| 00111111     |          |
| 01000000     |          |
| 到           | 1        |
| 01011111     |          |
| 01100000     |          |
| 到           | 2        |
| 01111111     |          |
| 10000000     |          |
| 到           | 2        |
| 10111111     |          |
| 11000000     |          |
| 到           | 3        |
| 11111111     |          |

接口0  64

接口1 32

接口2  96

接口3  64
