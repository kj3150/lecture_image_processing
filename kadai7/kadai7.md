# �ۑ�V���|�[�g

�t���[�f�ރT�C�g�u�ς������v�̎ʐ^�����摜�Ƃ���D���̉摜�͏c533��f�C��800��f�ɂ��f�B�W�^���J���[�摜�ł���D

���摜���@https://www.pakutaso.com/20150846218post-5860.html

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai7/kadai7org.jpg?raw=true)  
�}1 ���摜     


���̌��̉摜�𔒍��Z�W�摜�֕ϊ�������C��f�̃_�C�i�~�b�N�����W��0����255�Ɋg�傷��D�_�C�i�~�b�N�����W�Ƃ͉摜�ɂ����Ă͖��邳�ƈÂ��̍ő�l����эŏ��l�̍��ł���D���̍����傫���قǁC�L���_�C�i�~�b�N�����W��������D


ORG=imread('kadai7org.jpg'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�����s���D�\���������ʂ�}2�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai7/kadai7-1.png?raw=true)  
�}2 �����Z�W��

imhist(ORG); % �Z�x�q�X�g�O�����𐶐��A�\��

�ɂ��}2�̔Z�x�q�X�g�O�����𐶐��\������D���ʂ�}3�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai7/kadai7-2.png?raw=true)  
�}3 �}2�̔Z�x�q�X�g�O����

ORG = double(ORG);  
mn = min(ORG(:)); % �Z�x�l�̍ŏ��l���Z�o  
mx = max(ORG(:)); % �Z�x�l�̍ő�l���Z�o  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  


�ɂ��_�C�i�~�b�N�����W�̊g����s���D���ʂ�}4�Ɏ����D
�܂�mn=1�Cmx=249�ƂȂ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai7/kadai7-3.png?raw=true)  
�}4 �_�C�i�~�b�N�����W�̊g��

ORG = uint8(ORG);  %8�r�b�g�����Ȃ������֕ϊ�  
imhist(ORG); % �Z�x�q�X�g�O�����𐶐��A�\��

�ɂ��ORG��8�r�b�g�����Ȃ������֕ϊ����C�Z�x�q�X�g�O�����𐶐��\������D���ʂ�}5�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai7/kadai7-4.png?raw=true)  
�}5 �}4�̔Z�x�q�X�g�O����


�}2�Ɛ}4���ׂ�Ɛ}���E�̃J���[�o�[���Z�x�̍L���C�_�C�i�~�b�N�����W���g�傳��Ă��邱�Ƃ��킩��D

�}5�ɂ����āuORG = uint8(ORG);�v�̕������J�b�g�����ꍇ�CORG��double�^�ɂȂ�C�Z�x�q�X�g�O�����͐}6�̂悤�ɂȂ����D�����}�����������ꍇ�CORG��uint8�^�ɂȂ�Z�x�q�X�g�O�����͐}5�ɖ߂����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai7/kadai7-5.png?raw=true)  
�}6 �uORG = uint8(ORG);�v�����̏ꍇ�̔Z�x�q�X�g�O����

