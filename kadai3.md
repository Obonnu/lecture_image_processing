# 課題3レポート

標準画像「hiroshi_master」を原画像とする．この画像は縦360画素，横290画素による正方形のディジタルカラー画像である．

ORG=imread('hiroshi_master.jpg'); % 原画像の入力   
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって，原画像を読み込み白黒濃淡画像に変換し，表示した結果を図１に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai3-1.jpg)  
図1 原画像(白黒濃淡)

白黒濃淡の原画像に閾値を設定することで画素値をある一定の値から上は1、それ以外は0となるように処理する.すなわち,

IMG = ORG > 64; 
imagesc(IMG); colormap(gray); colorbar;

のようにすることで、閾値処理ができる.
閾値を64に設定した結果を図2に示す.

![閾値64](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai3-2.jpg)  
図2 閾値64の画像

同様に閾値を96,128,192の3パターンに設定し,処理を行う．

IMG = ORG > 96;
imagesc(IMG); colormap(gray); colorbar;

IMG = ORG > 128;
imagesc(IMG); colormap(gray); colorbar;

IMG = ORG > 192;
imagesc(IMG); colormap(gray); colorbar;

閾値処理の結果を図3～5に示す.

![閾値96](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai3-3.jpg)  
図3 閾値96

![閾値128](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai3-4.jpg)  
図4 閾値128

![閾値192](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai3-5.jpg)  
図5 閾値192

