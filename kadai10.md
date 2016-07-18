# 課題10レポート

標準画像「hiroshi_master」を原画像とする．この画像は縦360画素，横290画素によるディジタルカラー画像である．

ORG=imread('hiroshi_master.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;

によって，原画像を読み込み白黒濃淡に変換した結果を図１に示す．

![原画像](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai10-1.jpg)
図1 原画像(白黒濃淡)

画像のエッジ抽出を行う.
初めにブレウィット法によるエッジ抽出を行う.

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示

ブレウィット法でエッジ抽出した画像の結果を図２に示す．

![ブレウィット法によるエッジ抽出](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai10-2.jpg)
図2 ブレウィット法によるエッジ抽出

次にソベル法によるエッジ抽出を行う.

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示

ソベル法でエッジ抽出した画像の結果を図3に示す.

![ソベル法によるエッジ抽出](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai10-3.jpg)
図3 ソベル法によるエッジ抽出

次にキャニー法によるエッジ抽出を行う.

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示

キャニー法でエッジ抽出した画像の結果を図4に示す.

![キャニー法によるエッジ抽出](https://github.com/Obonnu/lecture_image_processing/blob/master/image/hiroshi_kadai10-4.jpg)
図4 キャニー法によるエッジ抽出

