# 課題４レポート

今回は比較のため，課題３と同じ画像であるフリー素材サイト「ぱくたそ」の写真を原画像とする．この画像は縦533画素，横800画素によるディジタルカラー画像である．

原画像元　https://www.pakutaso.com/20160656173post-8191.html

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3org.jpg?raw=true)  
図1 原画像     


この元の画像を白黒濃淡画像へ変換した後，画素の濃度ヒストグラムを生成する．


ORG=imread('kadai4org.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって，原画像を読み込み，白黒濃淡画像化を行う．表示した結果を図2に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai4/kadai4-1.png?raw=true)  
図2 白黒濃淡化


imhist(ORG); % ヒストグラムの表示

によって濃度ヒストグラムを表示する．結果を図3に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai4/kadai4-2.png?raw=true)  
図3 図2の濃度ヒストグラム

課題3にて閾値を4パターンにわけて二値化を行った．比較のため閾値を64とした画像と，192とした画像の濃度ヒストグラムを表示する．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai4/kadai3-2-1.png?raw=true)  
図4 閾値64

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai4/kadai3-2-2.png?raw=true)  
図5 図4の濃度ヒストグラム

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai4/kadai3-5-1.png?raw=true)  
図6 閾値192


![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai4/kadai3-5-2.png?raw=true)  
図7 図6の濃度ヒストグラム　　

    
実際に図5，図7で0(黒)と255(白)の2つに二値化されていることがわかる．




