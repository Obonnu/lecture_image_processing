# 課題7レポート

標準画像「hiroshi_master」を原画像とする．この画像は縦360画素，横290画素による正方形のディジタルカラー画像である．

ORG=imread('hiroshi_master.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;

によって，原画像を読み込み白黒濃淡に変換した結果を図１に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai7-1.jpg)  
図1 原画像(白黒濃淡)

原画像の

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大

の結果を図２に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai7-2.jpg)  
図2 

同様に

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大

の結果を図３に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai7-3.jpg)  
図3 

は，

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大

の結果を図４～６に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai7-4.jpg)  
図4 
