# Chapter1 : String and Array 
Cracking the Code Interview

https://goo.gl/ANVhnK

---

**Outline**
+ Array and String
+ Hash Table
+ ArrayList and Resizable Array
+ StringBuilder
+ Questions

----

### 在做 Array 跟 String 操作時

+ 注意效能
+ 凡事都有代價

---

甚麼是 Array and String?
為何他們常常被放在一起問?

----

Array in C: 有固定大小以及相同種類的資料集合
![](https://i.imgur.com/PSHdeAJ.jpg)

``` 
float marks[100];
```

----

String in C : Array of Characters. terminate by \0

```
char c[] = "abcd";
char c[] = {'a', 'b', 'c', 'd', '\0'};
```

----

### 在 C 語言 
問 String 的問題就是問 Array 的問題

----

How About Other Languages ?

----

### Array in Javascript
An array is a special variable, which can hold more than one value at a time.

```
var cars = ["Saab", "Volvo", "BMW"];
var mix = ["Saab", "Volvo", 1]; (no error)
```

----

### String in Javascript
primitive data type

```
var s = "this is a string"

```

----

### V8 Engine is written by C++

----

### Another Example: Golang
Golang Is A New C

----

Go Array: fixed size and type
Go String: string is byte slices


---

### Hash Table: 是一種高效能 mapping key 跟 value 的資料結構


Example: 電話簿
![](https://i.imgur.com/0HIg4e7.png)

----

### 如何實現最簡單的電話簿?

----

### Hash Table

+ BigO(1) Search time
+ 空間換取時間

----

### 簡易 Hash Table 步驟
+ 計算 Key 的 Hash Code.
+ Map Hash Code 到 Array Index.
    + hash(key)%array length
+ Collision: Linked List

----

![](https://i.imgur.com/NO6GJYF.png)

---

## ArrayList and Resizable Arrays

----

+ 當你需要使用 Array-like 但又是可變動大小資料結構時，請使用 ArrayList (Java)
+ ArrayList BigO(1) Access
+ 典型的Resize implement - 當 Array 滿了， 那麼 double array size (Java)
+ Double 的動作 BigO(N)

~~+ amortized insertion time 是 O(1)~~

---

## StringBuilder

----

### 問題: 把 string array 串一起成一個 string 要花多少時間 ?
+ 每個 string length = x
+ 總共 n 個 string in Array

```
string[] words = {"aa","bb","cc"}
string sentence = "aabbcc"
(x = 2, n =3 )

```


----

```
String joinWords(String[] words) {
    String sentence = "";
    for (String w : words) {
        sentence = sentence + w;
    }
    return sentence;
}

```
+ O(1x+2x+... nx) => O(x$n^2$) => O($n^2$)


----

### StringBuilder 為了解決這問題
+ string 變成 resizable array, 
+ 當需要時，再copy 成一個 string

```
String joinWords(String[] words) {
    StringBuilder sentence = StringBuilder();
    for (String w : words) {
        sentence.append(w)
    }
    return sentence.toString();
}
```

---

### 練習

+ Array and String 定義 ?
+ 有沒有 HashMap/HashTable ?
+ Resizable Array 是什麼 ? 
+ 是否有 StringBuilder ? 

----

### Golang

+ Array: fixed size and type

```
var a [10]int
```
+ String: basic type. string is byte slices

```

var hello = "hello"
```


----

+ map (built-in)

```
 m := make(map[string]int)
 m := make(map[string]int, 100)

```
+ Resizable Array: slice

```
//array
b := [2]string{"Penn", "Teller"}
//slice
letters := []string{"a", "b", "c", "d"}

```

----

StringBuilder? (如何 concatenate string ?)
[Efficient String Concatenation in Go](http://herman.asia/efficient-string-concatenation-in-go)

+ Method I : += 
    + BigO($n^2$)
```
setence = sentence + w
```

----


+ Method II : strings.Join 
    + Big(n)

```
    s := []string{}
	for i := 0; i < 1000; i++ {
		s = append(s, "a")
	}
	fmt.Println(strings.Join(s, ""))
```

----

+ Method III: bytes.Buffer
    + Big(n)

```
var buffer bytes.Buffer
for i := 0; i < 1000; i++ {
    buffer.WriteString("a")
}
fmt.Println(buffer.String())

```

----

For Short string

![](https://i.imgur.com/kIKc1VO.png)


----

For Longer string

![](https://i.imgur.com/hfsUudq.png)


----

Only for Join function

![](https://i.imgur.com/XJCpFMx.png)


---

### Questin 1.1: Is Unique
Implement an algorithm to determine if a string has all unique characters. What if you can not use additional data structure?

---

###### tags: `wwc` `cracking the code interview` `cracking` `interview` `string` `array` `slide` `presentation`
