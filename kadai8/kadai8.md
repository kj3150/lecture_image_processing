# �ۑ�W���|�[�g

�t���[�f�ރT�C�g�u�ς������v�̎ʐ^�����摜�Ƃ���D���̉摜�͏c533��f�C��800��f�ɂ��f�B�W�^���J���[�摜�ł���D

���摜���@https://www.pakutaso.com/20130551148post-2800.html

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai8/kadai8org.jpg?raw=true)  
�}1 ���摜     


���̌��̉摜�𔒍��Z�W�摜�֕ϊ�������C��l�����ꂽ�摜�̘A�������Ƀ��x��������D��l���摜�������ꂽ�摜�ɂ����āC���̕����i�܂��͍��̕����j���A��������f�ɓ����ԍ�������U�鏈����
���x�����O�ƌ����D


ORG=imread('kadai8org.jpg'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�����s���D�\���������ʂ�}2�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai8/kadai8-1.png?raw=true)  
�}2 �����Z�W��

IMG = ORG > 128; % 臒l128�œ�l��  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��

�ɂ��摜��臒l128�œ�l������D���ʂ�}3�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai8/kadai8-2.png?raw=true)  
�}3 �}2�̓�l��

IMG = bwlabeln(IMG); %�o�C�i�� �C���[�W���̘A���v�f�����x���t��  
imagesc(IMG); colormap(jet); colorbar; % �摜�̕\�� jet�̓J���[�X�P�[��


�ɂ�胉�x���t�����s���D���ʂ�}4�Ɏ����D


![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai8/kadai8-3.png?raw=true)  
�}4 ���x���t��




