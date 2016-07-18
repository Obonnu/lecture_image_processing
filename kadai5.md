# 課題5レポート

標準画像「hiroshi_master」を原画像とする．この画像は縦360画素，横290画素による正方形のディジタルカラー画像である．

ORG=imread('hiroshi_master.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;

によって，原画像を読み込み白黒濃淡に変換した結果を図１に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai5-1.jpg)  
図1 原画像

判別分析法を用いて、白黒濃淡原画像を二値化する.

はじめに,「imhist」コマンドを使用し,画像のヒストグラムデータを別ベクトルに格納する.

H = imhist(ORG);

次に、格納したデータを2つのクラスに分ける.

C1 = H(1:i);
C2 = H(i+1:256);

これは,格納したデータを一つずつ順番に取り出している.
取り出したC1とC2の画素値,平均値,分散,を算出する.

n1 = sum(C1); 
n2 = sum(C2);
myu1 = mean(C1); 
myu2 = mean(C2);
sigma1 = var(C1); 
sigma2 = var(C2);　

次に,クラス内分散とクラス間分散を算出する.

sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); 
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); 

最後に,「if」コマンドを用いて,クラス間分散をクラス内分散で割った値が0より大きい場合に値の再格納をするように設定する.

if max_val<sigma_B/sigma_w
max_val = sigma_B/sigma_w;
max_thres =i;
end;

これを画素値の最大である,「256」まで繰り返し行うことで,より正確な閾値で二値化することができる.
分析判別法で二値化した画像の結果を図２に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai5-2.jpg)  
図2 分析判別法による二値化画像

