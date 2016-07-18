# 課題4レポート

標準画像「hiroshi_master」を原画像とする．この画像は縦360画素，横290画素によるディジタルカラー画像である．

ORG=imread('hiroshi_master.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;

によって，原画像を読み込み白黒濃淡に変換した結果を図１に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai4-1.jpg)  
図1 原画像(白黒濃淡)

白黒濃淡原画像のヒストグラムを表示するために「imhist」コマンドを使用する．

imhist(ORG);

表示したヒストグラムの結果を図２に示す．

![ヒストグラム](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai4-2.jpg)  
図2 ヒストグラム

このように、画像のヒストグラムを表示することで、2値化など行う際の値の目安を知ることが出来る.