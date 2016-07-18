# 課題8レポート

標準画像「hiroshi_master」を原画像とする．この画像は縦360画素，横290画素による正方形のディジタルカラー画像である．

ORG=imread('hiroshi_master.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;

によって，原画像を読み込み白黒濃淡に変換した結果を図１に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai8-1.jpg)  
図1 原画像(白黒濃淡)

二値化した画像の連結成分にラベル付けを行う.そのために原画像(白黒濃淡)を閾値128で二値化する．

IMG = ORG > 128; % 閾値128で二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

閾値128で二値化した画像の結果を図２に示す．

![閾値128の画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai8-2.jpg)  
図2 閾値128の画像

二値化した画像に「bwlabeln」コマンドを使用する.

IMG = bwlabeln(IMG);
imagesc(IMG); colormap(jet); colorbar; % 画像の表示

ラベリングした画像の結果を図3に表示する.

![ラベリング](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai8-3.jpg)   
図2 ラベリング
