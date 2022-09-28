# キュー

スタックは、データの格納淳人は逆の順序でデータを取り出していくLIFO(後入れ先出し)方式であったが。窓口に並んだ待ち行列を処理するにはLIFO方式では後に並んだ客から処理されることになり、不公平である。

こうした場合はFIFO(先入れ先出し)方式のデータ構造が必要となる。このモデルが待ち行列(キュー)である。

![image](https://user-images.githubusercontent.com/82156802/192759660-5bac218f-cb6d-4ec3-ba03-1f2fd570d7e2.png)


キューにデータを入れることをenqueue、データを取り出すことをdequeueと呼ぶ。

## リングバッファ

![image](https://user-images.githubusercontent.com/82156802/192760194-0292f1cb-5acc-44a9-8876-3e327c6333cd.png)


![image](https://user-images.githubusercontent.com/82156802/192760033-57e3825f-913f-4ad1-b383-4e5ad2b5c5f3.png)

![image](https://user-images.githubusercontent.com/82156802/192760051-c5586dc3-5814-447a-95c8-54a0793063e8.png)

```c

```

