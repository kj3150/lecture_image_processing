# �ۑ�T���|�[�g

�t���[�f�ރT�C�g�u�ς������v�̎ʐ^�����摜�Ƃ���D���̉摜�͏c533��f�C��800��f�ɂ��f�B�W�^���J���[�摜�ł���D

���摜���@https://www.pakutaso.com/20140108024post-3744.html

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai5/kadai5org.jpg?raw=true)  
�}1 ���摜     


���̌��̉摜�𔒍��Z�W�摜�֕ϊ�������C���ʕ��͖@��p���ē�l������D

���ʕ��͖@�Ƃ́C�Ώە��̔Z�x�ƁC�w�i�̔Z�x�Ƃ����ꂼ��ł��ǂ��܂Ƃ܂�C���Ώە��Ɣw�i�Ƃ̈Ⴂ���ۗ��悤��臒l���߂���@�ł���D���Ȃ킿�C臒lt�ŉ摜��2�̃N���X�ɕ������Ƃ��C����2�̃N���X�ԕ��U�̊e�N���X�����U�ɑ΂����̒l���ł��傫���Ȃ�悤��臒lt���߂�D�����ŁC�N���X�ԕ��U���傫�����Ƃ͔w�i�ƑΏە����悭��������Ă��邱�Ƃł���C�܂��N���X�����U�����������Ƃ͑Ώە�����єw�i�����ꂼ��悭��ɂ܂Ƃ܂��Ă��邱�Ƃ��Ӗ����Ă���D

ORG=imread('kadai4org.jpg'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�����s���D�\���������ʂ�}2�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai5/kadai5-1.png?raw=true)  
�}2 �����Z�W��


H = imhist(ORG); %�q�X�g�O�����̃f�[�^���x�N�g��E�Ɋi�[�@�@
myu_T = mean(H);  
max_val = 0;  
max_thres = 1;  
for i=1:255  
C1 = H(1:i); %�q�X�g�O������2�̃N���X�ɕ�����  
C2 = H(i+1:256);  
n1 = sum(C1); %��f���̎Z�o  
n2 = sum(C2);  
myu1 = mean(C1); %���ϒl�̎Z�o  
myu2 = mean(C2);  
sigma1 = var(C1); %���U�̎Z�o  
sigma2 = var(C2);  
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %�N���X�����U�̎Z�o  
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %�N���X�ԕ��U�̎Z�o  
if max_val<sigma_B/sigma_w  
max_val = sigma_B/sigma_w;  
max_thres =i;  
end;  
end;

IMG = ORG > max_thres;  
imagesc(IMG); colormap(gray); colorbar;

�ɂ�蔻�ʕ��͖@��p������l�����s���D���ʂ�}3�Ɏ����D

![���摜](https://github.com/kj3150/lecture_image_processing/blob/master/kadai5/kadai5-2.png?raw=true)  
�}3 ���ʕ��͖@�ɂ���l��

���ۂɑΏە��ł���L�Ɣw�i�Ō������邱�Ƃ��ł���悤�ɓ�l������Ă���D




