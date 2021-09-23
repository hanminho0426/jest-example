## facebook/jest

- 리액트의 영향이 크겠지만 가장 핫한 테스트 도구
- Easy Setsup
- Instant Feedback
  - 고친 파일만 빠르게 테스트 다시 해주는 기능 등
- Snapshot Testing
  - 컴포넌트 테스트는 중요한 역할을 하는 스냅샷
- npx jest --watchAll 항상 테스트 켜진상태 명령어

```js
describe("expect test", () => {
  //describe 데이터를 묶음
  it("37 to equal 37", () => {
    expect(37).toBe(37);
  });
  it("{age: 39} to equal {age:39}", () => {
    expect({ age: 39 }).toEqual({ age: 39 });
  });
  it(".toHaveLength", () => {
    //문자열 길이검사
    expect("Hello").toHaveLength(5);
  });
  it(".toHaveProperty", () => {
    //키와 값 확인
    expect({ name: "Mark" }).toHaveProperty("name");
    expect({ name: "Mark" }).toHaveProperty("name", "Mark");
  });
  it(".toBeDefined", () => {
    //Defined 되어있는지 확인
    expect({ name: "Mark" }.name).toBeDefined();
    //expect({ name: "Mark" }.age).toBeDefined(); age는 undefined이기 때문에 오류
  });
  it(".toBeFalsy", () => {
    //Falsy한 값
    expect(false).toBeFalsy();
    expect("").toBeFalsy();
    expect(0).toBeFalsy();
    expect(null).toBeFalsy();
    expect(undefined).toBeFalsy();
    expect(NaN).toBeFalsy();
  });
  it(".toBeGreaterThan", () => {
    //보다 큰 값
    expect(10).toBeGreaterThan(9); //10은 9보다 큰 값
  });
  it(".toBeGreaterThanOrEqual", () => {
    //크거나 같은 값
    expect(10).toBeGreaterThanOrEqual(10); //10은 10보다 크거나 같은 값
  });
  it(".toBeInstanceOf", () => {
    class Foo {}
    expect(new Foo()).toBeInstanceOf(Foo);
  });
});
```
