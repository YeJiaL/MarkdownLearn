# 目录

[TOC]

## 前端

### JS判断输入的字符串是否是数字

```javascript
if (!checkNumber(gopage_val)) {
  alert("请输入正确页数(数字)");
  return false;
 }
//验证字符串是否是数字
function checkNumber(theObj) {
  var reg = /^[0-9]+.?[0-9]*$/;
  if (reg.test(theObj)) {
    return true;
  }
  return false;
}
```

### 指定元素存在执行某个操作

```javascript
if (exist){
  function1;
}else{
  var name=setInterval(function () {
  if (exist) {
     clearInterval(name);
     function1;
                }
  }, 1000 );
}
举例：
  if ($( target).data ('bootstrap.select'). $contentDownList) {
  setValues($ (target). data('bootstrap.select' ), values);
  } else {
  var int = setInterval(function () {
  if ($( target).data ('bootstrap.select'). $contentDownList) {
  clearInterval(int );
  setValues($ (target). data('bootstrap.select' ), values );
  }
  }, 1000 );
  }
```

### 0 alse null underfined比较

![0 alse null underfined比较](/img/JsCompare.png "0 alse null underfined比较")

## .Net

### C#中List〈string〉和string[]数组之间的相互转换

```c#
// 1.从System.String[]转到List<System.String>
System.String[] str={"str","string","abc"};
List<System.String> listS=new List<System.String>(str);
// 2.从List<System.String>转到System.String[]
List<System.String> listS=new List<System.String>();
listS.Add("str");
listS.Add("hello");
System.String[] str=listS.ToArray();
```

### layout的时候js加载顺序问题

当使用layout的时候，会提前运行此类代码，及时初始化函数放在上面也可以执行
git branch git testing
123

```js
1<script src ="~/Areas/Clt/Scripts/Report/reportRecordVue.js"></ script>
2 <script type ="text/javascript">
3var report = @ Html.Raw(ViewData["report" ]);
4 </script >即234行先执行，当中的Report变量可用

当不适用layout的时候，
@{
    Layout = null;
}

<script type ="text/javascript">
    var report = @ Html.Raw(ViewData["report" ]);
    </script >
    <script src ="~/Areas/Clt/Scripts/Report/reportRecordVue.js"></ script >
```

需将使用的变量放在前面

建议：无论使用不适用layout都放在初始化js的前面

### ibaits集合形式

```sql
select id =" queryConsultationByRefidList" resultMap="result" parameterClass="System.Collections.IList" >
      SELECT *
      FROM table c
      WHERE c.REFID in
      < iterate open =" (" close= ") " conjunction=",">
        #[]#
      </ iterate>
    </ select>

在ibaits中使用iterate，若传入的是一个list对象，如list<string> aaa等，则传入的参数不必命名为#aaa[]#,直接命名为#[]#即可,此时可不加property属性
                      若传入的是一个list对象中还包含有对象，如list<student> aaa等，若要匹配student中的参数，则传入的参数命名为#student[].name#
猜测？？：若传入的是基本类型（list里面装的类型数据是基本类型）则直接命名使用，
          若传入的是非基本类型（自己定义的model），则#model[].propertyname#
```

## Java

### 前后台处理方式

```Java
前台参数传递到后台：
var jsonStr = [ {
'name' : 'jim',
'age' : 20
}, {
'name' : 'king',
'age' : 26
}, {
'name' : 'jge',
'age' : 30
} ];
var url="./AjaxDemo/toGetJsonData_reponse.jsp";
$.ajax({
type : "post",
url : url,
dataType : 'json',
data : {
'mydata' : JSON.stringify(jsonStr)//注意一定要使用JSON.stringify (在IE6，IE7中不支持)
}
后台取数据
//  String jsonStr = "[{'name':'jim','age':20},{'name':'king','age':26},{'name':'jge','age':30}]";
String jsonStr = request.getParameter("mydata");
JSONArray jsonArray = JSONArray.fromObject(jsonStr);
String name = "";
String age = "";
for (int i = 0; i < jsonArray.size(); i++) {//int为后台，前台为var
JSONObject jsonJ = jsonArray.getJSONObject(i);
name = jsonJ.getString("name");
age = jsonJ.getString("age");
}
```