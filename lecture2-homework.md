# 第2课 课后作业

## 第1题 转换为bit位 Num2Bits
```
template Num2Bits(n) {
    signal input in;
    signal output out[n];
    var lc1=0;

    var e2=1;
    for (var i = 0; i<n; i++) {
        out[i] <-- (in >> i) & 1; // 仅仅是赋值
        out[i] * (out[i] -1 ) === 0; // 确保全为0 or 1
        lc1 += out[i] * e2; // 加和
        e2 = e2+e2; // 翻倍
    }

    lc1 === in;
}
```

## 第2题 判零 IsZero
```
template IsZero() {
    signal input in;
    signal output out;

    signal inv;

    inv <-- in!=0 ? 1/in : 0 // 1/in 应该就是 in^-1 逆元的意思;

    out <== -in*inv +1 // 如果in为0，则out=1，否则为0;
    in*out === 0// in和out至少有一个为0;
}
```

## 第3题 相等 IsEqual


## 第4题 选择器 Selector


## 第5题 判负 IsNegative


## 第6题 少于 LessThan


## 第7题 整数除法 IntegerDivide


## 第8题 排序 Sort 【可选】
