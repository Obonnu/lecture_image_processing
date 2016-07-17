# 課題2レポート

標準画像「hiroshi_master」を原画像とする．この画像は縦360画素，横290画素による正方形のディジタルカラー画像である．

ORG=imread('hiroshi_master.jpg'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み白黒で表現し，表示した結果を図１に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai2-1.jpg)  
図1 原画像(白黒)

原画像(白黒)を2階調画像に変換するために、画素値を1bit(2×1)で表現する.

IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;

2階調画像の結果を図２に示す．

![2階調](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai2-2.jpg)  
図2 2階調画像

同様に原画像(白黒)を4階調画像に変換するために、画素値を2bit(2×2)で表現する.

IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;
imagesc(IMG); colormap(gray); colorbar;  axis image;

とする．4階調画像の結果を図３に示す．

![4階調](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai2-3.jpg)  
図3 4階調画像

8階調画像の変換は,3bit(2×2×2)を表現するので,同様にして,

IMG3 = ORG>32;
IMG4 = ORG>64;
IMG5 = ORG>96;
IMG6 = ORG>128;
IMG7 = ORG>160;
IMG8 = ORG>192;
IMG9 = ORG>224;
IMG = IMG3 + IMG4 + IMG5 + IMG6 + IMG7 + IMG8 + IMG9;
imagesc(IMG); colormap(gray); colorbar;  axis image;

で表現する．8階調画像の結果を図４に示す．

![8階調画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai2-4.jpg)  
図4 8階調画像
