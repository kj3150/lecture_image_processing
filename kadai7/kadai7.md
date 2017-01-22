# 課題７レポート

フリー素材サイト「ぱくたそ」の写真を原画像とする．この画像は縦533画素，横800画素によるディジタルカラー画像である．

原画像元　https://www.pakutaso.com/20150846218post-5860.html

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai7/kadai7org.jpg?raw=true)  
図1 原画像     


この元の画像を白黒濃淡画像へ変換した後，画素のダイナミックレンジを0から255に拡大する．ダイナミックレンジとは画像においては明るさと暗さの最大値および最小値の差である．この差が大きいほど，広いダイナミックレンジが得られる．


ORG=imread('kadai7org.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって，原画像を読み込み，白黒濃淡画像化を行う．表示した結果を図2に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai7/kadai7-1.png?raw=true)  
図2 白黒濃淡化

imhist(ORG); % 濃度ヒストグラムを生成、表示

により図2の濃度ヒストグラムを生成表示する．結果を図3に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai7/kadai7-2.png?raw=true)  
図3 図2の濃度ヒストグラム

ORG = double(ORG);  
mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  


によりダイナミックレンジの拡大を行う．結果を図4に示す．
またmn=1，mx=249となった．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai7/kadai7-3.png?raw=true)  
図4 ダイナミックレンジの拡大

ORG = uint8(ORG);  %8ビット符号なし整数へ変換  
imhist(ORG); % 濃度ヒストグラムを生成、表示

によりORGを8ビット符号なし整数へ変換し，濃度ヒストグラムを生成表示する．結果を図5に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai7/kadai7-4.png?raw=true)  
図5 図4の濃度ヒストグラム


図2と図4を比べると図中右のカラーバーより濃度の広さ，ダイナミックレンジが拡大されていることがわかる．

図5において「ORG = uint8(ORG);」の部分をカットした場合，ORGはdouble型になり，濃度ヒストグラムは図6のようになった．これを挿入し直した場合，ORGはuint8型になり濃度ヒストグラムは図5に戻った．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai7/kadai7-5.png?raw=true)  
図6 「ORG = uint8(ORG);」無しの場合の濃度ヒストグラム

