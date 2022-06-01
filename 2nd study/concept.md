###### 2022-05-30 발표   
## Thin Lens Fomula
Pinhole camera에서 pinhole을 통과하는 모든 ray(광선)들은 film에 사영된다.   
이때 pinhole의 크기에 따라 투과되는 ray의 수가 달라지기 때문에 film에 맺히는 상도 다른 형태를 보일 것이다.   
* pinhole의 크기가 클 때
<img width="363" alt="image" src="https://user-images.githubusercontent.com/97183032/170949285-d44200b0-3073-48b2-b6e6-7f0cccd3401a.png">
더 많은 ray들이 들어오기 때문에 밝지만, 여러 ray가 사영되기 때문에 blur(흐림)가 생긴다.   
<br/><br/>
* pinhole의 크기가 작을 때
<img width="371" alt="image" src="https://user-images.githubusercontent.com/97183032/170949328-d2a5476c-a920-44a5-86d2-ef4a898f89c3.png">
더 적은 ray들이 들어오기 때문에 어둡지만, ray가 클때보다는 더 선명하다.  
<br/><br/>  
따라서 pinhole의 크기가 적당해야 선명한 영상을 얻을 수 있다.! (주의사항 : pinhole의 크기가 너무 작으면 회절이 발생한다.)   

## Lens
Lens는 film에 빛을 모아주는 역할을 한다.
### Lens의 중요한 2가지 가정(thin lens assumption)
1. lens의 중심을 지나는 RAY는 휘어지지 않는다.<br/><img width="237" alt="image" src="https://user-images.githubusercontent.com/97183032/170951500-eb5a8216-cf69-4aa9-98a4-a8412abbe5be.png">
2. optical axis(렌즈의 중심을 지나므로 굴절이 되지 않는 axis)와 평행한 ray는 focal point를 지난다.<br/><img width="232" alt="image" src="https://user-images.githubusercontent.com/97183032/170951840-afbd54e4-f3fb-48c0-bd78-8a6000c4d860.png">   
이렇게 lens를 통과한 ray들은 <strong>focal point가 film에 정확히 있어야</strong> 물체의 상이 잘 맺힐 것이다.    
### Lens와 물체와의 거리에 따른 상
* 물체가 가까울 때 : 원래 상이 맺히는 거리보다 짧기 때문에 ray들이 뭉쳐보인다.<br/><img width="363" alt="image" src="https://user-images.githubusercontent.com/97183032/170952539-d1a6e53d-ed3f-4848-926e-cc22db55c4eb.png">
* 물체가 멀 때 : focal point를 지난뒤 상이 맺혀서 마찬가지로 ray들이 뭉쳐보인다.<br/><img width="366" alt="image" src="https://user-images.githubusercontent.com/97183032/170952657-ac03ba9f-2e37-4514-b058-cd1a82a2d104.png">
* 물체가 적당한 거리일 때 : <strong>focal point가 film에 딱 맞게 되고</strong>, 선명한 상을 얻을 수 있다.<br/><img width="365" alt="image" src="https://user-images.githubusercontent.com/97183032/170952734-37658f09-ce63-4012-8f06-855114c7d7ff.png">
<br/><br/>
## image plane에 상을 잘 맺히게 하기 위한 물체 , lens, focal point 사이의 관계
위에서 살펴본 lens의 중요한 2가지 가정을 유념하며 그림 그리기.   
( Y : 물체의 높이, D : 물체부터 lens 까지 거리, D’ : lens 부터 image plane 까지 거리, f : lens 부터 focal point 까지 거리)   

<img width="289" alt="image" src="https://user-images.githubusercontent.com/97183032/170953266-75a2abfd-e370-4eaa-83ad-5944355f4cb5.png">
<img width="260" alt="image" src="https://user-images.githubusercontent.com/97183032/170953599-9ae01373-0cf4-48ab-aeb1-c61dc6034f07.png">   
닮은비를 이용하여 식 2개 유도 가능하다.  
<img width="81" alt="image" src="https://user-images.githubusercontent.com/97183032/170954313-c8e32a8f-e532-4bd3-8f34-a1df36135d62.png">
<img width="63" alt="image" src="https://user-images.githubusercontent.com/97183032/170954348-6e64ea7b-02ef-4bf1-88d2-f7a2a84aa8dc.png">

