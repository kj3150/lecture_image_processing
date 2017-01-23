# 課題９レポート

フリー素材サイト「ぱくたそ」の写真を原画像とする．この画像は縦531画素，横800画素によるディジタルカラー画像である．

原画像元　https://www.pakutaso.com/20130351081post-2559.html

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai9/kadai9org.jpg?raw=true)  
図1 原画像     


この元の画像を白黒濃淡画像へ変換した後，メディアンフィルターを適用し，ノイズ除去を体験する．また除去用のノイズを添付する．


ORG=imread('kadai9org.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって，原画像を読み込み，白黒濃淡画像化を行う．表示した結果を図2に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai9/kadai9-1.png?raw=true)  
図2 白黒濃淡化

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

により画像にノイズを添付する．結果を図3に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai9/kadai9-2.png?raw=true)  
図3 ノイズの添付

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

により平滑化フィルタでの雑音除去を行う．結果を図4に示す．


![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai9/kadai9-3.png?raw=true)  
図4 平滑化フィルタ

 
IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

によりメディアンフィルタでの雑音除去を行う．結果を図5に示す．medfilt2(ORG,[3 3])は2次元のメディアンフィルタ処理を実行し，各出力ピクセルは，入力イメージ内の対応するピクセル周辺にある3行3列近傍の中央値を含んでいる．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai9/kadai9-4.png?raw=true)  
図5 メディアンフィルタ

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  
IMG = filter2(f,IMG,'same'); % フィルタの適用  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

によりフィルタの設計，適用を行う．結果を図6に示す．


![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai9/kadai9-5.png?raw=true)  
図6 設計したフィルタの適用
