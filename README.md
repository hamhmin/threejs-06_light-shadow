### threejs-06_light-shadow


5가지 light와 shadow

## 배운 내용
- shadow 적용하기위한 작성법 
 * renderer.shadowMap.enabled = true;
 * receiveShadow(그림자를 생기는 영역에), castShadow(light와 그림자를 만들고자 하는 요소에)
- shadow 옵션
 * renderer.shadowMap.type
    * THREE.PCFShadowMap = 기본값
    * THREE.BasicShadowMap = radius 적용 안됨. 성능이 가장 좋음.
    * THREE.PCFSoftShadowMap = radius 적용안됨. 기본값보다 부드러운 시각 효과.
 * light.shadow
    * mapSize.width, heght = 
    * radius = shadow blur 값이 높을수록 흐림
    * camera.far = 그림자가 생성되는 최소 위치값
    * camera.near = 그림자가 생성되는 최대 위치값

 * Light 종류와 작성법
    * PointLight        = 정해진 위치에서 사방으로 빛이 퍼짐
    * SpotLight         = 원뿔 광원
    * HemisphereLight   = 두가지 색을 가진 광원
    * RectAreaLight     = 사각판 광원  // ligthHelper가 threejs에 내장되어있지않음. 사용하려면import 시켜야함'
 
 ## 응용
 * light.position.x = Math.cos(time)*5;
   light.position.y = Math.sin(time)*5;
   
  이용하여 밤낮을 만들 수 있을 것 같다.
    
    
    
