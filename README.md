# ogl-macfix
## opengl-tutorials fix patches for MacOS

In MacOS, [opengl-tutorial](https://github.com/opengl-tutorials/ogl) does not work, because MacOS frequently drops support for old libraries(glfw, glew, glm) or tools(cmake).  
This repository contains following fixes regarding the issue:
* If configuaring system is MacOS, latest glew/glfw/glm is used.
  - Dependencies are considered to installed via `brew`, so running `brew install glew glfw glm` may be required.
* latest version of xcode is supported.
* cmake 4 is supported(works for all OS).
   

While successfully upgrading most of the dependency, It was unable to fix [ANTTWEAKBAR](https://anttweakbar.sourceforge.io/doc/).  
Original version AND forked fix ([tschw/AntTweakBar](https://github.com/tschw/AntTweakBar)) have stopped maintaing long ago, and completly broken in MacOS.  
Therefore, following projects are currently not working, and excluded from `ALL_BUILD` only in MacOS :
* tutorial17_rotations
* misc05_picking_slow_easy
* misc05_picking_custom
* misc05_picking_BulletPhysics
  
Other projects works well, with both xcode and makefile generator in cmake 4.  
  
  
Fix for MacOS does not affect behavior in other platform. Besides, [latest cmake support patch](https://github.com/awidesky/ogl-macFix/compare/fdbb1877ea42e51deb87a86bc162ac13fd8403f9..5d9403b3f509e848ef038ada4f74c0759a1f1476) is for all OS, so both cmake 4 and 3 should work in all OS and generator.
  
    
  

컴퓨터그래픽스 수업 실습을 위해 오신 경우, 혹시라도 설치나 빌드, 사용 중 문제가 생기면 issue에 남겨 주세요.  
환경과 오류 메시지를 알려 주시면 최대한 도움 드리겠습니다.
