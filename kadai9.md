# 課題9レポート

標準画像「hiroshi_master」を原画像とする．この画像は縦360画素，横290画素によるディジタルカラー画像である．

ORG=imread('hiroshi_master.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;

によって，原画像を読み込み白黒濃淡に変換した結果を図１に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai9-1.jpg)  
図1 原画像(白黒濃淡)

メディアンフィルターを適用し、ノイズを除去する.
原画像にノイズを添付する.

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

ノイズを添付した画像の結果を図２に示す．

![ノイズ画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai9-2.jpg)  
図2 ノイズ画像

平滑化フィルタを適用し、雑音を除去する.

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去
imagesc(IMG); colormap(gray); colorbar;

雑音を除去した画像の結果を図3に示す.

![平滑化フィルタでの雑音除去](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai9-3.jpg)  
図3 平滑化フィルタでの雑音除去

メディアンフィルタを適用し、雑音を除去する.

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

雑音を除去した画像の結果を図4に示す.

![メディアンフィルタの雑音除去](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai9-4.jpg)  
図4 メディアンフィルタでの雑音除去

次にフィルタを作成し,雑音を除去する.

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計
IMG = filter2(f,IMG,'same'); % フィルタの適用
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

作成したフィルタを適用した画像の結果を図5に示す.

![作成したフィルタの雑音除去](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai9-5.jpg)  
図4 作成したフィルタでの雑音除去

