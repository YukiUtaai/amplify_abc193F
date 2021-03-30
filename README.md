# amplify_abc193F

## 概要

ABC193Fをアニーリングマシンで解いてみました。

## 実行方法

1. プログラムと同じ階層にAmplifyのアクセストークンを記載した`tokenfile.txt`を作成する。

（もしくは直接`client.token`にアクセストークンを入力する）

2. テストケースをダウンロードする。
https://www.dropbox.com/sh/nx3tnilzqz7df8a/AACpUzqOotp665-GQMdAbHJua/ABC193/F?dl=0&subfolder_nav_tracking=1

3. テストケースを置いたフォルダを指定する（inとoutのところをぞれぞれ）
```shell
files = os.listdir("in")
for file in files:
    with open("in/" + file, "r") as f:
        n = int(f.readline())
        c = [f.readline() for i in range(n)]
    with open("out/" + file, "r") as f:
        ans = int(f.readline())
```        
        
4. プログラムをを実行する

？が存在しないものや、n=1のものも解けるように改良しました。(2021/3/30)

無関係のスピンを1つ追加して計算し、結果からそのスピン分の-1を引いています。

おおよそ最適解が得られています。

```shell
01_sample.txt Amplify結果= 2 正解= 2
02_sample.txt Amplify結果= 4 正解= 4
03_sample.txt Amplify結果= 40 正解= 40
04_hand.txt Amplify結果= 0 正解= 0
05_hand.txt Amplify結果= 0 正解= 0
06_small.txt Amplify結果= 81 正解= 81
07_small.txt Amplify結果= 142 正解= 142
08_small.txt Amplify結果= 39 正解= 39
09_small.txt Amplify結果= 84 正解= 84
10_small.txt Amplify結果= 39 正解= 39
11_small.txt Amplify結果= 62 正解= 62
12_small.txt Amplify結果= 7 正解= 7
13_small.txt Amplify結果= 73 正解= 73
14_small.txt Amplify結果= 10 正解= 10
15_small.txt Amplify結果= 0 正解= 0
16_small.txt Amplify結果= 48 正解= 48
17_small.txt Amplify結果= 0 正解= 0
18_large.txt Amplify結果= 5535 正解= 5535
19_large.txt Amplify結果= 3690 正解= 3690
20_large.txt Amplify結果= 103 正解= 103
21_large.txt Amplify結果= 0 正解= 0
22_large.txt Amplify結果= 4442 正解= 4442
23_large.txt Amplify結果= 8550 正解= 8550
24_large.txt Amplify結果= 14699 正解= 14702
25_large.txt Amplify結果= 8635 正解= 8635
26_large.txt Amplify結果= 13750 正解= 13750
27_large.txt Amplify結果= 0 正解= 0
28_max.txt Amplify結果= 11358 正解= 11358
29_max.txt Amplify結果= 12739 正解= 12739
30_max.txt Amplify結果= 13885 正解= 13885
31_max.txt Amplify結果= 0 正解= 0
32_max.txt Amplify結果= 0 正解= 0
33_max.txt Amplify結果= 19800 正解= 19800
34_max.txt Amplify結果= 19800 正解= 19800
35_max.txt Amplify結果= 10220 正解= 10220
36_max.txt Amplify結果= 17350 正解= 17379
37_max.txt Amplify結果= 16049 正解= 16051
38_max.txt Amplify結果= 13629 正解= 13629
39_max.txt Amplify結果= 10828 正解= 10828
40_max.txt Amplify結果= 9927 正解= 9927
41_max.txt Amplify結果= 10089 正解= 10089

```

