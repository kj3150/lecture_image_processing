# �ۑ�R���|�[�g

�t���[�f�ރT�C�g�u�ς������v�̎ʐ^�����摜�Ƃ���D���̉摜�͏c533��f�C��800��f�ɂ��f�B�W�^���J���[�摜�ł���D

���摜���@https://www.pakutaso.com/20160656173post-8191.html

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3org.jpg?raw=true)  
�}1 ���摜     


���̌��̉摜���O���[�X�P�[����������C4�p�^�[����臒l��ݒ肵�C臒l���������摜��\������D


ORG=imread('kadai3org.jpg'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�

imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

�ɂ���āC���摜��ǂݍ��݁C�O���[�X�P�[�������s���D�\���������ʂ�}2�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3-1.png?raw=true)  
�}2 �O���[�X�P�[����


�P�x�l��64�ȏ�̉�f��1�C���̑���0�ɂ���p�^�[��

    
IMG = ORG > 64; % �P�x�l��64�ȏ�̉�f��1�C���̑���0�ɕϊ�  
imagesc(IMG); colormap(gray); colorbar;


![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3-2.png?raw=true)  
�}3 臒l64


�P�x�l��96�ȏ�̉�f��1�C���̑���0�ɂ���p�^�[��

IMG = ORG > 96;  
imagesc(IMG); colormap(gray); colorbar;


![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3-3.png?raw=true)  
�}4 臒l96

�P�x�l��128�ȏ�̉�f��1�C���̑���0�ɂ���p�^�[��



IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;�@�@




![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3-4.png?raw=true)  
�}5 臒l128

�P�x�l��192�ȏ�̉�f��1�C���̑���0�ɂ���p�^�[��

IMG = ORG > 192;  
imagesc(IMG); colormap(gray); colorbar;

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai3/kadai3-5.png?raw=true) 
�}6 臒l192


