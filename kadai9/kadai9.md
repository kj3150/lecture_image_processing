# �ۑ�X���|�[�g

�t���[�f�ރT�C�g�u�ς������v�̎ʐ^�����摜�Ƃ���D���̉摜�͏c531��f�C��800��f�ɂ��f�B�W�^���J���[�摜�ł���D

���摜���@https://www.pakutaso.com/20130351081post-2559.html

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai9/kadai9org.jpg?raw=true)  
�}1 ���摜     


���̌��̉摜�𔒍��Z�W�摜�֕ϊ�������C���f�B�A���t�B���^�[��K�p���C�m�C�Y������̌�����D�܂������p�̃m�C�Y��Y�t����D


ORG=imread('kadai9org.jpg'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�����s���D�\���������ʂ�}2�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai9/kadai9-1.png?raw=true)  
�}2 �����Z�W��

ORG = imnoise(ORG,'salt & pepper',0.02); % �m�C�Y�Y�t
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

�ɂ��摜�Ƀm�C�Y��Y�t����D���ʂ�}3�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai9/kadai9-2.png?raw=true)  
�}3 �m�C�Y�̓Y�t

IMG = filter2(fspecial('average',3),ORG); % �������t�B���^�ŎG������
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��

�ɂ�蕽�����t�B���^�ł̎G���������s���D���ʂ�}4�Ɏ����D


![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai9/kadai9-3.png?raw=true)  
�}4 �������t�B���^

 
IMG = medfilt2(ORG,[3 3]); % ���f�B�A���t�B���^�ŎG������  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��

�ɂ�胁�f�B�A���t�B���^�ł̎G���������s���D���ʂ�}5�Ɏ����Dmedfilt2(ORG,[3 3])��2�����̃��f�B�A���t�B���^���������s���C�e�o�̓s�N�Z���́C���̓C���[�W���̑Ή�����s�N�Z�����ӂɂ���3�s3��ߖT�̒����l���܂�ł���D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai9/kadai9-4.png?raw=true)  
�}5 ���f�B�A���t�B���^

f=[0,-1,0;-1,5,-1;0,-1,0]; % �t�B���^�̐݌v  
IMG = filter2(f,IMG,'same'); % �t�B���^�̓K�p  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��

�ɂ��t�B���^�̐݌v�C�K�p���s���D���ʂ�}6�Ɏ����D


![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai9/kadai9-5.png?raw=true)  
�}6 �݌v�����t�B���^�̓K�p
