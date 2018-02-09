時間複雜度

###### 簡報：https://goo.gl/L5vscu



---

## 期待／心理準備

----

## Q1: 什麼叫跑得快？

----

跑得快是一個有「**分階段**」的詞

----

![growth](https://i.imgur.com/OHR27Y1.png)

----

## Q2: 怎麼讓一支程式跑得快？

----

- 早期電腦 vs 量子計算機
- n＝5  vs n=100k
- 亂序 vs 升降序
- 演算法

----

![example](https://i.imgur.com/WQFXp4p.png)

----

###### Donald Knuth^[1]^認為一支程式的總運行時間取決於：

 - 每個statement所花費的執行時間
 - 每個statement重複執行的**次數**

----

##### Q1: 什麼叫跑得快？
##### Q2: 怎麼讓一支程式跑得快？
### Q3: 怎麼知道某支程式的 「 演算法 」 跑得快？

----

## 時間複雜度

數據輸入量n->$\infty$， 演算法的時間增長趨勢T(n)。

----

![growth](https://i.imgur.com/OHR27Y1.png)

----

### Big Idea(1)

- Growth of Algorithm 整體成長趨勢

- Amortized Time 共同分擔耗費的時間
   －>允許部份耗費大時間的步驟
   
- Subset of whole program 程式的核心邏輯

----

### Big Idea(2)   
- Insensitive to Input size 輸入量有關，但非主要

- Input size 輸入量n $\neq$ 
  Problem Size(number of operation)步驟計數
   - $\Theta$(n)   
   - $\Theta$(n^2^)   
   - $\Theta$($\log$n)
  

----

##### Asymptotic Line 漸進曲線^[2]^
![Asymptotic](https://i.imgur.com/FlKegbI.png =400x300)

###### $\cfrac{1}{6}$（n^3^ － 3n^2^ ＋ 2n)  
  ~n^3^ 

----

###### $\cfrac{1}{6}$（n^3^ － 3n^2^ ＋ 2n)  
  ~n^3^
- drop the constants 去掉常數
- drop non-dominant terms 去掉非最高階的子項

----

![example7](https://i.imgur.com/7iNc1g5.png)


----

### big $\Theta$ , big O  ,  big $\Omega$
![3](https://i.imgur.com/p8hQNWa.png)


----

![theta](https://i.imgur.com/A6ZXhz3.png =350x350)

######  $\Theta$(g(n))={f(n): 存在正數$c_1$，$c_2$和$n_0$使得對於n$\geq$$n_0$
######   0$\leq$$c_1$$\cdot$g(n)$\leq$f(n)$\leq$$c_2$$\cdot$g(n) } 

----

![o](https://i.imgur.com/5JAChOT.png =350x350)
######  O(g(n))={f(n): 存在正數c和$n_0$使得對於n$\geq$$n_0$
######   0$\leq$f(n)$\leq$c$\cdot$g(n) } 

> big O 是一種對最壞的保證

----

![omega](https://i.imgur.com/WRHBzt5.png =350x350)
######  $\Omega$(g(n))={f(n): 存在正數c和$n_0$使得對於n$\geq$$n_0$
######   0$\leq$c$\cdot$g(n)$\leq$ f(n)} 

>big $\Omega$ 最理想情况

----

小結：
![3](https://i.imgur.com/p8hQNWa.png =900x300)


時間複雜度來描述時間增長趨勢T(n)
- 平均： T(n) =  $\Theta$(g(n)) 
- 最壞／最長： T(n) = O(g(n)) 
- 最佳／最短時：T(n) = $\Omega$(g(n))


---

### 常見的幾大類big O

----

![categories](https://i.imgur.com/ORnwcAn.png =600x650)

----

![growth](https://i.imgur.com/33UhDVr.png =500x550)

----

$\log$n Runtime

[cs50_binary_search](https://www.youtube.com/watch?v=y62zj9ozPOM&t=158s)  21'55-24'39''

![log](https://i.imgur.com/UF3oTSY.png)


----

Recursive time 
```
int f(int n){
   if(n<=1){
     return 1;
   }
   return f(n-1)+f(n-1);
}
```

![recursive](https://i.imgur.com/hR1asAw.png)
2^0^+2^1^+2^2^+2^3^+2^4^ = 2^n+1^ -1
 
- 時間複雜度O(2^n^)
- 空間複雜度O(n)

延伸：example 15 用空間換時間

---

Be careful(1)：
- multi-part algorithms
![multi-part](https://i.imgur.com/1HJZjcS.png)
> [related to: example4&5]

----

- O($\sqrt{n}$)

![sqrt](https://i.imgur.com/IFRgwts.png)
> [from:example10]

----

Be careful(2)：
- input size small, **large** constants & **large** no-donminant terms

- when **sensitive** to input size, negative/positive input


---

Exercise
![2](https://i.imgur.com/BrVH1T3.png =500x300)

----

![4](https://i.imgur.com/KgS9SUZ.png =500x300)

----

![5](https://i.imgur.com/B8PixFd.png =500x300)

----

![6](https://i.imgur.com/yEp2KPE.png =500x300)

----

![9](https://i.imgur.com/u9hIgvw.png =500x300)

----

![10](https://i.imgur.com/gQ31CtS.png =500x300)


---

Reference:
[1]Robert Sedgewick《Algorithm》Page 178
![algorithm](https://algs4.cs.princeton.edu/cover.png =300x400)

----

[2]MIT OpenCourse: Introduction to Algorithms, Fall 2005 
(time:48'25'' link:https://goo.gl/TQiFND)
![Introduction to Algorithms](https://upload.wikimedia.org/wikipedia/en/4/41/Clrs3.jpeg)

----

[3] [Harvard CS50](https://www.youtube.com/watch?v=y62zj9ozPOM&t=158s)
