# �ۑ�P�O���|�[�g

�t���[�f�ރT�C�g�u�ς������v�̎ʐ^�����摜�Ƃ���D���̉摜�͏c533��f�C��800��f�ɂ��f�B�W�^���J���[�摜�ł���D

���摜���@https://www.pakutaso.com/20160532138post-7870.html
![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai10/kadai10org.jpg?raw=true)  
�}1 ���摜     


���̌��̉摜�𔒍��Z�W�摜�֕ϊ�������C�l�X�ȃG�b�W���o���s���D�摜����Ώە��̗֊s���̉�f�����o�����Ƃ��G�b�W���o�Ƃ����D��ʂɉ摜���̑Ώە��͔w�i�Ƃ̔Z�x�̍��ŕ����ł��邽�߁C�Z�x�̕ω��_�𒊏o���邱�ƂőΏە��̃G�b�W�����o�ł���D


ORG=imread('kadai10org.jpg'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�����s���D�\���������ʂ�}2�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai10/kadai10-1.png?raw=true)  
�}2 �����Z�W��

IMG = edge(ORG,'prewitt'); % �G�b�W���o�i�v���E�B�b�g�@�j  
imagesc(IMG); colormap('gray'); colorbar;% �摜�\��

�ɂ��v���E�B�b�g�@�ł̃G�b�W���o���s���D���ʂ�}3�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai10/kadai10-2.png?raw=true)  
�}3 �G�b�W���o�i�v���E�B�b�g�@�j

IMG = edge(ORG,'sobel'); % �G�b�W���o�i�\�x���@�j  
imagesc(IMG); colormap('gray'); colorbar;% �摜�\��

�ɂ��\�x���@�ł̃G�b�W���o���s���D���ʂ�}4�Ɏ����D


![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai10/kadai10-3.png?raw=true)  
�}4 �G�b�W���o�i�\�x���@�j

IMG = edge(ORG,'canny'); % �G�b�W���o�i�L���j�[�@�j  
imagesc(IMG); colormap('gray'); colorbar;% �摜�\��

�ɂ��L���j�[�@�ł̃G�b�W���o���s���D���ʂ�}5�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai10/kadai10-4.png?raw=true)  
�}4 �G�b�W���o�i�\�x���@�j


