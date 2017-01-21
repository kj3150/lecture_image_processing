# 課題２レポート

フリー素材サイト「ぱくたそ」の写真を原画像とする．この画像は縦548画素，横800画素によるディジタルカラー画像である．

原画像元　https://www.pakutaso.com/20161100334post-9699.html

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai2/kadai2org.jpg?raw=true)  
図1 原画像


この元の画像をグレースケール化した後，2階調，4階調，8階調の画像を生成する．


ORG=imread('kadai2org.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar; %rgbをグレースケールに  
imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，グレースケール化を行う．表示した結果を図2に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai2/kadai2-1.png?raw=true)  
図2 グレースケール化

2階調画像の生成を行う．グレースケール化した画像(ORG)を元の256段階の階調を2段階に区切るため，256/2=128の128段階で区切る．

    
IMG = ORG>128;   
imagesc(IMG); colormap(gray); colorbar;  axis image;

2階調化の結果を図3に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai2/kadai2-2.png?raw=true)  
図3 2階調化

同様に4階調を生成するために256/4=64より，64段階で区切る．

IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2;  
imagesc(IMG); colormap(gray); colorbar;  axis image;

4階調化の結果を図4に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai2/kadai2-3.png?raw=true)  
図4 4階調画像の生成

8階調化も同様に256/8=32より，32段階で区切ることで生成できる．  

IMG0 = ORG>32;  
IMG1 = ORG>64;  
IMG2 = ORG>96;  
IMG3 = ORG>128;  
IMG4 = ORG>160;  
IMG5 = ORG>192;  
IMG6 = ORG>224;  
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6  ;  
imagesc(IMG); colormap(gray); colorbar;  axis image;  　　

8階調化画像の結果を図5に示す．  



![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai2/kadai2-4.png?raw=true)  
図5 8階調画像の生成


