# 課題１０レポート

フリー素材サイト「ぱくたそ」の写真を原画像とする．この画像は縦533画素，横800画素によるディジタルカラー画像である．

原画像元　https://www.pakutaso.com/20160532138post-7870.html
![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai10/kadai10org.jpg?raw=true)  
図1 原画像     


この元の画像を白黒濃淡画像へ変換した後，様々なエッジ抽出を行う．画像から対象物の輪郭部の画素を取り出すことをエッジ抽出という．一般に画像中の対象物は背景との濃度の差で分離できるため，濃度の変化点を抽出することで対象物のエッジを検出できる．


ORG=imread('kadai10org.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって，原画像を読み込み，白黒濃淡画像化を行う．表示した結果を図2に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai10/kadai10-1.png?raw=true)  
図2 白黒濃淡化

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示

によりプレウィット法でのエッジ抽出を行う．結果を図3に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai10/kadai10-2.png?raw=true)  
図3 エッジ抽出（プレウィット法）

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示

によりソベル法でのエッジ抽出を行う．結果を図4に示す．


![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai10/kadai10-3.png?raw=true)  
図4 エッジ抽出（ソベル法）

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示

によりキャニー法でのエッジ抽出を行う．結果を図5に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai10/kadai10-4.png?raw=true)  
図4 エッジ抽出（ソベル法）