닮음비가 같음을 이용하여 유도한 2개의 식을 같다고 놓으면 아래와 같은 결과 유도 가능하다.   
<img width="98" alt="image" src="https://user-images.githubusercontent.com/97183032/170954414-a4763d6e-e185-4a0e-86ca-b12e9f0aba59.png">   
따라서 D, D’, f 를 잘 조정하면 image plane에 상이 잘 맺히게 조절할 수 있다.   
하지만 D와 f를 조절하는 것은 현실적으로 쉽지 않기 때문에 보통  <strong>D’(lens와 image plane 사이의 거리)를 조정해서</strong> in-focus 상태로 맞추게 된다.
<br/><br/>
## Depth of Field(DoF)
Depth of Field는 '초점이 맞는 범위'를 의미한다. (사진상에서 초점이 맞아서 선명하게 보이는 범위) 피사체의 위치가 best focus로부터 가까워지거나 멀어질 때 refocusing 없이 원하는 이미지 품질을 유지할 때 쓰인다.<br/>
<strong>aperture size(조리개 크기)를 조절</strong>해서 조정할 수 있다.   
<img width="309" alt="image" src="https://user-images.githubusercontent.com/97183032/170955454-37894cd9-de9b-45d7-ba99-ea7e92710d99.png">   
* 작은 aperture size를 가진다면   
들어오는 ray들이 더 확실하게 나누어져서 DoF가 증가, 그러나 들어오는 빛의 양이 적어져 어두운 이미지가 생성된다.
* 큰 aperture size를 가진다면   
반대로 DoF감소, 대신 더 밝은 이미지가 생성된다.
<br/><br/>
## Field of View(FoV)
Field of View(FoV)는 '카메라가 담을 수 있는 각도(화각)'을 의미한다.   
<img width="272" alt="image" src="https://user-images.githubusercontent.com/97183032/170956126-29c763f4-3b46-4b52-adeb-38d41eff3514.png">   
FoV를 크게하려면, 즉 카메라가 더 넓은 각도를 담으려면 f 감소 or d 증가 시킨다.  
그러나 현실적으로 d 조절은 힘드므로 <strong>f 를 감소시켜서 카메라가 더 넓은 각도를 담을 수 있게한다.</strong> 이 방식은 카메라의 줌(zoom)을 조절하는 방식에 사용된다.   
## Color image
컬러 영상은 R,G,B 3가지 색상정보를 모두 담기 위한 R,G,B 3개의 channel로 이루어진다.   
비용적인 문제로 인해 비싼카메라가 아니라면 보통 color filter를 1개만 사용한다.   
### color filter 1개로 3가지 색(R,G,B) 표현하는 방법
<img width="207" alt="image" src="https://user-images.githubusercontent.com/97183032/170957388-709066c4-5e67-4797-a93f-33962ccf6907.png"> <img width="213" alt="image" src="https://user-images.githubusercontent.com/97183032/170957406-6f196171-1fca-4281-b6dc-42dae3aea6be.png">   
픽셀마다 특정 색만 통과가능한 filter를 적용해서 색이 없는 부분들은 주변 색들의 평균값으로 interpolation(보간)해서 채워준다.   
<br/><br/>
## Image filtering
영상에는 여러 noise type이 있다. (noise : 원본영상보다 흐릿하게 보이거나, 점들이 있는 부분)   
<img width="194" alt="image" src="https://user-images.githubusercontent.com/97183032/170958967-63400ec3-5ed3-4a52-9e49-fa4b425d28c1.png">   
* salt and pepper noise : 검은점과 흰점
* impulse noise : 갑자기 튀는 흰색 점
* gaussian noise : 정규분포를 따르는 값이 random하게 더해진 것   

