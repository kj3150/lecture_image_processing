# �ۑ�Q���|�[�g

�t���[�f�ރT�C�g�u�ς������v�̎ʐ^�����摜�Ƃ���D���̉摜�͏c548��f�C��800��f�ɂ��f�B�W�^���J���[�摜�ł���D

���摜���@https://www.pakutaso.com/20161100334post-9699.html

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai2/kadai2org.jpg?raw=true)  
�}1 ���摜


���̌��̉摜���O���[�X�P�[����������C2�K���C4�K���C8�K���̉摜�𐶐�����D


ORG=imread('kadai2org.jpg'); % ���摜�̓���  
ORG = rgb2gray(ORG); colormap(gray); colorbar; %rgb���O���[�X�P�[����  
imagesc(ORG); axis image; % �摜�̕\��

�ɂ���āC���摜��ǂݍ��݁C�O���[�X�P�[�������s���D�\���������ʂ�}2�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai2/kadai2-1.png?raw=true)  
�}2 �O���[�X�P�[����

2�K���摜�̐������s���D�O���[�X�P�[���������摜(ORG)������256�i�K�̊K����2�i�K�ɋ�؂邽�߁C256/2=128��128�i�K�ŋ�؂�D

    
IMG = ORG>128;   
imagesc(IMG); colormap(gray); colorbar;  axis image;

2�K�����̌��ʂ�}3�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai2/kadai2-2.png?raw=true)  
�}3 2�K����

���l��4�K���𐶐����邽�߂�256/4=64���C64�i�K�ŋ�؂�D

IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2;  
imagesc(IMG); colormap(gray); colorbar;  axis image;

4�K�����̌��ʂ�}4�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai2/kadai2-3.png?raw=true)  
�}4 4�K���摜�̐���

8�K���������l��256/8=32���C32�i�K�ŋ�؂邱�ƂŐ����ł���D  

IMG0 = ORG>32;  
IMG1 = ORG>64;  
IMG2 = ORG>96;  
IMG3 = ORG>128;  
IMG4 = ORG>160;  
IMG5 = ORG>192;  
IMG6 = ORG>224;  
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6  ;  
imagesc(IMG); colormap(gray); colorbar;  axis image;  �@�@

8�K�����摜�̌��ʂ�}5�Ɏ����D  



![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai2/kadai2-4.png?raw=true)  
�}5 8�K���摜�̐���


