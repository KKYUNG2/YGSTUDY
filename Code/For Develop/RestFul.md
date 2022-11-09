# Rest

- 자원을 이름(자원의 표현)으로 구분하여 해당 자원의 상태(정보)를 주고 받는 모든 것을 의미합니다. 즉, 자원(resource)의 표현(representation)에 의한 상태 전달을 말합니다.
- REST는 ROA(Resource Oriented Architecture)를 따르는 웹 서비스 아키텍처입니다.
- 구체적인 의미로 HTTP URL(Uniform Resource Identifier)를 통해 자원(Resource)을 명시하고, HTTP Method(POST, GET, PUT, DELETE)를 통해 해당 자원에 대한 CRUD Operation을 적용하는 것을 의미합니다.

# Restful 웹서비스 개요
- **Rest의 원리를 따르는 시스템 = Restful**
- **HTTP와 URL기반으로 자원에 접근하는 어플리케이션 개발 인터페이스 방식을 말함.**

# Restful
- 일반적으로 REST라는 아키텍처를 구현하는 웹 서비스를 나타내기 위해 사용되는 용어입니다.
- REST API를 제공하는 웹 서비스를 Restful하다고 할 수 있습니다.
- 즉, REST 원리를 따르는 시스템은 Restful이란 용어로 지칭됩니다.

# Restful하지 못한 경우
- CRUD 기능을 모두 POST로만 처리하는 API
- 라우트(route)에 resource, id 외의 정보가 들어가는 경우(/books/updateName)