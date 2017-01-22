# 課題５レポート

フリー素材サイト「ぱくたそ」の写真を原画像とする．この画像は縦533画素，横800画素によるディジタルカラー画像である．

原画像元　https://www.pakutaso.com/20140108024post-3744.html

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai5/kadai5org.jpg?raw=true)  
図1 原画像     


この元の画像を白黒濃淡画像へ変換した後，判別分析法を用いて二値化する．

判別分析法とは，対象物の濃度と，背景の濃度とがそれぞれ最も良くまとまり，かつ対象物と背景との違いが際立つように閾値を定める方法である．すなわち，閾値tで画像を2つのクラスに分けたとき，その2つのクラス間分散の各クラス内分散に対する比の値が最も大きくなるように閾値tを定める．ここで，クラス間分散が大きいことは背景と対象物がよく分離されていることであり，またクラス内分散が小さいことは対象物および背景がそれぞれよく一つにまとまっていることを意味している．

ORG=imread('kadai4org.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって，原画像を読み込み，白黒濃淡画像化を行う．表示した結果を図2に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai5/kadai5-1.png?raw=true)  
図2 白黒濃淡化


H = imhist(ORG); %ヒストグラムのデータを列ベクトルEに格納　　
myu_T = mean(H);  
max_val = 0;  
max_thres = 1;  
for i=1:255  
C1 = H(1:i); %ヒストグラムを2つのクラスに分ける  
C2 = H(i+1:256);  
n1 = sum(C1); %画素数の算出  
n2 = sum(C2);  
myu1 = mean(C1); %平均値の算出  
myu2 = mean(C2);  
sigma1 = var(C1); %分散の算出  
sigma2 = var(C2);  
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出  
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出  
if max_val<sigma_B/sigma_w  
max_val = sigma_B/sigma_w;  
max_thres =i;  
end;  
end;

IMG = ORG > max_thres;  
imagesc(IMG); colormap(gray); colorbar;

により判別分析法を用いた二値化を行う．結果を図3に示す．

![原画像](https://github.com/kj3150/lecture_image_processing/blob/master/kadai5/kadai5-2.png?raw=true)  
図3 判別分析法による二値化

実際に対象物である猫と背景で見分けることができるように二値化されている．




