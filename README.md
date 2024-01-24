- 2.1~2.4
  - Q. 객체지향 프로그래밍이 절차적 프로그래밍에 비해 유리한 면은 무엇인가요?
  - (민철) Q. 객체지향 프로그래밍이 절차적 프로그래밍보다 대규모의 복잡한 프로그램 개발에 더 적합한 이유를 설명해주세요.
  - Q. (2.2.4) `Iterator` 를 예시로 들어 다형성을 설명해주세요.
  - Q. (정희) (2.2.1) 캡슐화의 장점에 대해서 설명해주세요.
  - Q. 추상화를 이용하면 사람이 복잡한 시스템을 잘 다룰 수 있게 된다고 합니다. 왜 그런가요?
  - Q. (2.2.2) 우리는 객체지향 프로그래밍을 시도하지만 나도 모르게 절차적 프로그래밍으로 개발하게 되는 경우가 있습니다. 무엇을 놓친걸까요?
  - Q. (2.2.1) 외부로부터의 접근 제한을 통해 필요한 데이터, 기능만을 외부에 노출시키는것을 `캡슐화` 라고 합니다. javascript를 통해 캡슐화를 보여주는 예시코드를 작성해주세요.
  - (무호) Q. (2.3.3) 요구 사항을 전달 받고 나서 객체지향 설계를 하려면 어떻게 해야 하나요?
  - Q. (2.2.3) 상속은 어떤 단점이 있나요?
  - ====
  - Q. 다음 코드에서 각 클래스의 관계는 일반화, 실체화, 합성, 의존 관계 중 무엇일까요?
  1. DefaultApiAuthenticator - ApiAuthenticator
  2. DefaultApiAuthenticator - MysqlCredentialStorage
  3. DefaultApiAuthenticator - ApiRequest

     ```java
     public interface ApiAuthenticatior {
       void auth(String url);
       void auth(ApiRequest apiRequest);
     }

     public class DefaultApiAuthenticatorImpl implemens ApiAuthenticator {
       private CredentialStorage credentialStorage;

       public DefaultApiAuthenticator () {
         this.credentialStorage = new MysqlCredentialStorage();
       }

       public DefaultApiAutenticator (CredentialStorage credentialStorage) {
         this.credentialStorage = credentialStorage;
       }

       @Override
       public void auth(ApiRequest apiRequest) {
          ...
       }
     }
     ```
- 2.5 ~ 2.6
  - Q. 풍성한 도메인 모델 기반 개발 방식과 빈약한 도메인 모델 기반 개발 방식의 차이
  - Q. 풍성한 도메인 모델 기반의 개발 방식이 필요한 경우에 대해서 설명해주세요.
  - Q. DDD는 언제 사용하는 것이 적합한가요?
  - Q. 풍성한 도메인 모델(ex. DDD)과 빈약한 도메인 모델(ex. MVC)의 차이점은 무엇인가요?
  - Q. DDD에서 비즈니스 논리는 Domain 클래스에 집중됩니다. 그럼에도 불구하고 Service 클래스가 남아 있어야 하는 이유는 무엇인가요?
  - Q. 다음 코드는 OOP의 장점을 위배하는 좋지 않은 코드입니다. 어떤 문제점이 발생할 수 있는지 설명해주세요.
    ```java
    public class ShoppingCart {
      private int itemsCount;
      private double totalPrice;
      private List<ShoppingCartItem> items = new ArrayList<>();

      public int getItemsCount() {
        return this.itemsCount;
      }

      public int setItemsCount(int itemsCount) {
        this.itemsCount = itemsCount;
      }

      public double getTotalPrice() {
        return this.totalPrice;
      }

      public double setTotalPrice(double totalPrice) {
        this.totalPrice = totalPrice;
      }

      public List<ShoppingCartItem> getItems() {
        return this.items;
      }

      public void addItem(ShoppingCartItem item) {
        this.items.add(item);
        this.itemsCount++;
        this.totalPrice += item.getPrice();
      }
    }
    ```
- 2.7 ~ 2.9
  - Q. 추상 클래스와 인터페이스는 각각 어떤 문제를 해결하기 위해서 사용하나요?
  - Q. 상속과 합성 중에서 언제 상속 또는 합성을 사용하는 게 좋은가요?
  - Q. 인터페이스 기반 설계가 필요한 경우를 설명해주세요.
  - Q. 인터페이스 남용이 주는 문제는 무엇인가요? 남용을 방지하고자 하는 방법에는 무엇이 있나요?
  - Q. 상속이 만드는 문제는 무엇인가요? 이를 합성으로 어떻게 해결이 가능한가요?
