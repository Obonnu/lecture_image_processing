# 課題6レポート

標準画像「hiroshi_master」を原画像とする．この画像は縦360画素，横290画素による正方形のディジタルカラー画像である．

ORG=imread('hiroshi_master.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;

によって，原画像を読み込み白黒濃淡に変換した結果を図１に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai3-1.jpg)  
図1 原画像(白黒濃淡)

白黒濃淡画像を二値化する.値は128とする.

IMG = ORG>128; % 128による二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

128で二値化した画像の結果を図２に示す．

![二値化(128)](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai6-1.jpg)  
図2 二値化(128)

次にディザ法による二値化を行う.処理を行うために,「dither」コマンドを使用する.

IMG = dither(ORG); % ディザ法による二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

ディザ法による画像の結果を図３に示す．

![ディザ法](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai6-2.jpg)  
図3 ディザ法

