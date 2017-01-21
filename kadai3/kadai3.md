# 課題３レポート

フリー素材サイト「ぱくたそ」の写真を原画像とする．この画像は縦533画素，横800画素によるディジタルカラー画像である．

原画像元　https://www.pakutaso.com/20160656173post-8191.html

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3org.jpg?raw=true)  
図1 原画像     


この元の画像をグレースケール化した後，4パターンの閾値を設定し，閾値処理した画像を表示する．


ORG=imread('kadai3org.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって，原画像を読み込み，グレースケール化を行う．表示した結果を図2に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3-1.png?raw=true)  
図2 グレースケール化


輝度値が64以上の画素を1，その他を0にするパターン

    
IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換  
imagesc(IMG); colormap(gray); colorbar;


![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3-2.png?raw=true)  
図3 閾値64


輝度値が96以上の画素を1，その他を0にするパターン

IMG = ORG > 96;  
imagesc(IMG); colormap(gray); colorbar;


![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3-3.png?raw=true)  
図4 閾値96

輝度値が128以上の画素を1，その他を0にするパターン



IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;　　




![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3-4.png?raw=true)  
図5 閾値128

輝度値が192以上の画素を1，その他を0にするパターン

IMG = ORG > 192;  
imagesc(IMG); colormap(gray); colorbar;

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3-5.png?raw=true)  
図6 閾値192


