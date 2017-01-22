# 課題６レポート

フリー素材サイト「ぱくたそ」の写真を原画像とする．この画像は縦531画素，横800画素によるディジタルカラー画像である．

原画像元　https://www.pakutaso.com/20130334080post-2554.html

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai6/kadai6org.jpg?raw=true)  
図1 原画像     


この元の画像を白黒濃淡画像へ変換した後，閾値を設ける方法，ディザ法の2つで二値化を行う．ディザ法とは疑似濃淡表示の表示法の一つで，原画像の各画素の濃度値を画素位置によりあらかじめ定められたディザマトリクスTの値(閾値)と比較し，その大小関係で出力画素の濃度値を決定する．


ORG=imread('kadai4org.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって，原画像を読み込み，白黒濃淡画像化を行う．表示した結果を図2に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai6/kadai6-1.png?raw=true)  
図2 白黒濃淡化

IMG = ORG>128; % 128による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

により閾値を128とした二値化を行う．結果を図3に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai6/kadai6-2.png?raw=true)  
図3 閾値を128とした二値化

IMG = dither(ORG); % ディザ法による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

によりディザ法による二値化を行う．結果を図4に示す．

ditherではディザリングによって見かけのカラー解像度を上げてイメージを変換

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai6/kadai6-3.png?raw=true)  
図4 ディザ法による二値化


疑似濃淡表示は実際にファクシミリ等のように2値の濃度値しか表現できない表示装置などでを用いて，多階調画像を表示することが要求される場合に用いられる方法で，そのひとつが今回のディザ法である．  
ディザ法による二値化は，適当に閾値の濃度を設定したものよりも画像が鮮明になっている．



