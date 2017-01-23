# 課題８レポート

フリー素材サイト「ぱくたそ」の写真を原画像とする．この画像は縦533画素，横800画素によるディジタルカラー画像である．

原画像元　https://www.pakutaso.com/20130551148post-2800.html

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai8/kadai8org.jpg?raw=true)  
図1 原画像     


この元の画像を白黒濃淡画像へ変換した後，二値化された画像の連結成分にラベルをつける．二値化画像処理された画像において，白の部分（または黒の部分）が連続した画素に同じ番号を割り振る処理を
ラベリングと言う．


ORG=imread('kadai8org.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって，原画像を読み込み，白黒濃淡画像化を行う．表示した結果を図2に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai8/kadai8-1.png?raw=true)  
図2 白黒濃淡化

IMG = ORG > 128; % 閾値128で二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

により画像を閾値128で二値化する．結果を図3に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai8/kadai8-2.png?raw=true)  
図3 図2の二値化

IMG = bwlabeln(IMG); %バイナリ イメージ内の連結要素をラベル付け  
imagesc(IMG); colormap(jet); colorbar; % 画像の表示 jetはカラースケール


によりラベル付けを行う．結果を図4に示す．


![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai8/kadai8-3.png?raw=true)  
図4 ラベル付け




