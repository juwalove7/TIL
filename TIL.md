# TIL
9/7

1. class 를 띄워쓰기 기준으로 class 명을 여러개 줄 수 있다.

```jsx
<button class="all__btn img__btn img__btn update__btn">
```

2. table 에서 colgroup 은 table 의 첫번째 자식 요소로 배치되며, 각 그룹을 나타내는 
    
    col 요소를 포함한다.
    

```jsx
<table class="tableClass">
						<colgroup>
							<col width="25%">
							<col width="25%">
							<col width="25%">
							<col width="25%">
						</colgroup>
						<tr>
							<th class="thNeed">환자ID</th>
							<td colspan="3"><input type="text" class="tdInputClass" placeholder="test" maxlength="20" style="width: 28%; height: 50%;" readonly="readonly" disabled="disabled" /></td>
						</tr>
```

3. colspan은 여러 열(column)을 병합하는 데 사용된다.

```jsx
<th colspan="값">헤더 내용</th>
<td colspan="값">내용</td>

<table border="1">
  <tr>
    <td>열 1</td>
    <td>열 2</td>
    <td colspan="2">열 3과 4를 병합</td>
    <td>열 5</td>
  </tr>
  <tr>
    <td>데이터 1</td>
    <td>데이터 2</td>
    <td>데이터 3</td>
    <td>데이터 4</td>
    <td>데이터 5</td>
  </tr>
</table>
```

4. placeholder 는 입력 필드가 비어 있을 때 보이는 임시 텍스트를 설정할 수 있다.

```jsx
placeholder="test"
```

5. maxlength 는 입력 필드에 제한된 길이만큼 입력하도록 할 수 있다.

```jsx
<input type="text" maxlength="숫자">
```

6. readonly 는 해당 입력 필드를 읽기 전용(read-only) 상태로 만든다.
    
    읽기 전용 필드는 사용자가 내용을 편집하거나 수정할 수 없으며, 
    
    단순히 내용을 표시하거나 읽을 수만 있다.
    

```jsx
<input type="text" readonly="readonly">
```

7. disabled 는 사용자에게 특정 조건이나 상황에서 폼 요소를 비활성화 하는데 사용한다.

```jsx
<button type="submit" disabled="disabled">전송</button>
```

8. 기본적으로 웹 브라우저는 클릭 이벤트가 발생하면 해당 요소에 연결된 기본 동작(예: 링크를 따라가거나 폼을 제출하는 등)을 수행하려고 한다.
    
    그러나 **`onclick="return false"`**를 사용하면 이 기본 동작을 중지할 수 있다.
    

```jsx
onclick="return false"
```

9. input 안에 placeholder 내용이 아닌 id 로 지정해준 걸로 value의 내용을 집어넣을 수 있다.

```jsx
<input id="inputNumId" placeholder="'-'를 제외하고 입력해주세요." />

<script>
document.getElementById("inputNumId").value = "01012345678";
</script>
```

10. **`oninput`** 이벤트는 사용자가 입력 필드에 텍스트를 입력하거나 수정할 때마다 발생하며, 
    
    보통 실시간으로 입력 내용을 검증하거나 처리하는 데 사용된다.
    

```jsx
<input oninput="this.value = this.value.replace(/[^0-9.]/g, '').replace(/(\..*)\./g, '$1');" />
```

11. css에서 가상선택자 사용

```css
.class명::before { content: "*" }  ->  class로 지정된 것 앞에 *를 넣는다.
.class명::before { content: "*" }  ->  class로 지정된 것 뒤에 *를 넣는다.
```


9/8

1. input 에서 날짜를 선택할 수 있는 type의 종류

```jsx
<input type="date" />  -->  날짜를 선택할 수 있는 달력을 표시(YYYY-MM-DD)
<input type="time" />  -->  시간을 입력할 수 있는 입력 상자 표시(오전,오후-H-M)
<input type="datetime-local" />  -->  날짜와 시간을 선택할 수 있는 입력 상자 표시(YYYY-MM-DD -H-M-오전,오후)
<input type="month" />  -->  연도와 월을 선택할 수 있는 입력 상자 표시(YYYY-MM)
<input type="week" />  -->  연도와 주차를 선택할 수 있게 표시(YYYY-몇번째 주)
```
