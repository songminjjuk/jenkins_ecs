# jenkins_ecs
CI/CD configuration with ECS using Jenkins

frontend 폴더 안에 있는 React app의 소스 코드가 변경이 되면, 이를 감지해서 Jenkins 서버로 trigger를 하여 react-pipeline을 실행
backend 폴더 안에 있는 Spring app의 소스 코드가 변경이 되면, 이를 감지해서 Jenkins 서버로 trigger를 하여 spring-pipeline을 실행
github_webhook을 이용하지 않고 별도의 workflow 파일을 작성하여 trigger를 보내게 한 이유는 react 소스 코드만 변경이 되었을 때는 spring 소스 코드를 빌드할 필요 x
마찬가지로, spring 소스 코드만 변경이 되었을 때는 react 소스 코드를 빌드할 필요 x
이를 구분하기 위해서 github repository 단위로 hook을 보내는 github_webhook 말고 workflow 파일을 작성하여 별도로 trigger를 보내주게 구성함 
