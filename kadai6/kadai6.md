# �ۑ�U���|�[�g

�t���[�f�ރT�C�g�u�ς������v�̎ʐ^�����摜�Ƃ���D���̉摜�͏c531��f�C��800��f�ɂ��f�B�W�^���J���[�摜�ł���D

���摜���@https://www.pakutaso.com/20130334080post-2554.html

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai6/kadai6org.jpg?raw=true)  
�}1 ���摜     


���̌��̉摜�𔒍��Z�W�摜�֕ϊ�������C臒l��݂�����@�C�f�B�U�@��2�œ�l�����s���D�f�B�U�@�Ƃ͋^���Z�W�\���̕\���@�̈�ŁC���摜�̊e��f�̔Z�x�l����f�ʒu�ɂ�肠�炩���ߒ�߂�ꂽ�f�B�U�}�g���N�XT�̒l(臒l)�Ɣ�r���C���̑召�֌W�ŏo�͉�f�̔Z�x�l�����肷��D


ORG=imread('kadai4org.jpg'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�����s���D�\���������ʂ�}2�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai6/kadai6-1.png?raw=true)  
�}2 �����Z�W��

IMG = ORG>128; % 128�ɂ���l��  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��

�ɂ��臒l��128�Ƃ�����l�����s���D���ʂ�}3�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai6/kadai6-2.png?raw=true)  
�}3 臒l��128�Ƃ�����l��

IMG = dither(ORG); % �f�B�U�@�ɂ���l��  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��

�ɂ��f�B�U�@�ɂ���l�����s���D���ʂ�}4�Ɏ����D

dither�ł̓f�B�U�����O�ɂ���Č������̃J���[�𑜓x���グ�ăC���[�W��ϊ�

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai6/kadai6-3.png?raw=true)  
�}4 �f�B�U�@�ɂ���l��


�^���Z�W�\���͎��ۂɃt�@�N�V�~�����̂悤��2�l�̔Z�x�l�����\���ł��Ȃ��\�����u�Ȃǂł�p���āC���K���摜��\�����邱�Ƃ��v�������ꍇ�ɗp��������@�ŁC���̂ЂƂ�����̃f�B�U�@�ł���D  
�f�B�U�@�ɂ���l���́C�K����臒l�̔Z�x��ݒ肵�����̂����摜���N���ɂȂ��Ă���D



