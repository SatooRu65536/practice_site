# 第11回 NET分野実習　2022年7月13日

## ポートフォワーティング
* ポートを公開することで外部からアクセスできるようになる

## うらないアプリ
* 名前の文字数から占うのは面白くない  
-> 文字コードを足した数値で占う
```JavaScript
for (let i=0; i<data.name.length; i++) {
    num += data.name.charCodeAt(i)
}
```

<img src="./images/s1.png" width="600">
<img src="./images/s2.png" width="600">

* 毎日同じ結果は面白くない
-> 日付を数値化して占う数値に足す
```JavaScript
const dt = new Date();
const date_num = Number(dt.getFullYear()) + Number(dt.getMonth()) + Number(dt.getDate())
```

<img src="./images/s3.png" width="600">
<img src="./images/s4.png" width="600">

* 上記２つを足した値を割るだけでは周期的に変化してしまう  
（翌日は前日+1 の値となるため）  
-> 日付をシード値とした乱数を足す
```JavaScript
class Random {
    constructor(seed = 19681106) {
        this.x = 31415926535;
        this.y = 8979323846;
        this.z = 2643383279;
        this.w = seed;
    }
    
    // XorShift
    next() {
        let t;
    
        t = this.x ^ (this.x << 11);
        this.x = this.y; this.y = this.z; this.z = this.w;
        return this.w = (this.w ^ (this.w >>> 19)) ^ (t ^ (t >>> 8)); 
    }
    
    // min以上max以下の乱数を生成する
    nextInt(min, max) {
        const r = Math.abs(this.next());
        return min + (r % (max + 1 - min));
    }
}

let random = new Random(date_num);
num = random.nextInt(0, 10000);
```

<img src="./images/s5.png" width="600">
<img src="./images/s6.png" width="600">

<br>

完成!

<img src="./images/s7.png" width="600">
<img src="./images/s8.png" width="600">


### 参考
[シード値から乱数を生成](http://dotnsf.blog.jp/archives/1080312090.html)
