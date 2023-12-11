# Google BootCamp2023 논문 읽기모임

Google BootCamp에서 Host로 매주 금요일 밤에 진행한 논문 읽기 모임에서 제가 발표한 논문을 정리한 레포입니다.
  
  
  
  
  
  
  
  
  
  



## Computer Vision
### Image Generative Model
--------------------------
1. Restricted Boltzmann Machine(RBM)과 Deep Belief Network(DBN)
     
   2000년대 초기의 Generative Model RBM과 RBM을 쌓아서 만든 Deep Belief Network에 관한 논문입니다.  
   Hinton 교수님은 Andrew Ng 교수님과의 인터뷰에서 자신이 수행한 연구에서 기억에 남는 연구로 DBN에 관한 연구를 뽑았습니다.
   DBN은 Weight Initialization 기법이 없던 시절 모델의 Gradient Vanishing을 줄여주기 위한 Initialization 방법으로 사용됐고 효과가 좋았다고 합니다.

   <a href='https://github.com/Pulyong/Paper_Review/blob/main/Computer%20Vision/Generative%20model/A%20Fast%20Learning%20Algorithm%20for%20Deep%20Belief%20Nets.pdf' target='_blank'>Review link</a>
      
   link: https://www.cs.toronto.edu/~hinton/absps/fastnc.pdf

   Real MNIST
   
   <img width="60%" src="https://github.com/Pulyong/Paper_Review/assets/76218918/c82347b4-01fb-492b-89a1-0f2854694eda"/>

   RBM Reconstruction MNIST

   <img width="60%" src="https://github.com/Pulyong/Paper_Review/assets/76218918/5b291db7-5d47-4f9d-9ea2-313a7e0edabe"/>

2. Auto-Encoding Variational Bayes

   Variational Auto-Encoder에 대한 논문입니다.
   Variational Inference를 통해 원하는 분포에 근사 시키고 Deep Neural Network를 Maximum Likelihood 관점으로 해석한 점이 재미있는 논문이였습니다.
   수학적으로 완성도 있고 심도 깊은 논문이였고, 여러 응용이 들어갈 수 있는 모델이라 흥미로웠습니다.

   <a href='https://github.com/Pulyong/Paper_Review/blob/main/Computer%20Vision/Generative%20model/Auto-Encoding%20Variational%20Bayes.pdf' target='_blank'>Review link</a>  
     
   link: https://arxiv.org/pdf/1312.6114.pdf

   Real MNIST
   
   <img width="60%" src="https://github.com/Pulyong/Paper_Review/assets/76218918/0ead4f44-a086-4ab6-9e31-17028af58a2c"/>

   VAE Reconstruction MNIST

   <img width="60%" src="https://github.com/Pulyong/Paper_Review/assets/76218918/d6660735-bc7a-4f8c-9334-8aec6d8b6d4b"/>

3. Generative Adversarial Nets

    GAN에 대한 논문입니다.
    Generative Model을 공부하고 싶었던 이유가 바로 GAN 때문이였습니다.
    처음 GAN을 접하고 두 모델이 경쟁하면서 학습이 가능하다는 사실이 흥미로웠습니다. 또한 해당 모델의 타당성을 수학적으로 증명한 것 또한 굉장히 배울점이 많았습니다.
    GAN은 수많은 variation을 만든 만큼 Diffusion model이 등장했지만 충분히 매력적이고 효과적인 모델이라고 생각합니다.

    <a href='https://github.com/Pulyong/Paper_Review/blob/main/Computer%20Vision/Generative%20model/Generative%20Adversarial%20Nets.pdf' target='_blank'>Review link</a>
     
    link: https://browse.arxiv.org/pdf/1406.2661.pdf

    Generate MNIST
  
    <img width="60%" src="https://github.com/Pulyong/Paper_Review/assets/76218918/1bd86333-d6e1-41fb-95bd-f804137d15c1"/>
    
4. CycleGAN

    GAN을 이용한 Style Transfer 논문입니다.
    Pix2Pix 논문에서는 Input Image와 style이 바뀐 Target Image pair가 필요했습니다. 하지만 현실적으로 Pair Image는 구하기 힘들기 때문에 CycleGAN은 Unpair Image를 Input과 Target으로 주게됩니다.
    Input과 Target Image가 서로의 도메인으로 변환 되었다가 다시 본인의 도메인으로 Reconstruct하는 방식을 통해 최대한 Image 형태의 변환 없이 Style만 상대의 도메인으로 transfer 시키는 아이디어가 흥미로웠습니다.

    <a href='https://github.com/Pulyong/Paper_Review/blob/main/Computer%20Vision/Generative%20model/Unpaired%20Image-to-Image%20Translation%20using%20Cycle-Consistent%20Adversarial%20Networks.pdf' target='_blank'>Review link</a>
      
    link: https://arxiv.org/pdf/1703.10593.pdf
  
  
5. Denoising Diffusion Probabilistic Models

   Diffusion Model에 대한 논문입니다.
   최근에 Image Generation 분야에서 빠르게 발전되고 있는 모델입니다.
   단순 Image-to-Image Generation 뿐만 아니라 Text-to-Image, Speech|Audio Generation 등등 굉장히 많은 도메인에서 사용되고 있습니다.


   <a href='https://github.com/Pulyong/Paper_Review/blob/main/Computer%20Vision/Generative%20model/DDPM.pdf' target='_blank'>Review link</a>
    
   link: https://arxiv.org/pdf/2006.11239.pdf

   Implementation은 <a href='https://github.com/Pulyong/All_About_Diffusion' target='_blank'>All_About_Diffusion</a> repo에 올릴 예정입니다.

### CNN
---------
1. InternImage: Exploring Large-Scale Vision Foundation Models with Deformable Convolutions
   CVPR 2023에 Accept된 논문으로 COCO Object Detection task에서 Vision Transformer의 성능을 CNN으로 뛰어넘어 2023년 초기에 SOTA를 달성한 모델입니다.  
   논문은 Transformer의 성능이 좋았던 이유를 long-range dependence와 adaptive spatial aggregation으로 정의하고, 이를 Deformable Convolution을 통해 만족시켰습니다.
   이를통해 computation/memory efficient가 떨어진다는 Transformer의 단점까지 해결했다고 논문은 주장했습니다.  
     
   link: https://arxiv.org/pdf/2211.05778.pdf
