# Tacotron Korean TTS implementation using Tensorflow2

### Requirements
* Python 3.7
* tensorflow 2.0 이상
* jamo

### Environments
- ubuntu 20.04
- RTX 3070ti
- Nvidia-driver-470
- [CUDA 11.2](https://developer.nvidia.com/cuda-11.2.0-download-archive)
- [cuDNN 8.1.1](https://developer.nvidia.com/cudnn)
- python 3.7
- tensorflow 2.7.0
- tensorflow-gpu 2.7.0
- keras 2.7.0
- jamo 0.4.1
- matplotlib 3.5.1
- numpy 1.21.6
- pandas 1.3.5

### [ubuntu 20.04 기본 설정](https://github.com/favorcat/TIL/blob/main/ubuntu/setting.md)

### Training

1. **한국어 음성 데이터 다운로드**

    * [KSS](https://www.kaggle.com/bryanpark/korean-single-speaker-speech-dataset)

2. **`~/Tacotron-Korean-Tensorflow2`에 학습 데이터 준비**

   ```
   Tacotron-Korean-Tensorflow2
     |- kss
         |- 1
         |- 2
         |- 3
         |- 4
         |- transcript.v.1.x.txt
   ```

3. **Preprocess**
   ```
   python preprocess.py
   ```
     * data 폴더에 학습에 필요한 파일들이 생성됩니다

4. **Train**
   ```
   python train1.py
   python train2.py
   ```
     * train1.py - train2.py 순으로 실행합니다
     * 저장한 모델이 있으면 가장 최근의 모델을 불러와서 재학습합니다

5. **Synthesize**
   ```
   python test1.py
   python test2.py
   ```
     * test1.py - test2.py 순으로 실행하면 output 폴더에 wav 파일이 생성됩니다



윈도우에서 Tacotron 한국어 TTS 학습하기
  * https://chldkato.tistory.com/141
  
Tacotron 정리
  * https://chldkato.tistory.com/143
