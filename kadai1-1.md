# �ۑ�P���|�[�g

�t���[�f�ރT�C�g�u�ς������v�̎ʐ^�����摜�Ƃ���D���̉摜�͏c548��f�C��800��f�ɂ��f�B�W�^���J���[�摜�ł���D

���摜�� https://www.pakutaso.com/20150524127post-5476.html

ORG=imread('Lenna.png'); % ���摜�̓���  
imagesc(ORG); axis image; % �摜�̕\��

�ɂ���āC���摜��ǂݍ��݁C�\���������ʂ�}1�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/image/kadai1-1.png?raw=true)  
�}1 ���摜

���摜��1/2�T���v�����O����ɂ́C�摜��1/2�{�ɏk��������C2�{�Ɋg�傷��΂悢�D�Ȃ��C�g�傷��ۂɂ́C�P����Ԃ��邽�߂Ɂubox�v�I�v�V������ݒ肷��D

IMG = imresize(ORG,0.5); % �摜�̏k��  
IMG2 = imresize(IMG,2,'box'); % �摜�̊g��

1/2�T���v�����O�̌��ʂ�}2�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/image/kadai1-2.png?raw=true)  
�}2 1/2�T���v�����O

���l�Ɍ��摜��1/4�T���v�����O����ɂ́C�摜��1/2�{�ɏk��������C2�{�Ɋg�傷��΂悢�D���Ȃ킿�C

IMG = imresize(ORG,0.5); % �摜�̏k��  
IMG2 = imresize(IMG,2,'box'); % �摜�̊g��

�Ƃ���D1/4�T���v�����O�̌��ʂ�}3�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/image/kadai1-3.png?raw=true)  
�}3 1/4�T���v�����O

1/8����1/32�T���v�����O�́C

IMG = imresize(ORG,0.5); % �摜�̏k��  
IMG2 = imresize(IMG,2,'box'); % �摜�̊g��

���J��Ԃ��D�T���v�����O�̌��ʂ�}4�`6�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/image/kadai1-4.png?raw=true)  
�}4 1/8�T���v�����O

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/image/kadai1-5.png?raw=true)  
�}5 1/16�T���v�����O

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/image/kadai1-6.png?raw=true)  
�}6 1/32�T���v�����O

���̂悤�ɃT���v�����O�����傫���Ȃ�ƁC���U�C�N��̃T���v�����O�c�݂���������D