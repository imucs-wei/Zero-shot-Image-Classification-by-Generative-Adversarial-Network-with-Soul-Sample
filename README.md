本存储库构建于论文《Zero-shot Image Classification by Generative Adversarial Network with Soul Sample》

相关说明如下：

1.代码运行环境
    numpy     1.17.2
    scipy     1.3.1
    torch     0.3.1
    
2.数据集下载：http://datasets.d2.mpi-inf.mpg.de/xian/xlsa17.zip

3.运行样例：
# zsl_awa
python gan.py --proto_param1 3e-2 --proto_param2 3e-5 --ratio 0.1  --manualSeed 9182 --cls_weight 0.01 --preprocessing --val_every 1 --lr 0.00001 --cuda --image_embedding res101 --class_embedding att --netG_name MLP_G --netD_name MLP_CRITIC --nepoch 70 --syn_num 300 --ngh 4096 --ndh 4096 --lambda1 10 --critic_iter 5 --dataset AWA1 --batch_size 64 --nz 85 --attSize 85 --resSize 2048 --outname awa 

# gzsl_awa
python gan.py --proto_param1 1e-3 --proto_param2 3e-5 --ratio 0.1 --gzsl --manualSeed 9182 --cls_weight 0.01 --preprocessing --val_every 1 --lr 0.00001 --cuda --image_embedding res101 --class_embedding att --netG_name MLP_G --netD_name MLP_CRITIC --nepoch 70 --syn_num 1800 --ngh 4096 --ndh 4096 --lambda1 10 --critic_iter 5 --nclass_all 50 --dataset AWA1 --batch_size 64 --nz 85 --attSize 85 --resSize 2048 --outname awa 

# zsl_cub
python gan.py --proto_param1 1e-2 --proto_param2 0.001 --ratio 0.6  --manualSeed 3483 --val_every 1 --cls_weight 0.01 --preprocessing --cuda --image_embedding res101 --class_embedding att --netG_name MLP_G --netD_name MLP_CRITIC --nepoch 70 --ngh 4096 --ndh 4096 --lr 0.0001 --classifier_lr 0.001 --lambda1 10 --critic_iter 5 --dataset CUB --batch_size 64 --nz 312 --attSize 312 --resSize 2048 --syn_num 300 --outname cub 

# gzsl_cub
python gan.py --proto_param1 1e-2 --proto_param2 0.001 --ratio 0.2 --gzsl --manualSeed 3483 --val_every 1 --cls_weight 0.01 --preprocessing --cuda --image_embedding res101 --class_embedding att --netG_name MLP_G --netD_name MLP_CRITIC --nepoch 70 --ngh 4096 --ndh 4096 --lr 0.0001 --classifier_lr 0.001 --lambda1 10 --critic_iter 5 --dataset CUB --nclass_all 200 --batch_size 64 --nz 312 --attSize 312 --resSize 2048 --syn_num 300 --outname cub

# zsl_sun
python gan.py --proto_param1 3e-1 --proto_param2 3e-4 --ratio 0.5  --manualSeed 4115 --cls_weight 0.01 --val_every 1 --preprocessing --cuda --image_embedding res101 --class_embedding att --netG_name MLP_G --netD_name MLP_CRITIC --nepoch 70 --ngh 4096 --ndh 4096 --lambda1 10 --critic_iter 5 --dataset SUN --batch_size 64 --nz 102 --attSize 102 --resSize 2048 --lr 0.0002 --classifier_lr 0.0005 --syn_num 100 --outname sun

# gzsl_sun
python gan.py --proto_param1 3e-1 --proto_param2 3e-5 --ratio 0.1 --gzsl --manualSeed 4115 --cls_weight 0.01 --val_every 1 --preprocessing --cuda --image_embedding res101 --class_embedding att --netG_name MLP_G --netD_name MLP_CRITIC --nepoch 70 --ngh 4096 --ndh 4096 --lambda1 10 --critic_iter 5 --dataset SUN --batch_size 64 --nz 102 --attSize 102 --resSize 2048 --lr 0.0002 --syn_num 400 --classifier_lr 0.001 --nclass_all 717 --outname sun 