<strong>영상의 noise들을 제거하기 위해 weight average</strong>(가중치를 곱하는 것)을 이용한다. (weight들은 filter(kernel)이라고도 한다.)   
input영상에 대해 Filter를 한칸씩 이동하면서 각 성분과 곱한 합을 계산하고, 이 값을 해당 filter의 가운데 위치(index)의 값으로 저장된다.   
* 1차원일 때   <br/><img width="218" alt="image" src="https://user-images.githubusercontent.com/97183032/170959808-0a431a77-350d-4b90-b83e-7a7afc40ab28.png">  
* 2차원일 때   <br/><img width="283" alt="image" src="https://user-images.githubusercontent.com/97183032/170959923-eea886b8-c2da-469c-bb2a-8c03be7ecd1e.png"><br/>
2차원일 때도 1차원과 비슷한 원리로 2차원의 필터를 이용하여 2차원의 output을 얻어낸다.   
이런 계산과정을 <strong>convolution</strong>이라고 한다.
### convolution 연산 성질
* commutative: fg=gf   
* associative: (fg)h=f(gh)   
* scalars factor out: kfg=fkg=k(f*g)   
* distributes over+: f*(g+h)=fg+fh   
<br/><br/>
## Edge case
영상의 edge(테두리) 조건에 따라 convolution을 하는 경우를 지정해줄 수도 있다. 따라서 출력영상의 크기도 조절가능하다.   
<img width="389" alt="image" src="https://user-images.githubusercontent.com/97183032/170961380-e909c4ca-9247-45c9-a86a-0d0e495723b1.png">   
(f는 입력영상, g는 filter)   
* full : g의 한 부분이라도 입력영상의 값이 있으면 convolution 연산을 수행한다. <strong>출력영상은 원래 영상보다 커진다.</strong>   
* same : g의 중앙위치에 입력영상의 값이 있으면 convolution 연산을 수행한다. <strong>출력영상은 원래 영상과 동일하다.</strong> 
* valid : g의 모든위치에 입력영상의 값이 있으면 convolution 연산을 수행한다. <strong>출력영상은 원래 영상보다 작아진다.</strong>   
<br/>
full이나 same에서 출력영상이 입력영상보다 크거나 같은 크기로 나오면, filter사이의 비워져 있는 부분을 3가지 option을 이용하여 처리 가능하다.   
<img width="134" alt="image" src="https://user-images.githubusercontent.com/97183032/170962078-a37a5e3c-976f-4565-8257-1dcde7731e72.png">   
1. Symm : filter 바로 아래 값 copy해서 채우기   <br/>
2. Circular/wrap : 영상이 순환적으로 이어져있다 생각하고 맨 아래와 위에 값 copy해서 채우기   <br/>
3. Pad/fill : 0으로 모든 값 채우기(=zero padding)   
<br/><br/>

## Linear filter
<img width="350" alt="image" src="https://user-images.githubusercontent.com/97183032/170964563-0a9dd89c-f4f7-4d6a-9c90-a40bf6e54d25.png">   
(출처 : https://youtu.be/WeNpd_YEF6I )   <br/>
영상을 더 sharpening(또렷하게)하는 원리는 입력영상에서 부드러운부분을 빼주면 detail한 부분만 남게된다.   
<img width="358" alt="image" src="https://user-images.githubusercontent.com/97183032/170964796-e68333cc-dae5-4f3b-8383-884b4b69efe2.png">   
이때 원본 영상에 detail한 부분의 가중치를 부여해서 더해주면 더 sharp(또렷)한 영상을 얻을 수 있다. 그리고 가중치를 더 많이 부여할수록 더욱 sharp해진다.   
<img width="281" alt="image" src="https://user-images.githubusercontent.com/97183032/170965207-d0109457-22c5-498d-a5bc-de069e6d5c9f.png">   
<br/><br/>

## Box smoothing
영상이 모자이크된 것 처럼 박스모양으로 보일때, box smoothing을 통해 해결가능하다.   
<img width="300" alt="image" src="https://user-images.githubusercontent.com/97183032/170998020-8241039e-a50b-48a0-9b38-b36bf2846b13.png">   
per-pixel weights(중앙으로부터 거리에 따라 값이 다른 filter, 즉 gaussian filter)을 적용하여 해결한다.   
필터의 시그마(분산)을 조정하여 필터의 크기 조절 가능하며, 보통 필터크기의 1/6정도로 시그마를 설정한다.   
<img width="358" alt="image" src="https://user-images.githubusercontent.com/97183032/170998708-de4cbe94-f948-4e81-94c5-ed55bd88cac6.png">   
그런데 모자이크 noise말고 흰 색점들이 있는 noise에서는, 큰 값의 noise가 존재하기 때문에 gaussian filter를 적용해도 여전히 큰 값을 가진다.   
이 문제를 해결하기 위해 median filter를 사용한다.
<br/><br/>
## Median filter
말 그대로 중간값을 사용하는 필터이다.   
output들의 값들을 정렬해서 중간값을 선택한다면 큰 값이 선택되지 않을 것이다.   
<img width="316" alt="image" src="https://user-images.githubusercontent.com/97183032/170999368-d862a48d-e341-47ff-b94a-bfc5fa2123cd.png">   
<br/><br/>
## 실습
* [average filtering 실습](https://github.com/dalsu0222/Computer-Vision-Study/blob/main/2nd%20study/average_filtering.ipynb)
* [image sharpening 실습](https://github.com/dalsu0222/Computer-Vision-Study/blob/main/2nd%20study/image_sharpening.ipynb)
* [Gaussian filter & Median filter 실습](https://github.com/dalsu0222/Computer-Vision-Study/blob/main/2nd%20study/Gaussian_filter%26Median_filter.ipynb)
* [사진으로 실습해보기](https://github.com/joomj2000/Computer-Vision/blob/main/study_2/%EC%82%AC%EC%A7%84%EC%9C%BC%EB%A1%9C_%EC%8B%A4%EC%8A%B5%ED%95%B4%EB%B3%B4%EA%B8%B0.ipynb)
