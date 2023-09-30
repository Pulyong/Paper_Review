# Google BootCamp2023 논문 읽기모임

Google BootCamp에서 Host로 매주 금요일 밤에 진행한 논문 읽기 모임에서 제가 발표한 논문을 정리한 레포입니다.
  
  
  
  
  
  
  
  
  
  



## Computer Vision
### Image Generative Model
--------------------------
1. Restricted Boltzmann Machine(RBM)과 Deep Belief Network(DBN)
     
   2000년대 초기의 Generative Model RBM과 RBM을 쌓아서 만든 Deep Belief Network에 관한 논문입니다.  
   Hinton 교수님은 Andrew Ng 교수님과의 인터뷰에서 자신이 수행한 연구에서 기억에 남는 연구로 DBN에 관한 연구를 뽑았습니다.
   DBN은 Weight Initialization 기법이 없던 시절 모델의 Gradient Vanishing을 줄여주기 위한 Initialization 방법으로 사용됐고 효과가 좋았다고 합니다.
   
   link: https://www.cs.toronto.edu/~hinton/absps/fastnc.pdf

### CNN
---------
1. InternImage: Exploring Large-Scale Vision Foundation Models with Deformable Convolutions
   CVPR 2023에 Accept된 논문으로 COCO Object Detection task에서 Vision Transformer의 성능을 CNN으로 뛰어넘어 2023년 초기에 SOTA를 달성한 모델입니다.  
   논문은 Transformer의 성능이 좋았던 이유를 long-range dependence와 adaptive spatial aggregation으로 정의하고, 이를 Deformable Convolution을 통해 만족시켰습니다.
   이를통해 computation/memory efficient가 떨어진다는 Transformer의 단점까지 해결했다고 논문은 주장했습니다.  
     
   link: https://arxiv.org/pdf/2211.05778.pdf
