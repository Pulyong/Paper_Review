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

   Real MNIST
   
   <img width="60%" src="https://github.com/Pulyong/Paper_Review/assets/76218918/c82347b4-01fb-492b-89a1-0f2854694eda"/>

   RBM Reconstruction MNIST

   <img width="60%" src="https://github.com/Pulyong/Paper_Review/assets/76218918/5b291db7-5d47-4f9d-9ea2-313a7e0edabe"/>

3. Auto-Encoding Variational Bayes

   Variational Auto-Encoder에 대한 논문입니다.
   Variational Inference를 통해 원하는 분포에 근사 시키고 Deep Neural Network를 Maximum Likelihood 관점으로 해석한 점이 재미있는 논문이였습니다.
   수학적으로 완성도 있고 심도 깊은 논문이였고, 여러 응용이 들어갈 수 있는 모델이라 흥미로웠습니다.

   link: https://arxiv.org/pdf/1312.6114.pdf

   Real MNIST
   
   <img width="60%" src="https://github.com/Pulyong/Paper_Review/assets/76218918/0ead4f44-a086-4ab6-9e31-17028af58a2c"/>

   VAE Reconstruction MNIST

   <img width="60%" src="https://github.com/Pulyong/Paper_Review/assets/76218918/d6660735-bc7a-4f8c-9334-8aec6d8b6d4b"/>

### CNN
---------
1. InternImage: Exploring Large-Scale Vision Foundation Models with Deformable Convolutions
   CVPR 2023에 Accept된 논문으로 COCO Object Detection task에서 Vision Transformer의 성능을 CNN으로 뛰어넘어 2023년 초기에 SOTA를 달성한 모델입니다.  
   논문은 Transformer의 성능이 좋았던 이유를 long-range dependence와 adaptive spatial aggregation으로 정의하고, 이를 Deformable Convolution을 통해 만족시켰습니다.
   이를통해 computation/memory efficient가 떨어진다는 Transformer의 단점까지 해결했다고 논문은 주장했습니다.  
     
   link: https://arxiv.org/pdf/2211.05778.pdf
